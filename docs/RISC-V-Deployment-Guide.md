# PicoClaw RISC-V Deployment Guide

## Overview

PicoClaw is a lightweight AI assistant optimized for resource-constrained environments, with full support for RISC-V architecture. This guide provides comprehensive instructions for deploying PicoClaw on RISC-V boards.

## Supported Hardware

| Board | CPU | RAM | Price | Best For |
|-------|-----|-----|-------|----------|
| LicheeRV-Nano | C906 @ 1GHz | 256MB | $9.9 | Home Assistant |
| NanoKVM | RISC-V | Varies | $30-50 | Server Management |
| NanoKVM-Pro | RISC-V | Varies | $100 | Enterprise KVM |
| MaixCAM | RISC-V + AI | 256MB | $50 | AI Camera |
| MaixCAM2 | RISC-V + AI | 512MB | $100 | 4K AI Camera |

## Installation Methods

### Method 1: Pre-compiled Binary (Recommended)

```bash
# Download RISC-V binary
wget https://github.com/sipeed/picoclaw/releases/latest/download/picoclaw_Linux_riscv64.tar.gz

# Extract
tar -xzf picoclaw_Linux_riscv64.tar.gz

# Install
sudo mv picoclaw /usr/local/bin/
sudo chmod +x /usr/local/bin/picoclaw

# Initialize
picoclaw onboard
```

### Method 2: Cross-Compilation

On your development machine (x86_64/ARM64):

```bash
# Clone repository
git clone https://github.com/sipeed/picoclaw.git
cd picoclaw

# Build for RISC-V
GOOS=linux GOARCH=riscv64 make build

# Transfer to RISC-V board
scp build/picoclaw-linux-riscv64 root@<board-ip>:/usr/local/bin/picoclaw
```

### Method 3: Build on RISC-V Board

```bash
# Clone repository
git clone https://github.com/sipeed/picoclaw.git
cd picoclaw

# Install dependencies
make deps

# Build
make build

# Install
make install
```

## Configuration

### Minimal Configuration for RISC-V

Create `~/.picoclaw/config.json`:

```json
{
  "agents": {
    "defaults": {
      "workspace": "~/.picoclaw/workspace",
      "model": "glm-4.7",
      "max_tokens": 2048,
      "temperature": 0.7,
      "max_tool_iterations": 10,
      "restrict_to_workspace": true
    }
  },
  "providers": {
    "zhipu": {
      "api_key": "YOUR_API_KEY",
      "api_base": "https://open.bigmodel.cn/api/paas/v4"
    }
  },
  "tools": {
    "web": {
      "duckduckgo": {
        "enabled": true,
        "max_results": 5
      }
    }
  }
}
```

### Memory Optimization

For boards with limited RAM (< 256MB):

```json
{
  "agents": {
    "defaults": {
      "max_tokens": 1024,
      "max_tool_iterations": 5
    }
  }
}
```

## Hardware Access (I2C/SPI)

### Enable I2C

```bash
# Load I2C module
modprobe i2c-dev

# Verify I2C buses
ls /dev/i2c-*

# Detect buses
picoclaw agent -m "i2c detect"
```

### LicheeRV-Nano Pinmux Configuration

```bash
# Stop WiFi (I2C shares pins with WiFi)
/etc/init.d/S30wifi stop

# Configure pinmux for I2C-1
devmem 0x030010d0 32 0x2  # SCL
devmem 0x030010d4 32 0x2  # SDA

# Scan for devices
picoclaw agent -m "i2c scan bus:1"
```

### Read Sensor Data

Example: Reading AHT20 temperature/humidity sensor:

```bash
picoclaw agent -m "i2c read bus:1 address:0x38 register:0xAC length:6"
```

## Performance Benchmarks

### LicheeRV-Nano (C906 @ 1GHz, 256MB RAM)

- **Boot time**: ~0.8s
- **Idle RAM**: 6-8 MB
- **Peak RAM**: ~15 MB
- **Response time**: 1-3s (API dependent)

### Resource Usage by Operation

| Operation | RAM Usage | CPU Usage |
|-----------|-----------|-----------|
| Idle | 6-8 MB | < 1% |
| Text chat | 10-12 MB | 5-10% |
| Web search | 12-15 MB | 10-15% |
| File operations | 8-10 MB | 5-8% |
| I2C/SPI access | 8-10 MB | 3-5% |

## Troubleshooting

### Permission Denied (I2C/SPI)

```bash
# Add user to i2c group
sudo usermod -a -G i2c $USER

# Or run as root
sudo picoclaw agent
```

### Out of Memory

Reduce token limit and iterations:

```json
{
  "agents": {
    "defaults": {
      "max_tokens": 512,
      "max_tool_iterations": 3
    }
  }
}
```

### WiFi Stops Working After I2C

I2C-1 and SPI-2 share pins with WiFi on many boards:

```bash
# Restart WiFi
/etc/init.d/S30wifi start

# Use I2C-0 instead if available
picoclaw agent -m "i2c scan bus:0"
```

## Resources

- [LicheeRV-Nano Wiki](https://wiki.sipeed.com/hardware/en/lichee/RV_Nano/1_intro.html)
- [PicoClaw GitHub](https://github.com/sipeed/picoclaw)
- [RISC-V International](https://riscv.org/)
- [Sipeed Documentation](https://wiki.sipeed.com/)

---

**Last Updated**: 2026-02-15  
**PicoClaw Version**: Latest

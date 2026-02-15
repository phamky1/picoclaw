<div align="center">
  <img src="assets/logo.jpg" alt="PicoClaw" width="512">

  <h1>PicoClaw: Trợ lý AI siêu hiệu quả được viết bằng Go</h1>

  <h3>Phần cứng $10 · RAM 10MB · Khởi động 1s · 皮皮虾，我们走！</h3>

  <p>
    <img src="https://img.shields.io/badge/Go-1.21+-00ADD8?style=flat&logo=go&logoColor=white" alt="Go">
    <img src="https://img.shields.io/badge/Arch-x86__64%2C%20ARM64%2C%20RISC--V-blue" alt="Hardware">
    <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
    <br>
    <a href="https://picoclaw.io"><img src="https://img.shields.io/badge/Website-picoclaw.io-blue?style=flat&logo=google-chrome&logoColor=white" alt="Website"></a>
    <a href="https://x.com/SipeedIO"><img src="https://img.shields.io/badge/X_(Twitter)-SipeedIO-black?style=flat&logo=x&logoColor=white" alt="Twitter"></a>
  </p>

 [中文](README.zh.md) | [日本語](README.ja.md) | [English](README.md) | **Tiếng Việt**
</div>

---

## 🦐 Giới thiệu

PicoClaw là một trợ lý AI cá nhân cực kỳ nhẹ được lấy cảm hứng từ [nanobot](https://github.com/HKUDS/nanobot), được tái cấu trúc hoàn toàn từ đầu bằng ngôn ngữ Go thông qua một quá trình tự khởi động (self-bootstrapping), trong đó chính AI agent đã điều khiển toàn bộ quá trình di chuyển kiến trúc và tối ưu hóa mã nguồn.

⚡️ Chạy được trên phần cứng $10 với RAM <10MB: Tiết kiệm 99% bộ nhớ so với OpenClaw và rẻ hơn 98% so với Mac mini!

<table align="center">
  <tr align="center">
    <td align="center" valign="top">
      <p align="center">
        <img src="assets/picoclaw_mem.gif" width="360" height="240">
      </p>
    </td>
    <td align="center" valign="top">
      <p align="center">
        <img src="assets/licheervnano.png" width="400" height="240">
      </p>
    </td>
  </tr>
</table>

> [!CAUTION]
> **🚨 BẢO MẬT & KÊNH CHÍNH THỨC**
>
> * **KHÔNG CÓ CRYPTO:** PicoClaw **KHÔNG** có token/coin chính thức. Mọi tuyên bố trên `pump.fun` hoặc các nền tảng giao dịch khác đều là **LỪA ĐẢO**.
> * **DOMAIN CHÍNH THỨC:** Website chính thức **DUY NHẤT** là **[picoclaw.io](https://picoclaw.io)**, và website công ty là **[sipeed.com](https://sipeed.com)**
> * **Cảnh báo:** Nhiều domain `.ai/.org/.com/.net/...` được đăng ký bởi bên thứ ba.
> * **Cảnh báo:** PicoClaw đang trong giai đoạn phát triển sớm và có thể có các vấn đề bảo mật mạng chưa được giải quyết. Không triển khai vào môi trường production trước phiên bản v1.0.

## ✨ Tính năng

🪶 **Siêu nhẹ**: Chỉ <10MB bộ nhớ — nhỏ hơn 99% so với Clawdbot - chức năng cốt lõi.

💰 **Chi phí tối thiểu**: Đủ hiệu quả để chạy trên phần cứng $10 — rẻ hơn 98% so với Mac mini.

⚡️ **Siêu nhanh**: Khởi động nhanh hơn 400 lần, chỉ 1 giây ngay cả trên CPU đơn nhân 0.6GHz.

🌍 **Khả năng di động thực sự**: File nhị phân tự chứa duy nhất trên RISC-V, ARM và x86, chỉ một cú nhấp chuột!

🤖 **Tự khởi động bằng AI**: Triển khai tự động bằng Go — 95% code cốt lõi được tạo bởi Agent với sự tinh chỉnh của con người.

|                               | OpenClaw      | NanoBot                  | **PicoClaw**                              |
| ----------------------------- | ------------- | ------------------------ | ----------------------------------------- |
| **Ngôn ngữ**                  | TypeScript    | Python                   | **Go**                                    |
| **RAM**                       | >1GB          | >100MB                   | **< 10MB**                                |
| **Khởi động**</br>(0.8GHz core) | >500s         | >30s                     | **<1s**                                   |
| **Chi phí**                   | Mac Mini 599$ | Hầu hết Linux SBC </br>~50$ | **Bất kỳ Board Linux nào**</br>**Chỉ từ 10$** |

<img src="assets/compare.jpg" alt="PicoClaw" width="512">

## 🔧 Tính năng chính

### 1. **Trợ lý AI đa năng**
- Chat tương tác thông minh với nhiều mô hình LLM
- Hỗ trợ nhiều nhà cung cấp: OpenRouter, Zhipu, Anthropic, OpenAI, Gemini, Groq
- Quản lý bộ nhớ dài hạn và ngữ cảnh hội thoại
- Tìm kiếm web tích hợp (Brave Search, DuckDuckGo)

### 2. **Công cụ (Tools) phong phú**
- **Hệ thống file**: Đọc, ghi, chỉnh sửa, liệt kê file
- **Shell**: Thực thi lệnh hệ thống
- **Web search**: Tìm kiếm thông tin trên internet
- **Cron**: Lập lịch tác vụ định kỳ
- **I2C/SPI**: Điều khiển phần cứng trực tiếp (đặc biệt cho RISC-V boards)
- **Spawn**: Tạo subagent cho tác vụ bất đồng bộ
- **Message**: Giao tiếp với người dùng

### 3. **Kết nối đa kênh**
Kết nối PicoClaw qua nhiều nền tảng chat:
- **Telegram** (Khuyến nghị - dễ cài đặt)
- **Discord**
- **QQ** (Trung Quốc)
- **DingTalk**
- **LINE**
- **CLI** (Command Line Interface)

### 4. **Skills mở rộng**
Hệ thống skills có thể tùy chỉnh:
- **GitHub**: Tương tác với repository GitHub
- **Hardware**: Điều khiển I2C/SPI peripherals
- **Weather**: Kiểm tra thời tiết
- **Tmux**: Quản lý terminal sessions
- **Summarize**: Tóm tắt văn bản
- **Skill Creator**: Tạo skills mới

### 5. **Tính năng bảo mật**
- Sandbox môi trường làm việc
- Giới hạn truy cập file và lệnh
- Bảo vệ khỏi các lệnh nguy hiểm
- Xác thực người dùng trên các kênh chat

### 6. **Tác vụ định kỳ (Heartbeat)**
- Thực hiện tác vụ tự động theo lịch
- Kiểm tra email, lịch, thời tiết định kỳ
- Chạy background tasks với subagent

## 🚀 Triển khai trên RISC-V

PicoClaw hỗ trợ đầy đủ kiến trúc RISC-V, đặc biệt được tối ưu cho các board Sipeed.

### ⚙️ Phần cứng được hỗ trợ

| Board | Giá | Đặc điểm | Phù hợp cho |
|-------|-----|----------|-------------|
| **LicheeRV-Nano** | $9.9 | RISC-V C906 @ 1GHz, 256MB RAM | Trợ lý gia đình tối thiểu |
| **NanoKVM** | $30-50 | RISC-V + KVM qua IP | Bảo trì server tự động |
| **NanoKVM-Pro** | $100 | Version nâng cao | Quản lý datacenter |
| **MaixCAM** | $50 | RISC-V + Camera AI | Giám sát thông minh |
| **MaixCAM2** | $100 | 4K AI Camera | Camera AI thế hệ mới |

### 📥 Cài đặt trên RISC-V

#### **Phương pháp 1: Sử dụng binary đã biên dịch sẵn**

```bash
# 1. Tải xuống binary cho RISC-V từ trang releases
wget https://github.com/sipeed/picoclaw/releases/latest/download/picoclaw_Linux_riscv64.tar.gz

# 2. Giải nén
tar -xzf picoclaw_Linux_riscv64.tar.gz

# 3. Di chuyển vào thư mục binary
sudo mv picoclaw /usr/local/bin/

# 4. Cấp quyền thực thi
sudo chmod +x /usr/local/bin/picoclaw

# 5. Khởi tạo cấu hình
picoclaw onboard
```

#### **Phương pháp 2: Build từ source (cho developer)**

```bash
# 1. Clone repository
git clone https://github.com/sipeed/picoclaw.git
cd picoclaw

# 2. Cài đặt Go 1.21+ trên RISC-V board
# (Hoặc cross-compile từ máy khác)

# 3. Build cho RISC-V
GOOS=linux GOARCH=riscv64 make build

# 4. Binary sẽ ở trong thư mục build/
ls build/picoclaw-linux-riscv64

# 5. Cài đặt
make install
```

#### **Phương pháp 3: Cross-compile từ máy khác**

```bash
# Trên máy phát triển (x86_64/ARM64)
git clone https://github.com/sipeed/picoclaw.git
cd picoclaw

# Build cho RISC-V
GOOS=linux GOARCH=riscv64 go build -ldflags "-s -w" -o picoclaw-riscv64 ./cmd/picoclaw

# Chuyển file sang RISC-V board qua SCP
scp picoclaw-riscv64 root@<risc-v-board-ip>:/usr/local/bin/picoclaw
```

### ⚙️ Cấu hình trên RISC-V

```bash
# 1. Khởi tạo
picoclaw onboard

# 2. Chỉnh sửa config
vi ~/.picoclaw/config.json
```

**Cấu hình tối thiểu cho RISC-V:**

```json
{
  "agents": {
    "defaults": {
      "workspace": "~/.picoclaw/workspace",
      "model": "glm-4.7",
      "max_tokens": 4096,
      "temperature": 0.7,
      "max_tool_iterations": 15,
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

### 🔌 Sử dụng I2C/SPI trên RISC-V

PicoClaw có khả năng điều khiển hardware trực tiếp trên RISC-V boards thông qua I2C và SPI.

#### **Thiết lập I2C trên LicheeRV-Nano**

```bash
# 1. Load module I2C
modprobe i2c-dev

# 2. Kiểm tra bus I2C có sẵn
picoclaw agent -m "i2c detect"

# 3. Quét thiết bị trên bus
picoclaw agent -m "i2c scan bus:1"

# 4. Đọc dữ liệu từ cảm biến (ví dụ: AHT20)
picoclaw agent -m "i2c read bus:1 address:0x38 register:0xAC length:6"
```

#### **Lưu ý về Pinmux**

Trên các board Sipeed, nhiều pin I2C/SPI được chia sẻ với WiFi. Bạn cần:

```bash
# Tắt WiFi nếu sử dụng các pin shared
/etc/init.d/S30wifi stop

# Load i2c-dev module
modprobe i2c-dev

# Cấu hình pinmux (xem board-specific docs)
# Ví dụ cho LicheeRV-Nano:
devmem 0x030010d0 32 0x2
devmem 0x030010d4 32 0x2
```

### 🐳 Chạy với Docker trên RISC-V

```bash
# Clone repo
git clone https://github.com/sipeed/picoclaw.git
cd picoclaw

# Cấu hình
cp config/config.example.json config/config.json
vi config/config.json

# Build Docker image cho RISC-V
docker build -t picoclaw:riscv64 .

# Chạy
docker run -d \
  --name picoclaw \
  -v ~/.picoclaw:/root/.picoclaw \
  picoclaw:riscv64 gateway
```

### 📊 Tối ưu hóa cho RISC-V

#### **Giảm sử dụng RAM**

```json
{
  "agents": {
    "defaults": {
      "max_tokens": 2048,
      "max_tool_iterations": 10
    }
  }
}
```

#### **Sử dụng mô hình nhẹ**

Chọn các mô hình phù hợp với tài nguyên hạn chế:
- **glm-4.7** (Zhipu) - Tốt cho tiếng Trung
- **gemini-1.5-flash** - Nhanh và nhẹ
- **llama-3.1-8b** (Groq) - Free tier

### 🧪 Test trên RISC-V

```bash
# Test cơ bản
picoclaw agent -m "Hello, what can you do?"

# Test I2C (nếu có hardware)
picoclaw agent -m "Scan I2C bus 1 and list all devices"

# Test web search
picoclaw agent -m "Search for latest RISC-V news"

# Test file operations
picoclaw agent -m "Create a test file in workspace"
```

### 📈 Benchmark trên RISC-V

**LicheeRV-Nano (C906 @ 1GHz, 256MB RAM):**
- Khởi động: ~0.8s
- RAM sử dụng: 6-8MB (idle)
- RAM peak: ~15MB (khi xử lý)
- Thời gian phản hồi: 1-3s (tùy thuộc LLM API)

## 📚 Tài liệu tham khảo

### Tài liệu board RISC-V
- [LicheeRV-Nano Wiki](https://wiki.sipeed.com/hardware/en/lichee/RV_Nano/1_intro.html)
- [MaixCAM Documentation](https://wiki.sipeed.com/maixcam)
- [NanoKVM Guide](https://wiki.sipeed.com/nanokvm)

### API Keys
- **LLM**: [OpenRouter](https://openrouter.ai/keys) · [Zhipu](https://open.bigmodel.cn/usercenter/proj-mgmt/apikeys) · [Anthropic](https://console.anthropic.com)
- **Web Search**: [Brave Search](https://brave.com/search/api) (2000 free queries/tháng)
- **Voice**: [Groq](https://console.groq.com) (Whisper transcription miễn phí)

## 🛠️ CLI Commands

| Lệnh | Mô tả |
|------|-------|
| `picoclaw onboard` | Khởi tạo config & workspace |
| `picoclaw agent -m "..."` | Chat với agent |
| `picoclaw agent` | Chế độ chat tương tác |
| `picoclaw gateway` | Khởi động gateway cho chat apps |
| `picoclaw status` | Hiển thị trạng thái |
| `picoclaw cron list` | Liệt kê các tác vụ đã lên lịch |
| `picoclaw cron add ...` | Thêm tác vụ mới |

## 🐛 Xử lý sự cố

### Lỗi "Permission denied" khi truy cập I2C
```bash
# Thêm user vào group i2c
sudo usermod -a -G i2c $USER

# Hoặc chạy với quyền root
sudo picoclaw agent
```

### Không tìm thấy I2C bus
```bash
# Load module
modprobe i2c-dev

# Kiểm tra device tree
ls /dev/i2c-*
```

### WiFi ngừng hoạt động sau khi dùng I2C
```bash
# I2C-1/SPI-2 chia sẻ pins với WiFi SDIO
# Không thể dùng cả hai cùng lúc
# Khởi động lại WiFi:
/etc/init.d/S30wifi start
```

### Out of Memory trên board RAM thấp
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

## 🤝 Đóng góp

PRs được hoan nghênh! Codebase được thiết kế nhỏ gọn và dễ đọc. 🤗

**Developer Group**: Yêu cầu ít nhất 1 PR đã được merge.

**User Groups**:
- Discord: <https://discord.gg/V4sAZ9XWpN>

<img src="assets/wechat.png" alt="PicoClaw WeChat" width="512">

## 📝 License

MIT License - xem [LICENSE](LICENSE) để biết chi tiết.

---

## 🌟 Các ứng dụng triển khai trên RISC-V

### 1. **Trợ lý gia đình thông minh**
- LicheeRV-Nano ($9.9) + Speaker + Microphone
- Điều khiển giọng nói cho smart home
- Kiểm tra thời tiết, tin tức, lịch

### 2. **Giám sát server tự động**
- NanoKVM ($30) trên mỗi server
- Tự động phát hiện và report sự cố
- Thực thi lệnh bảo trì từ xa

### 3. **Camera giám sát AI**
- MaixCAM ($50) với PicoClaw
- Phát hiện chuyển động và cảnh báo
- Nhận diện đối tượng và gửi thông báo

### 4. **IoT Hub**
- PicoClaw làm gateway trung tâm
- Thu thập dữ liệu từ sensors (I2C/SPI)
- Xử lý và phân tích dữ liệu local

---

**Tài liệu này được tạo để giúp cộng đồng Việt Nam dễ dàng triển khai PicoClaw trên RISC-V.**

**Liên hệ & Hỗ trợ**: [GitHub Issues](https://github.com/sipeed/picoclaw/issues)

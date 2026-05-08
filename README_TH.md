# 📖 Gemini CLI - เอกสารเวอร์ชันไทย (Thai Full Documentation)

[![Gemini CLI CI](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml)
[![Gemini CLI E2E (Chained)](https://github.com/google-gemini/gemini-cli/actions/workflows/chained_e2e.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/chained_e2e.yml)
[![Version](https://img.shields.io/npm/v/@google/gemini-cli)](https://www.npmjs.com/package/@google/gemini-cli)
[![License](https://img.shields.io/github/license/google-gemini/gemini-cli)](https://github.com/google-gemini/gemini-cli/blob/main/LICENSE)

## 🇹🇭 เนื้อหา
- [บทนำ](#บทนำ)
- [เหตุใด Gemini CLI](#เหตุใด-gemini-cli)
- [การติดตั้ง](#การติดตั้ง)
  - [Windows PowerShell (แนะนำ)](#-ติดตั้งบน-windows-powershell-sdk-style)
- [ตัวอย่างการใช้งาน](#ตัวอย่างการใช้งาน)
- [เอกสารเพิ่มเติม](#เอกสารเพิ่มเติม)

---

## บทนำ

**Gemini CLI** เป็นตัวแทน AI แบบโอเพนซอร์สที่ออกแบบมาสำหรับนักพัฒนา โดยนำพลังของ Gemini เข้าสู่เทอร์มินัลของคุณโดยตรง

### คุณลักษณะหลัก

| ✨ | รายละเอียด |
|:---:|:---|
| 🎯 | ใช้ได้ฟรี (60 req/min, 1,000 req/day) |
| 🧠 | Gemini 3 Models พร้อมหน้าต่างบริบท 1M tokens |
| 🔧 | เครื่องมือในตัว (Search, File Ops, Shell, Web) |
| 🔌 | MCP Protocol สำหรับการขยาย |
| 💻 | Terminal-first design |
| 🛡️ | Apache 2.0 Licensed |

---

## เหตุใด Gemini CLI?

### 🎯 ระดับฟรี (Free Tier)
- 60 คำขอต่อนาที
- 1,000 คำขอต่อวัน
- ใช้งานได้กับบัญชี Google ส่วนตัว

### 🧠 โมเดล Gemini ที่ทรงพลัง
- Gemini 3 Flash (เร็ว)
- Gemini 3 Pro (แม่นยำ)
- หน้าต่างบริบท 1 ล้านโทเค็น (ไฟล์ขนาดใหญ่)
- การใช้เหตุผลที่ปรับปรุง

### 🔧 เครื่องมือในตัว
- **Google Search Grounding** - ข้อมูลแบบเรียลไทม์
- **File Operations** - อ่าน/เขียนไฟล์
- **Shell Commands** - รันคำสั่ง Terminal
- **Web Fetching** - ดึงเนื้อหาเว็บ

### 🔌 ขยายได้ (Extensible)
- MCP Server Integration
- Custom Commands
- Third-party Tools

---

## 📦 การติดตั้ง

### 📋 ข้อกำหนดระบบ
- **Node.js**: 16.x หรือสูงกว่า
- **npm**: 7.x หรือสูงกว่า
- **OS**: macOS, Linux, Windows

### การติดตั้งด่วน

#### 1️⃣ **npx (ทดลองใช้ทันทีโดยไม่ติดตั้ง)**

```bash
npx @google/gemini-cli
```

✅ **ข้อดี**: ไม่ต้องติดตั้งอะไร ทดลองใช้ได้ทันที
⚠️ **ข้อเสีย**: ช้ากว่าการติดตั้งแบบถาวร

#### 2️⃣ **npm (ติดตั้งเป็นส่วนกลาง)**

```bash
npm install -g @google/gemini-cli
```

✅ **ข้อดี**: เร็ว ใช้ได้ทั่วระบบ
⚠️ **ข้อเสีย**: ต้องติดตั้ง Node.js

#### 3️⃣ **Homebrew (macOS/Linux)**

```bash
brew install gemini-cli
```

#### 4️⃣ **MacPorts (macOS)**

```bash
sudo port install gemini-cli
```

#### 5️⃣ **Anaconda (สภาพแวดล้อมจำกัด)**

```bash
# สร้างสภาพแวดล้อมใหม่
conda create -y -n gemini_env -c conda-forge nodejs

# เปิดใช้งาน
conda activate gemini_env

# ติดตั้ง Gemini CLI
npm install -g @google/gemini-cli
```

---

### ⭐ **ติดตั้งบน Windows PowerShell (SDK Style)**

#### ขั้นตอน 1: ตรวจสอบ Node.js

```powershell
node -v
npm -v
```

ถ้าไม่ติดตั้ง ให้ดาวน์โหลดจาก: https://nodejs.org/

#### ขั้นตอน 2: ติดตั้ง Gemini CLI

```powershell
npm install -g @google/gemini-cli
```

#### ขั้นตอน 3: ตั้งค่า API Key (Permanent Environment Variable)

```powershell
# วิธีที่ 1: ตั้งค่า User Environment Variable (แนะนำ)
[System.Environment]::SetEnvironmentVariable('GEMINI_API_KEY', 'ใส่_API_KEY_ของคุณที่นี่', 'User')

# วิธีที่ 2: ตั้งค่า System Environment Variable (ต้องผู้ดูแลระบบ)
[System.Environment]::SetEnvironmentVariable('GEMINI_API_KEY', 'ใส่_API_KEY_ของคุณที่นี่', 'Machine')
```

#### ขั้นตอน 4: ปิดและเปิด PowerShell ใหม่

```powershell
# ตรวจสอบว่า Environment Variable ตั้งค่าถูกต้อง
$env:GEMINI_API_KEY

# ถ้าเห็นค่า Key แสดงว่าตั้งค่าสำเร็จแล้ว
```

#### ขั้นตอน 5: ทดสอบ

```powershell
gemini
# หรือ
gemini -p "Hello world"
```

#### 🔒 เคล็ดลับความปลอดภัย

| ⚠️ | คำแนะนำ |
|:---:|:---|
| ❌ | ไม่ควร Hardcode Key ในสคริปต์ |
| ✅ | ใช้ Environment Variables |
| ✅ | ใช้ `.gitignore` สำหรับไฟล์เสริม |
| ✅ | หมุนเวียน Key เป็นระยะ |

---

## 🚀 ตัวอย่างการใช้งาน

### 🎯 การใช้งานพื้นฐาน

#### เริ่มต้นในไดเรกทอรีปัจจุบัน

```bash
gemini
# เมนูโต้ตอบจะปรากฏขึ้น
```

#### ส่ง Query ทันทีผ่าน CLI

```bash
# คำถามง่าย
gemini -p "Explain this function"

# JSON Output (สำหรับสคริปต์)
gemini -p "List all files" --output-format json

# Real-time Streaming
gemini -p "Deploy and test" --output-format stream-json
```

#### เลือกโมเดล

```bash
# Gemini 3 Flash (เร็ว)
gemini -m gemini-3-flash

# Gemini 3 Pro (แม่นยำ)
gemini -m gemini-3-pro
```

#### รวมหลายไดเรกทอรี

```bash
gemini --include-directories ../lib,../docs
```

### 🎓 ตัวอย่างเรียนรู้

#### ตัวอย่าง 1: สร้างบอท Discord

```bash
cd my-project/
gemini
> Create a Discord bot that answers FAQ questions from FAQ.md file
```

#### ตัวอย่าง 2: วิเคราะห์โค้ด

```bash
git clone https://github.com/google-gemini/gemini-cli
cd gemini-cli
gemini
> Summarize the changes made yesterday
```

#### ตัวอย่าง 3: Debugging

```bash
# วางไฟล์ที่มีข้อผิดพลาด
gemini
> Fix this error: [paste error message]
> Show me how to debug this
```

---

## 🔐 การตรวจสอบสิทธิ์ (Authentication)

### ตัวเลือก 1: Google OAuth (แนะนำสำหรับผู้ใช้ส่วนตัว)

```bash
gemini
# เลือก "Sign in with Google"
# เบราว์เซอร์จะเปิดขึ้น ลงชื่อเข้าใช้ Google
```

**ข้อดี:**
- ฟรีสูงสุด 60 req/min, 1,000 req/day
- ไม่ต้องสร้าง API Key
- อัปเดตโมเดลอัตโนมัติ

### ตัวเลือก 2: API Key (สำหรับการควบคุมโมเดล)

1. ไปที่ https://aistudio.google.com/apikey
2. คลิก "Get API Key"
3. ตั้งค่า Environment Variable:

```bash
# macOS/Linux
export GEMINI_API_KEY="YOUR_API_KEY"
gemini

# Windows PowerShell
[System.Environment]::SetEnvironmentVariable('GEMINI_API_KEY', 'YOUR_API_KEY', 'User')
gemini
```

### ตัวเลือก 3: Vertex AI (สำหรับองค์กร)

```bash
export GOOGLE_API_KEY="YOUR_API_KEY"
export GOOGLE_GENAI_USE_VERTEXAI=true
export GOOGLE_CLOUD_PROJECT="your-project-id"
gemini
```

---

## 📚 คำสั่ง (Commands)

### คำสั่ง Slash

```bash
/help              # ดูคำสั่งทั้งหมด
/chat <message>    # ส่งข้อความ
/code              # ลง Code Mode
/search <query>    # ค้นหาด้วย Google
/files             # ดูไฟล์ที่โหลด
/exit              # ออก
```

### Flag ที่สำคัญ

```bash
-p, --prompt       # ส่ง Prompt โดยตรง
-m, --model        # เลือกโมเดล
--output-format    # json / stream-json / text
```

---

## 🔧 การตั้งค่า (Configuration)

### ไฟล์ Config หลัก

ตั้งค่าใน `~/.gemini/settings.json`:

```json
{
  "model": "gemini-3-flash",
  "temperature": 0.7,
  "maxTokens": 2048,
  "enableSearch": true
}
```

### Context File (GEMINI.md)

สร้างไฟล์ `GEMINI.md` ในโครงการเพื่อให้บริบท:

```markdown
# Project Context

This is a Node.js project for a Discord bot.
- Framework: discord.js
- Database: MongoDB
- Node version: 16.x

## Important Notes
- Use async/await instead of callbacks
- Follow ES6+ standards
```

---

## 🛠️ MCP Server Integration

ใช้ MCP (Model Context Protocol) เพื่อขยาย Gemini CLI:

### ตั้งค่า MCP Server

```bash
# ที่ ~/.gemini/settings.json
{
  "mcpServers": [
    {
      "name": "github",
      "command": "node",
      "args": ["path/to/github-mcp.js"]
    }
  ]
}
```

### ใช้ MCP Server

```bash
gemini
> @github List my open pull requests
> @slack Send a message to #dev
> @database Query active users
```

---

## ⚡ Performance Tips

### 🚀 ปรับปรุงความเร็ว

```bash
# ใช้ Flash Model (เร็วกว่า)
gemini -m gemini-3-flash

# ลดจำนวน Token
gemini -p "Summarize: ..." --max-tokens 500

# ใช้ Streaming
gemini -p "Generate code" --output-format stream-json
```

### 💾 ประหยัด Token

- ใช้โปรเจกต์เล็ก ๆ
- ใช้ Context File ที่เหมาะสม
- ปิดใช้ Google Search ถ้าไม่จำเป็น

---

## 🐛 Troubleshooting

### ปัญหา: "Command not found: gemini"

**สาเหตุ:** npm global path ไม่อยู่ใน PATH

```bash
# ตรวจสอบ npm global path
npm config get prefix

# เพิ่มเข้า PATH (Linux/macOS)
export PATH="$PATH:$(npm config get prefix)/bin"

# Windows PowerShell
$env:Path += ";$(npm config get prefix)\bin"
```

### ปัญหา: "API Key not found"

```bash
# ตรวจสอบ Environment Variable
echo $GEMINI_API_KEY  # Linux/macOS
$env:GEMINI_API_KEY   # Windows PowerShell

# ตั้งค่าใหม่
export GEMINI_API_KEY="YOUR_KEY"
```

### ปัญหา: "Node.js version not compatible"

```bash
# ตรวจสอบเวอร์ชัน
node -v
npm -v

# อัปเกรด Node.js จาก nodejs.org
```

---

## 📞 ความช่วยเหลือและการสนับสนุน

| 📧 | ช่องทาง |
|:---:|:---|
| 🐛 | [Report Issue](https://github.com/nongsandyza/gemini-cli/issues) |
| 💬 | [GitHub Discussions](https://github.com/google-gemini/gemini-cli/discussions) |
| 📖 | [Official Docs](https://geminicli.com/docs/) |
| 🎓 | [Free Course](https://learn.deeplearning.ai/courses/gemini-cli) |

---

## 📄 License & Legal

- **License**: [Apache License 2.0](./LICENSE)
- **Terms**: [Terms & Privacy](https://www.geminicli.com/docs/resources/tos-privacy)
- **Security**: [Security Policy](./SECURITY.md)

---

## 🎯 สรุป

| ✅ | ทำได้ทันที |
|:---:|:---|
| 📲 | ติดตั้ง 1 บรรทัด (npm install -g) |
| 🔑 | ตั้งค่า API Key ครั้งเดียว |
| 🚀 | เริ่มใช้งานได้เลย |
| 🆓 | ใช้ฟรี 1,000 req/day |

---

<p align="center">
  สร้างด้วย ❤️ โดย Google และชุมชนโอเพนซอร์ส
  <br/>
  <a href="https://github.com/nongsandyza/gemini-cli">GitHub Repository</a>
</p>

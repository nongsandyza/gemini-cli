# Gemini CLI — README (ภาษาไทย)

[![Gemini CLI CI](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml)
[![Gemini CLI E2E (Chained)](https://github.com/google-gemini/gemini-cli/actions/workflows/chained_e2e.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/chained_e2e.yml)
[![Version](https://img.shields.io/npm/v/@google/gemini-cli)](https://www.npmjs.com/package/@google/gemini-cli)
[![License](https://img.shields.io/github/license/google-gemini/gemini-cli)](https://github.com/google-gemini/gemini-cli/blob/main/LICENSE)

![Gemini CLI Screenshot](/docs/assets/gemini-screenshot.png)

Gemini CLI เป็นตัวแทน AI แบบโอเพนซอร์สที่นำพลังของ Gemini เข้าสู่เทอร์มินัลของคุณโดยตรง มันมอบการเข้าถึง Gemini ที่เบาและให้เส้นทางที่ตรงที่สุดจากพร้อมท์ของคุณไปยังแบบจำลอง

เรียนรู้เพิ่มเติมเกี่ยวกับ Gemini CLI ได้ที่: https://geminicli.com/docs/

## 🚀 เหตุใด Gemini CLI?

- **🎯 ระดับฟรี**: 60 คำขอ/นาที และ 1,000 คำขอ/วัน (บัญชี Google ส่วนบุคคล)
- **🧠 โมเดล Gemini 3**: รองรับการ reasoning ที่ดีขึ้นและบริบทขนาด 1M โทเค็น
- **🔧 เครื่องมือในตัว**: Google Search grounding, file operations, shell commands, web fetching
- **🔌 ขยายได้**: สนับสนุน MCP (Model Context Protocol) สำหรับการรวมกำหนดเอง
- **💻 เน้นเทอร์มินัล**: ออกแบบมาสำหรับนักพัฒนาที่ทำงานบน CLI
- **🛡️ โอเพนซอร์ส**: ภายใต้ใบอนุญาต Apache 2.0

## 📦 การติดตั้ง

ดูคำแนะนำฉบับสมบูรณ์: https://www.geminicli.com/docs/get-started/installation

### ติดตั้งแบบด่วน (Quick Install)

รันทันทีด้วย npx:

```bash
npx @google/gemini-cli
```

ติดตั้งแบบ global ด้วย npm:

```bash
npm install -g @google/gemini-cli
```

ติดตั้งด้วย Homebrew (macOS/Linux):

```bash
brew install gemini-cli
```

ติดตั้งด้วย MacPorts (macOS):

```bash
sudo port install gemini-cli
```

ติดตั้งด้วย Anaconda (สำหรับสภาพแวดล้อมที่จำกัด):

```bash
conda create -y -n gemini_env -c conda-forge nodejs
conda activate gemini_env
npm install -g @google/gemini-cli
```

## 📋 คุณสมบัติหลัก

### การเข้าใจและการสร้างโค้ด

- สอบถามและแก้ไขฐานโค้ดขนาดใหญ่
- สร้างแอปจาก PDF, รูปภาพ หรือสเก็ตช์ด้วยความสามารถมัลติโมดัล
- ดีบักและแก้ไขปัญหาโดยใช้ภาษาธรรมชาติ

### อัตโนมัติและการรวมระบบ

- อัตโนมัติงานปฏิบัติการ เช่น ตรวจสอบ Pull Requests หรือจัดการการรีเบสที่ซับซ้อน
- ใช้ MCP servers เพื่อเชื่อมต่อความสามารถใหม่ๆ เช่น media generation
- รันแบบไม่โต้ตอบสำหรับสคริปต์และเวิร์กโฟลว์

### ความสามารถขั้นสูง

- ใช้ Google Search ในตัวสำหรับ grounding ข้อมูลเรียลไทม์
- บันทึกและกู้คืนการสนทนา (checkpointing)
- ไฟล์บริบทแบบกำหนดเอง (GEMINI.md)

### การรวมกับ GitHub

รวม Gemini CLI เข้ากับเวิร์กโฟลว์ GitHub ด้วย Gemini CLI GitHub Action เพื่อช่วยในงาน เช่น การตรวจสอบ PR อัตโนมัติ การติดป้ายปัญหา และการช่วยเหลือตามความต้องการ

## 🔐 ตัวเลือกการยืนยันตัวตน

เลือกวิธีการที่เหมาะสมกับความต้องการของคุณ:

### ตัวเลือก 1: ลงชื่อเข้าใช้ด้วย Google (OAuth)

**เหมาะสำหรับ:** นักพัฒนารายบุคคลและผู้ที่มี Gemini Code Assist License

```bash
# เริ่ม Gemini CLI แล้วเลือก 'Sign in with Google'
gemini
```

หากใช้สิทธิ์ที่ชำระ ต้องตั้งค่า Google Cloud Project:

```bash
export GOOGLE_CLOUD_PROJECT="YOUR_PROJECT_ID"
gemini
```

### ตัวเลือก 2: Gemini API Key

**เหมาะสำหรับ:** นักพัฒนาที่ต้องการควบคุมโมเดลหรือการเข้าถึงแบบชำระเงิน

```bash
# ขอคีย์จาก https://aistudio.google.com/apikey
export GEMINI_API_KEY="YOUR_API_KEY"
gemini
```

### ตัวเลือก 3: Vertex AI

**เหมาะสำหรับ:** ทีมองค์กรและงาน production

```bash
export GOOGLE_API_KEY="YOUR_API_KEY"
export GOOGLE_GENAI_USE_VERTEXAI=true
gemini
```

## 🚀 เริ่มต้นใช้งาน

เริ่มในไดเรกทอรีปัจจุบัน:

```bash
gemini
```

รวมหลายไดเรกทอรี:

```bash
gemini --include-directories ../lib,../docs
```

ใช้โมเดลเฉพาะ:

```bash
gemini -m gemini-2.5-flash
```

โหมดไม่โต้ตอบ (สำหรับสคริปต์):

```bash
gemini -p "Explain the architecture of this codebase"
```

สำหรับเอาต์พุตแบบมีโครงสร้าง:

```bash
gemini -p "Explain the architecture of this codebase" --output-format json
```

สำหรับการสตรีมเหตุการณ์แบบเรียลไทม์:

```bash
gemini -p "Run tests and deploy" --output-format stream-json
```

## 🤝 การมีส่วนร่วม

ยินดีรับการมีส่วนร่วมจากชุมชน: รายงานบั๊ก ปรับปรุงเอกสาร ส่งโค้ด และแบ่งปันส่วนขยาย MCP

ดู CONTRIBUTING.md สำหรับแนวทางการพัฒนาและการส่ง PR

---

<p align="center">สร้างด้วย ❤️ โดย Google และชุมชนโอเพนซอร์ส</p>

# Gemini CLI

[![Gemini CLI CI](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml)
[![Gemini CLI E2E (Chained)](https://github.com/google-gemini/gemini-cli/actions/workflows/chained_e2e.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/chained_e2e.yml)
[![Version](https://img.shields.io/npm/v/@google/gemini-cli)](https://www.npmjs.com/package/@google/gemini-cli)
[![License](https://img.shields.io/github/license/google-gemini/gemini-cli)](https://github.com/google-gemini/gemini-cli/blob/main/LICENSE)
[![View Code Wiki](https://assets.codewiki.google/readme-badge/static.svg)](https://codewiki.google/github.com/google-gemini/gemini-cli?utm_source=badge&utm_medium=github&utm_campaign=github.com/google-gemini/gemini-cli)

![Gemini CLI Screenshot](/docs/assets/gemini-screenshot.png)

Gemini CLI เป็นตัวแทน AI แบบโอเพนซอร์สที่นำพลังของ Gemini เข้าสู่เทอร์มินัลของคุณโดยตรง มันมอบการเข้าถึง Gemini ที่เบาน้อยและให้เส้นทางที่ตรงที่สุดจากพร้อมท์ของคุณไปยังแบบจำลองของเรา

เรียนรู้เพิ่มเติมเกี่ยวกับ Gemini CLI ในเอกสารของเรา: [documentation](https://geminicli.com/docs/)

## 🚀 เหตุใด Gemini CLI?

- **🎯 ระดับฟรี**: 60 คำขอ/นาที และ 1,000 คำขอ/วัน พร้อมบัญชี Google ส่วนตัว
- **🧠 โมเดล Gemini 3 ที่มีพลังมาก**: เข้าถึงการใช้เหตุผลที่ปรับปรุงและหน้าต่างบริบท 1 ล้านโทเค็น
- **🔧 เครื่องมือในตัว**: Google Search grounding, file operations, shell commands, web fetching
- **🔌 ขยายได้**: สนับสนุน MCP (Model Context Protocol) สำหรับการรวมกำหนดเองที่กำหนดเอง
- **💻 ใจกลางเทอร์มินัล**: ออกแบบมาสำหรับนักพัฒนาที่สดใสที่บรรทัดคำสั่ง
- **🛡️ โอเพนซอร์ส**: ได้รับใบอนุญาต Apache 2.0

## 📦 การติดตั้ง

ดู
[Gemini CLI installation, execution, and releases](https://www.geminicli.com/docs/get-started/installation)
สำหรับข้อกำหนดระบบที่แนะนำและคำแนะนำการติดตั้งโดยละเอียด

### การติดตั้งด่วน

#### รัน npx ทันทีโดยไม่ต้องติดตั้ง

```bash
# Using npx (no installation required)
npx @google/gemini-cli
```

#### ติดตั้งเป็นส่วนกลางด้วย npm

```bash
npm install -g @google/gemini-cli
```

#### ติดตั้งเป็นส่วนกลางด้วย Homebrew (macOS/Linux)

```bash
brew install gemini-cli
```

#### ติดตั้งเป็นส่วนกลางด้วย MacPorts (macOS)

```bash
sudo port install gemini-cli
```

#### ติดตั้งด้วย Anaconda (สำหรับสภาพแวดล้อมที่จำกัด)

```bash
# Create and activate a new environment
conda create -y -n gemini_env -c conda-forge nodejs
conda activate gemini_env

# Install Gemini CLI globally via npm (inside the environment)
npm install -g @google/gemini-cli
```

## ช่องทางการเปิดตัว

ดู [Releases](https://www.geminicli.com/docs/changelogs) สำหรับรายละเอียดเพิ่มเติม

### Preview

รिลีส preview ใหม่จะเผยแพร่แต่ละสัปดาห์เวลา 23:59 UTC ในวันอังคาร รีลีสเหล่านี้จะไม่ได้รับการตรวจสอบอย่างครบถ้วน และอาจมีการถดถอยหรือปัญหาอื่นๆ ที่ยังคงเหลืออยู่ โปรดช่วยเราทดสอบและติดตั้งด้วยแท็ก `preview`

```bash
npm install -g @google/gemini-cli@preview
```

### Stable

- รีลีส stable ใหม่จะเผยแพร่แต่ละสัปดาห์เวลา 20:00 UTC ในวันอังคาร นี่จะเป็นการส่งเสริมเต็มรูปแบบของรีลีส `preview` ของสัปดาห์ที่แล้ว + การแก้ไขข้อบกพร่องและการตรวจสอบ ใช้แท็ก `latest`

```bash
npm install -g @google/gemini-cli@latest
```

### Nightly

- รีลีสใหม่จะเผยแพร่ทุกวันเวลา 00:00 UTC นี่จะเป็นการเปลี่ยนแปลงทั้งหมดจากสาขา main ตามที่แสดงในเวลารีลีส ควรสันนิษฐานว่ามีการตรวจสอบที่ค้างและปัญหา ใช้แท็ก `nightly`

```bash
npm install -g @google/gemini-cli@nightly
```

## 📋 คุณสมบัติหลัก

### การเข้าใจ & การสร้างโค้ด

- Query and edit large codebases
- Generate new apps from PDFs, images, or sketches using multimodal capabilities
- Debug issues and troubleshoot with natural language

### Automation & Integration

- Automate operational tasks like querying pull requests or handling complex
  rebases
- Use MCP servers to connect new capabilities, including
  [media generation with Imagen, Veo or Lyria](https://github.com/GoogleCloudPlatform/vertex-ai-creative-studio/tree/main/experiments/mcp-genmedia)
- Run non-interactively in scripts for workflow automation

## 🔐 Authentication Options

Choose the authentication method that best fits your needs:

### Option 1: Sign in with Google (OAuth login using your Google Account)

**✨ Best for:** Individual developers as well as anyone who has a Gemini Code
Assist License. (see [quota limits and terms of service](https://cloud.google.com/gemini/docs/quotas) for details)

**Benefits:**

- **Free tier**: 60 requests/min and 1,000 requests/day
- **Gemini 3 models** with 1M token context window
- **No API key management** - just sign in with your Google account
- **Automatic updates** to latest models

#### Start Gemini CLI, then choose _Sign in with Google_ and follow the browser authentication flow when prompted

```bash
gemini
```

#### If you are using a paid Code Assist License from your organization, remember to set the Google Cloud Project

```bash
# Set your Google Cloud Project
export GOOGLE_CLOUD_PROJECT="YOUR_PROJECT_ID"
gemini
```

### Option 2: Gemini API Key

**✨ Best for:** Developers who need specific model control or paid tier access

**Benefits:**

- **Free tier**: 1000 requests/day with Gemini 3 (mix of flash and pro)
- **Model selection**: Choose specific Gemini models
- **Usage-based billing**: Upgrade for higher limits when needed

```bash
# Get your key from https://aistudio.google.com/apikey
export GEMINI_API_KEY="YOUR_API_KEY"
gemini
```

### Option 3: Vertex AI

**✨ Best for:** Enterprise teams and production workloads

**Benefits:**

- **Enterprise features**: Advanced security and compliance
- **Scalable**: Higher rate limits with billing account
- **Integration**: Works with existing Google Cloud infrastructure

```bash
# Get your key from Google Cloud Console
export GOOGLE_API_KEY="YOUR_API_KEY"
export GOOGLE_GENAI_USE_VERTEXAI=true
gemini
```

For Google Workspace accounts and other authentication methods, see the
[authentication guide](https://www.geminicli.com/docs/get-started/authentication).

## 🚀 Getting Started

### Basic Usage

#### Start in current directory

```bash
gemini
```

#### Include multiple directories

```bash
gemini --include-directories ../lib,../docs
```

#### Use specific model

```bash
gemini -m gemini-2.5-flash
```

#### Non-interactive mode for scripts

Get a simple text response:

```bash
gemini -p "Explain the architecture of this codebase"
```

For more advanced scripting, including how to parse JSON and handle errors, use
the `--output-format json` flag to get structured output:

```bash
gemini -p "Explain the architecture of this codebase" --output-format json
```

For real-time event streaming (useful for monitoring long-running operations),
use `--output-format stream-json` to get newline-delimited JSON events:

```bash
gemini -p "Run tests and deploy" --output-format stream-json
```

---

<p align="center">
  Built with ❤️ by Google and the open source community
</p>

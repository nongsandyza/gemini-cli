# Gemini CLI

[![Gemini CLI CI](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml)
[![Gemini CLI E2E (Chained)](https://github.com/google-gemini/gemini-cli/actions/workflows/chained_e2e.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/chained_e2e.yml)
[![Version](https://img.shields.io/npm/v/@google/gemini-cli)](https://www.npmjs.com/package/@google/gemini-cli)
[![License](https://img.shields.io/github/license/google-gemini/gemini-cli)](https://github.com/google-gemini/gemini-cli/blob/main/LICENSE)
[![View Code Wiki](https://assets.codewiki.google/readme-badge/static.svg)](https://codewiki.google/github.com/google-gemini/gemini-cli?utm_source=badge&utm_medium=github&utm_campaign=github.com/google-gemini/gemini-cli)

![Gemini CLI Screenshot](/docs/assets/gemini-screenshot.png)

Gemini CLI เป็นตัวแทน AI แบบโอเพนซอร์สที่นำพลังของ Gemini เข้าสู่เทอร์มินัลของคุณโดยตรง มันมอบการเข้าถึง Gemini ที่เบาน้อยและให้เส้นทางที่ตรงที่สุดจากพร้อมท์ของคุณไปยังแบบจำลองของเรา

เรียนรู้เพิ่มเติมเกี่ยวกับ Gemini CLI ในเอกสารของเรา: [documentation](https://geminicli.com/docs/)

> 📌 **สำหรับนักพัฒนาไทย**: ดูเอกสารเวอร์ชันไทยแบบเต็มที่ [README_TH.md](./README_TH.md)

## 🚀 เหตุใด Gemini CLI?

- **🎯 ระดับฟรี**: 60 คำขอ/นาที และ 1,000 คำขอ/วัน พร้อมบัญชี Google ส่วนตัว
- **🧠 โมเดล Gemini 3 ที่มีพลังมาก**: เข้าถึงการใช้เหตุผลที่ปรับปรุงและหน้าต่างบริบท 1 ล้านโทเค็น
- **🔧 เครื่องมือในตัว**: Google Search grounding, file operations, shell commands, web fetching
- **🔌 ขยายได้**: สนับสนุน MCP (Model Context Protocol) สำหรับการรวมกำหนดเองที่กำหนดเอง
- **💻 ใจกลางเทอร์มินัล**: ออกแบบมาสำหรับนักพัฒนาที่สดใสที่บรรทัดคำสั่ง
- **🛡️ โอเพนซอร์ส**: ได้รับใบอนุญาต Apache 2.0

## 📦 การติดตั้ง

ดู [Gemini CLI installation, execution, and releases](https://www.geminicli.com/docs/get-started/installation) สำหรับข้อกำหนดระบบที่แนะนำและคำแนะนำการติดตั้งโดยละเอียด

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

#### ⭐ **ติดตั้งบน Windows PowerShell (SDK Style)**

สำหรับผู้ใช้ Windows ที่ต้องการการตั้งค่า Permanent:

```powershell
# ขั้นตอน 1: ตรวจสอบ Node.js ด้วยคำสั่ง
node -v

# ขั้นตอน 2: ติดตั้ง Gemini CLI เป็นส่วนกลาง
npm install -g @google/gemini-cli

# ขั้นตอน 3: ตั้งค่า API Key เพื่อใช้ตลอดไป (Permanent)
[System.Environment]::SetEnvironmentVariable('GEMINI_API_KEY', 'ใส่_KEY_ของคุณ_ที่นี่', 'User')

# ขั้นตอน 4: ปิดและเปิด PowerShell ใหม่ แล้วทดสอบ
gemini
```

> 💡 **เคล็ดลับสำคัญ**: หลังจากตั้งค่า Environment Variable คุณต้อง **ปิดและเปิด PowerShell ใหม่** เพื่อให้การเปลี่ยนแปลงมีผล

> 🔒 **ความปลอดภัย**: Environment Variable นี้จะบันทึกที่ระบบของคุณ ไม่จำเป็นต้องใส่ Key ทีละครั้ง

## ช่องทางการเปิดตัว

ดู [Releases](https://www.geminicli.com/docs/changelogs) สำหรับรายละเอียดเพิ่มเติม

### Preview

รีลีส preview ใหม่จะเผยแพร่ทุกสัปดาห์เวลา 23:59 UTC ในวันอังคาร ริลีสเหล่านี้จะไม่ได้รับการตรวจสอบอย่างครบถ้วน และอาจมีการถดถอยหรือปัญหาอื่นๆ ที่ยังคงเหลืออยู่ โปรดช่วยเราทดสอบและติดตั้งด้วยแท็ก `preview`

```bash
npm install -g @google/gemini-cli@preview
```

### Stable

- รีลีส stable ใหม่จะเผยแพร่ทุกสัปดาห์เวลา 20:00 UTC ในวันอังคาร นี่จะเป็นการส่งเสริมเต็มรูปแบบของรีลีส `preview` ของสัปดาห์ที่แล้ว + การแก้ไขบัญหาและการตรวจสอบใดๆ ใช้แท็ก `latest`

```bash
npm install -g @google/gemini-cli@latest
```

### Nightly

- รีลีสใหม่จะเผยแพร่ทุกวันเวลา 00:00 UTC นี่จะเป็นการเปลี่ยนแปลงทั้งหมดจากสาขา main ตามที่แสดงในเวลารีลีส ควรสันนิษฐานว่ามีการตรวจสอบที่ค้างและปัญหา ใช้แท็ก `nightly`

```bash
npm install -g @google/gemini-cli@nightly
```

## 📋 คุณสมบัติหลัก

### การเข้าใจและการสร้างโค้ด

- ข้อมูลแบบสอบถามและแก้ไขฐานโค้ดขนาดใหญ่
- สร้างแอปใหม่จากไฟล์ PDF, รูปภาพหรือร่างโดยใช้ความสามารถมัลติโมดัล
- ปีแง้วปัญหาและแก้ไขปัญหากับภาษาธรรมชาติ

### สารบัญอัตโนมัติและการรวมข้อมูล

- อัตโนมัติงานปฏิบัติการเช่นข้อมูลแบบสอบถามคำขอดึงข้อมูลหรือการปรับปรุงพื้นฐาน
- ใช้เซิร์ฟเวอร์ MCP เพื่อเชื่อมต่อความสามารถใหม่ รวมถึง [media generation with Imagen, Veo or Lyria](https://github.com/GoogleCloudPlatform/vertex-ai-creative-studio/tree/main/experiments/mcp-genmedia)
- รันแบบไม่ใช้งานแบบอิสระในสคริปต์เพื่อสารบัญอัตโนมัติเวิร์กโฟลว์

### ความสามารถขั้นสูง

- จากกราวด์ข้อมูลแบบสอบถามของคุณด้วยการค้นหา Google ในตัว [Google Search](https://ai.google.dev/gemini-api/docs/grounding) สำหรับข้อมูลแบบเรียลไทม์
- การสนทนาบันทึกเพื่อบันทึกและดำเนินการเซ็นชั่นที่ซับซ้อน
- ไฟล์บริบทที่กำหนดเองมนต์ (GEMINI.md) เพื่อปรับแต่งพฤติกรรมสำหรับโครงการของคุณ

### การรวม GitHub

รวม Gemini CLI โดยตรงเข้าในเวิร์กโฟลว์ GitHub ของคุณด้วย [**Gemini CLI GitHub Action**](https://github.com/google-github-actions/run-gemini-cli):

- **ตรวจสอบคำขอดึงข้อมูล**: ตรวจสอบโค้ดอัตโนมัติพร้อมฟีดแบ็กแบบบริบทและข้อเสนอแนะ
- **การจัดหมวดหมู่ปัญหา**: การติดป้ายกำกับอัตโนมัติและการจัดลำดับความสำคัญของปัญหา GitHub ตามการวิเคราะห์เนื้อหา
- **ความช่วยเหลือตามความต้องการ**: กล่าว `@gemini-cli` ในปัญหาและคำขอดึงข้อมูลเพื่อขอความช่วยเหลือด้านการดีบัก คำอธิบาย หรือการมอบหมายงาน
- **เวิร์กโฟลว์ที่กำหนดเอง**: สร้างเวิร์กโฟลว์อัตโนมัติตามกำหนดการและตามความต้องการที่ปรับแต่งให้เหมาะกับความต้องการของทีมของคุณ

## 🔐 ตัวเลือกการตรวจสอบสิทธิ์

เลือกวิธีการตรวจสอบสิทธิ์ที่เหมาะสมที่สุดกับความต้องการของคุณ:

### ตัวเลือก 1: ลงชื่อเข้าใช้ด้วย Google (OAuth login using your Google Account)

**✨ เหมาะที่สุดสำหรับ:** นักพัฒนารายบุคคลและใครก็ตามที่มีใบอนุญาต Gemini Code Assist (ดู [quota limits and terms of service](https://cloud.google.com/gemini/docs/quotas) สำหรับรายละเอียด)

**ประโยชน์:**

- **ระดับฟรี**: 60 คำขอ/นาที และ 1,000 คำขอ/วัน
- **โมเดล Gemini 3** พร้อมหน้าต่างบริบท 1 ล้านโทเค็น
- **ไม่มีการจัดการคีย์ API** - เพียงลงชื่อเข้าใช้ด้วยบัญชี Google ของคุณ
- **การอัปเดตอัตโนมัติ** ไปยังโมเดลล่าสุด

#### เริ่ม Gemini CLI จากนั้นเลือก _Sign in with Google_ และทำตามขั้นตอนการตรวจสอบสิทธิ์เบราว์เซอร์เมื่อมีการแจ้ง

```bash
gemini
```

#### หากคุณใช้ใบอนุญาต Code Assist ที่ชำระเงินจากองค์กรของคุณ โปรดจำไว้ว่าต้องตั้งค่าโครงการ Google Cloud

```bash
# Set your Google Cloud Project
export GOOGLE_CLOUD_PROJECT="YOUR_PROJECT_ID"
gemini
```

### ตัวเลือก 2: Gemini API Key

**✨ เหมาะที่สุดสำหรับ:** นักพัฒนาที่ต้องการควบคุมโมเดลเฉพาะหรือการเข้าถึงระดับ paid

**ประโยชน์:**

- **ระดับฟรี**: 1000 คำขอ/วัน ด้วย Gemini 3 (ส่วนผสมของ flash และ pro)
- **ตัวเลือกโมเดล**: เลือกโมเดล Gemini เฉพาะ
- **บิลโดยใช้เท่าที่คุณใช้**: อัปเกรดเพื่อขีดจำกัดที่สูงขึ้นตามต้องการ

```bash
# Get your key from https://aistudio.google.com/apikey
export GEMINI_API_KEY="YOUR_API_KEY"
gemini
```

### ตัวเลือก 3: Vertex AI

**✨ เหมาะที่สุดสำหรับ:** ทีมองค์กรและโครงการการผลิต

**ประโยชน์:**

- **คุณสมบัติองค์กร**: ความปลอดภัยและการปฏิบัติตามข้อบังคับขั้นสูง
- **ปรับขนาดได้**: ขีดจำกัดอัตรากว่างที่สูงขึ้นพร้อมบัญชีการเรียกเก็บเงิน
- **การรวม**: ทำงานกับโครงสร้างพื้นฐาน Google Cloud ที่มีอยู่

```bash
# Get your key from Google Cloud Console
export GOOGLE_API_KEY="YOUR_API_KEY"
export GOOGLE_GENAI_USE_VERTEXAI=true
gemini
```

สำหรับบัญชี Google Workspace และวิธีการตรวจสอบสิทธิ์อื่นๆ โปรดดู [authentication guide](https://www.geminicli.com/docs/get-started/authentication)

## 🚀 เริ่มต้นใช้งาน

### การใช้งานพื้นฐาน

#### เริ่มในไดเรกทอรีปัจจุบัน

```bash
gemini
```

#### รวมหลายไดเรกทอรี

```bash
gemini --include-directories ../lib,../docs
```

#### ใช้โมเดลเฉพาะ

```bash
gemini -m gemini-2.5-flash
```

#### โหมดไม่ใช้งานแบบอิสระสำหรับสคริปต์

รับการตอบกลับข้อความง่ายๆ:

```bash
gemini -p "Explain the architecture of this codebase"
```

สำหรับการสคริปต์ขั้นสูง รวมถึงวิธีการแยกวิเคราะห์ JSON และจัดการข้อผิดพลาด ให้ใช้ `--output-format json` ธง เพื่อรับเอาต์พุตที่มีโครงสร้าง:

```bash
gemini -p "Explain the architecture of this codebase" --output-format json
```

สำหรับการสตรีมเหตุการณ์แบบเรียลไทม์ (มีประโยชน์สำหรับการตรวจสอบการดำเนินการที่ยาวนาน) ให้ใช้ `--output-format stream-json` เพื่อรับเหตุการณ์ JSON ที่คั่นด้วยบรรทัดใหม่:

```bash
gemini -p "Run tests and deploy" --output-format stream-json
```

### ตัวอย่างด่วน

#### เริ่มต้นโครงการใหม่

```bash
cd new-project/
gemini
> Write me a Discord bot that answers questions using a FAQ.md file I will provide
```

#### วิเคราะห์โค้ดที่มีอยู่

```bash
git clone https://github.com/google-gemini/gemini-cli
cd gemini-cli
gemini
> Give me a summary of all of the changes that went in yesterday
```

## 📚 เอกสาร

### เริ่มต้นใช้งาน

- [**Quickstart Guide**](https://www.geminicli.com/docs/get-started) - เริ่มต้นอย่างรวดเร็ว
- [**Authentication Setup**](https://www.geminicli.com/docs/get-started/authentication) - การกำหนดค่าการตรวจสอบสิทธิ์โดยละเอียด
- [**Configuration Guide**](https://www.geminicli.com/docs/reference/configuration) - การตั้งค่าและการปรับแต่ง
- [**Keyboard Shortcuts**](https://www.geminicli.com/docs/reference/keyboard-shortcuts) - เคล็ดลับการผลิต

### คุณสมบัติหลัก

- [**Commands Reference**](https://www.geminicli.com/docs/reference/commands) - คำสั่ง slash ทั้งหมด (`/help`, `/chat`, ฯลฯ)
- [**Custom Commands**](https://www.geminicli.com/docs/cli/custom-commands) - สร้างคำสั่งที่ใช้ซ้ำได้ของคุณเอง
- [**Context Files (GEMINI.md)**](https://www.geminicli.com/docs/cli/gemini-md) - ให้บริบทที่ยั่งยืนกับ Gemini CLI
- [**Checkpointing**](https://www.geminicli.com/docs/cli/checkpointing) - บันทึกและสร้างความเห็นอีกครั้ง
- [**Token Caching**](https://www.geminicli.com/docs/cli/token-caching) - ปรับปรุงการใช้โทเค็น

### เครื่องมือและส่วนขยาย

- [**Built-in Tools Overview**](https://www.geminicli.com/docs/reference/tools)
  - [File System Operations](https://www.geminicli.com/docs/tools/file-system)
  - [Shell Commands](https://www.geminicli.com/docs/tools/shell)
  - [Web Fetch & Search](https://www.geminicli.com/docs/tools/web-fetch)
- [**MCP Server Integration**](https://www.geminicli.com/docs/tools/mcp-server) - ขยายด้วยเครื่องมือที่กำหนดเอง
- [**Custom Extensions**](https://geminicli.com/docs/extensions/writing-extensions) - สร้างและแบ่งปันคำสั่งของคุณเอง

### หัวข้อขั้นสูง

- [**Headless Mode (Scripting)**](https://www.geminicli.com/docs/cli/headless) - ใช้ Gemini CLI ในเวิร์กโฟลว์อัตโนมัติ
- [**IDE Integration**](https://www.geminicli.com/docs/ide-integration) - ตัวแปลง VS Code
- [**Sandboxing & Security**](https://www.geminicli.com/docs/cli/sandbox) - สภาพแวดล้อมการดำเนินการที่ปลอดภัย
- [**Trusted Folders**](https://www.geminicli.com/docs/cli/trusted-folders) - ควบคุมนโยบายการดำเนินการตามโฟลเดอร์
- [**Enterprise Guide**](https://www.geminicli.com/docs/cli/enterprise) - ปรับใช้และจัดการในสภาพแวดล้อมองค์กร
- [**Telemetry & Monitoring**](https://www.geminicli.com/docs/cli/telemetry) - การติดตามการใช้งาน
- [**Tools reference**](https://www.geminicli.com/docs/reference/tools) - ภาพรวมเครื่องมือในตัว
- [**Local development**](https://www.geminicli.com/docs/local-development) - เครื่องมือการพัฒนาในพื้นที่

### การแก้ไขปัญหาและการสนับสนุน

- [**Troubleshooting Guide**](https://www.geminicli.com/docs/resources/troubleshooting) - ปัญหาทั่วไปและแนวทางแก้ไข
- [**FAQ**](https://www.geminicli.com/docs/resources/faq) - คำถามที่พบบ่อย
- ใช้คำสั่ง `/bug` เพื่อรายงานปัญหาโดยตรงจาก CLI

### การใช้เซิร์ฟเวอร์ MCP

กำหนดค่าเซิร์ฟเวอร์ MCP ใน `~/.gemini/settings.json` เพื่อขยาย Gemini CLI ด้วยเครื่องมือที่กำหนดเอง:

```text
> @github List my open pull requests
> @slack Send a summary of today's commits to #dev channel
> @database Run a query to find inactive users
```

ดู [MCP Server Integration guide](https://www.geminicli.com/docs/tools/mcp-server) สำหรับคำแนะนำการตั้งค่า

## 🤝 การมีส่วนร่วม

เรายินดีต้อนรับการมีส่วนร่วม! Gemini CLI เป็นโอเพนซอร์สอย่างเต็มที่ (Apache 2.0) และเราสนับสนุนให้ชุมชนทำสิ่งต่อไปนี้:

- รายงานข้อบัญหาและแนะนำคุณสมบัติ
- ปรับปรุงเอกสาร
- ส่งการปรับปรุงโค้ด
- แบ่งปันเซิร์ฟเวอร์ MCP และส่วนขยายของคุณ

ดู [Contributing Guide](./CONTRIBUTING.md) สำหรับการตั้งค่าการพัฒนา มาตรฐานการเข้ารหัส และวิธีการส่ง pull requests

ตรวจสอบ [Official Roadmap](https://github.com/orgs/google-gemini/projects/11) สำหรับคุณสมบัติและความสำคัญที่วางแผนไว้

## 📖 ทรัพยากร

- **[Free Course](https://learn.deeplearning.ai/courses/gemini-cli-code-and-create-with-an-open-source-agent/information)** - เรียนรู้พื้นฐาน
- **[Official Roadmap](./ROADMAP.md)** - ดูว่ามีอะไรมาต่อไป
- **[Changelog](https://www.geminicli.com/docs/changelogs)** - ดูการอัปเดตที่โดดเด่นเมื่อเร็วๆ นี้
- **[NPM Package](https://www.npmjs.com/package/@google/gemini-cli)** - รีจิสทรีแพ็คเกจ
- **[GitHub Issues](https://github.com/google-gemini/gemini-cli/issues)** - รายงานข้อบัญหาหรือขอคุณสมบัติ
- **[Security Advisories](https://github.com/google-gemini/gemini-cli/security/advisories)** - การอัปเดตความปลอดภัย

### ถอนการติดตั้ง

ดู [Uninstall Guide](https://www.geminicli.com/docs/resources/uninstall) สำหรับคำแนะนำการนำออก

## 📄 ข้อมูลทางกฎหมาย

- **License**: [Apache License 2.0](LICENSE)
- **Terms of Service**: [Terms & Privacy](https://www.geminicli.com/docs/resources/tos-privacy)
- **Security**: [Security Policy](SECURITY.md)

<p align="left">
 <a href="https://www.star-history.com/google-gemini/gemini-cli">
  <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/badge?repo=google-gemini/gemini-cli&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/badge?repo=google-gemini/gemini-cli" />
   <img alt="Star History Rank" src="https://api.star-history.com/badge?repo=google-gemini/gemini-cli" />
  </picture>
 </a>
</p>

---

<p align="center">
  สร้างด้วย ❤️ โดย Google และชุมชนโอเพนซอร์ส
  <br/>
  📌 <strong><a href="./README_TH.md">ดูเวอร์ชันไทยแบบเต็ม</a></strong>
</p>

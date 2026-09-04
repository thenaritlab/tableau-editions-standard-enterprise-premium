# 🚀 คู่มือเปิดใช้งาน Tableau Pulse และ Tableau Agent (Cloud & On-Premise)

> คู่มือฉบับรวมขั้นตอน "เปิดสวิตช์" ฟีเจอร์ AI ของ Tableau — Tableau Pulse และ Tableau Agent — ทั้งบน Tableau Cloud และ Tableau Server (On-Premise) พร้อมลิงก์อ้างอิงอย่างเป็นทางการจาก Tableau ทุกขั้นตอน

[![Tableau](https://img.shields.io/badge/Tableau-2026-E97627?logo=tableau&logoColor=white)](https://www.tableau.com)
[![Language](https://img.shields.io/badge/ภาษา-ไทย-blue)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

🏠 [หน้าแรก](./README.md) &nbsp;|&nbsp; ⬅️ [เปรียบเทียบ Edition](./01-tableau-editions-comparison-th.md) &nbsp;|&nbsp; 📄 กำลังอ่าน: **คู่มือเปิดใช้งาน**

---

## 📑 สารบัญ

- [ภาพรวม & สิ่งที่ต้องมีก่อนเริ่ม](#-ภาพรวม--สิ่งที่ต้องมีก่อนเริ่ม)
- [📊 เปิดใช้งาน Tableau Pulse (Tableau Cloud เท่านั้น)](#-เปิดใช้งาน-tableau-pulse-tableau-cloud-เท่านั้น)
- [🤖 เปิดใช้งาน Tableau Agent บน Tableau Cloud](#-เปิดใช้งาน-tableau-agent-บน-tableau-cloud)
- [🤖 เปิดใช้งาน Tableau Agent บน Tableau Server (On-Premise)](#-เปิดใช้งาน-tableau-agent-บน-tableau-server-on-premise)
- [🔑 สิทธิ์ผู้ใช้งาน (Permissions) ที่เกี่ยวข้อง](#-สิทธิ์ผู้ใช้งาน-permissions-ที่เกี่ยวข้อง)
- [📚 ลิงก์อ้างอิงทางการทั้งหมด](#-ลิงก์อ้างอิงทางการทั้งหมด)

---

## ภาพรวม & สิ่งที่ต้องมีก่อนเริ่ม

| ฟีเจอร์ | ใช้ได้บน Deployment ไหน | Edition ขั้นต่ำ | ต้องเชื่อม Salesforce Org ไหม |
|---|---|---|---|
| **Tableau Pulse** (พื้นฐาน) | ☁️ Tableau Cloud เท่านั้น | Standard ขึ้นไป | ❌ ไม่ต้อง |
| **Tableau Agent ใน Pulse** | ☁️ Tableau Cloud เท่านั้น | Cloud+ / Tableau+ | ✅ ต้องเชื่อม + เปิด Einstein Generative AI |
| **Tableau Agent** (Viz Authoring / Prep) | ☁️ Tableau Cloud | Cloud+ / Tableau+ | ✅ ต้องเชื่อม + เปิด Einstein Generative AI |
| **Tableau Agent** (Viz Authoring / Prep) | 🖥️ Tableau Server (On-Premise) | ทุก Edition (ตั้งแต่เวอร์ชัน **2025.3**) | ❌ ไม่ต้อง — แต่ต้องมี API Key ของ OpenAI/Azure OpenAI เอง |

> [!WARNING]
> **Tableau Pulse ไม่รองรับบน Tableau Server (On-Premise)** — เป็นฟีเจอร์ที่ผูกกับ Tableau Cloud เท่านั้น หากองค์กรใช้ Tableau Server แบบ Self-hosted และต้องการ Pulse จะต้องพิจารณาย้ายไปใช้ Tableau Cloud หรือใช้ Tableau Agent บน Server แทน (ซึ่งให้ประสบการณ์ AI คนละแบบกัน)

---

## 📊 เปิดใช้งาน Tableau Pulse (Tableau Cloud เท่านั้น)

Tableau Pulse ปิดใช้งานเป็นค่าเริ่มต้น ต้องให้ Site Administrator เข้าไปเปิดเอง

1. เข้าสู่ระบบ Tableau Cloud ด้วยบัญชีที่มีสิทธิ์ **Site Administrator**
2. จากเมนูด้านซ้าย เลือก **Settings**
3. เลื่อนไปหาหัวข้อ **Tableau Pulse Deployment** แล้วติ๊ก **Turn on Tableau Pulse**
4. เลือกขอบเขตผู้ใช้งาน: **For all users on this site** (ทุกคน) หรือ **Only for users in a specified group** (กลุ่มที่กำหนด — เหมาะกับการทดลองใช้ก่อน Roll out เต็มรูปแบบ)
5. (ทางเลือก) เลื่อนไปหัวข้อ **Availability of Tableau AI** แล้วติ๊ก **"Tableau Pulse: Summarizes key metric insights"** เพื่อให้ AI ช่วยสรุป Insight เป็นภาษาที่อ่านง่ายขึ้น
6. กด **Save**
7. ไปที่เมนู **Tableau Pulse** ทางซ้าย แล้วเลือก **New Metric Definition** เพื่อเริ่มสร้าง Metric แรกจาก Published Data Source

> [!TIP]
> แนะนำให้เริ่มแบบ **Controlled Rollout** — เปิดให้กลุ่มเล็ก ๆ ทดลองใช้ก่อน แล้วค่อยขยายเป็นทั้งองค์กร เพื่อให้ผู้ใช้เข้าใจวิธีตั้ง Metric และ Digest ก่อนเปิดวงกว้าง

📎 อ้างอิง: [Set Up Your Site for Tableau Pulse — Tableau Help](https://help.tableau.com/current/online/en-us/pulse_set_up.htm)

---

## 🤖 เปิดใช้งาน Tableau Agent บน Tableau Cloud

การเปิด Tableau Agent บน Cloud ต้องทำ 2 ฝั่งคู่กัน คือฝั่ง **Salesforce** และฝั่ง **Tableau Cloud** เนื่องจากฟีเจอร์นี้วิ่งผ่าน Einstein Trust Layer

**สิ่งที่ต้องมีก่อน:** Edition ต้องเป็น **Cloud+ หรือ Tableau+ Bundle**, มีสิทธิ์ Tableau Site Administrator, และมี Salesforce Org ที่เปิดใช้ Einstein Generative AI แล้ว

1. **เปิดใช้งาน Salesforce Org** — เตรียม Org ที่จะใช้เชื่อมกับ Tableau Cloud (ถ้ายังไม่มี ต้องสร้างและตั้งค่า Data Cloud ก่อน)
2. **ตั้งค่า Data Cloud Architect User** — กำหนดผู้ใช้ในฝั่ง Salesforce ที่จะดูแลการเชื่อมต่อ Data Cloud
3. **สร้าง Connected App ใน Salesforce** — ไปที่ Salesforce Setup → App Manager → New Connected App เพื่อสร้าง OAuth Client ID/Secret สำหรับเชื่อมกับ Tableau
4. **กลับมาที่ Tableau Cloud → Settings → AI in Tableau** — ใส่ข้อมูล Salesforce Org ที่เตรียมไว้เพื่อเชื่อมต่อ (Connect)
5. **เปิดฟีเจอร์ที่ต้องการทีละส่วน** ภายใต้หัวข้อ AI in Tableau:
   - **Tableau Agent สำหรับ Viz Authoring** — ให้ผู้ใช้สร้าง Visualization ด้วยภาษาธรรมชาติ
   - **Tableau Agent สำหรับ Tableau Prep** — ให้ผู้ใช้ทำความสะอาดข้อมูลด้วยภาษาธรรมชาติ
   - **Tableau Agent ใน Pulse** — เปิด Conversational Q&A ข้าม Metric (ต้องเปิด Tableau Pulse ไว้ก่อนแล้ว)
6. **เลือกขอบเขตผู้ใช้งาน** — เลือกได้ว่าจะเปิดให้ทุกคน หรือเฉพาะกลุ่มผู้ใช้ที่กำหนด (รองรับเฉพาะ Viz Authoring และ Prep เท่านั้น — Pulse ผูกกับขอบเขตของ Pulse ที่ตั้งไว้แล้ว)
7. กด **Save**

> [!NOTE]
> หากยังไม่มี Tableau+ แต่อยากทดลองใช้ Tableau Agent ก่อน สามารถสมัคร **Tableau Cloud Free Trial** ซึ่งรวม Tableau Agent ไว้ให้ทดลองใช้ได้ทันทีโดยไม่ต้องเชื่อม Salesforce Org

📎 อ้างอิง:
- [Turn On AI in Your Tableau Cloud Site — Tableau Help](https://help.tableau.com/current/online/en-us/setup_tabAI_site_setting.htm)
- [Build Tableau Prep flows with Tableau Agent — Tableau Help](https://help.tableau.com/current/prep/en-us/prep_einstein.htm)

---

## 🤖 เปิดใช้งาน Tableau Agent บน Tableau Server (On-Premise)

บน Tableau Server การเปิด Tableau Agent **ง่ายกว่า Cloud** เพราะไม่ต้องเชื่อม Salesforce Org — แต่ต้องหา LLM มาเชื่อมเอง (Bring Your Own LLM)

**สิ่งที่ต้องมีก่อน:**
- Tableau Server เวอร์ชัน **2025.3 ขึ้นไป**
- สิทธิ์ **Server Administrator**
- สัญญาใช้งานกับ **OpenAI** หรือ **Azure OpenAI** (Azure OpenAI รองรับตั้งแต่เวอร์ชัน 2026.2) พร้อม **API Key**
- ถ้าใช้ Azure OpenAI ต้องมี Model ที่ Deploy ไว้ใน Azure แล้ว

**ขั้นตอน:**

1. เข้าสู่ระบบ Tableau Server ด้วยบัญชี **Server Administrator**
2. ไปที่ Site ที่ต้องการเปิดใช้งาน แล้วเลือก **Settings**
3. ที่หัวข้อ **AI in Tableau** กด **Connect**
4. ในหน้าต่าง **Connect to LLM** เลือก LLM Provider: **OpenAI** หรือ **Azure OpenAI**
5. กรอก **API Key** ของ LLM Provider ที่เตรียมไว้ (ถ้าเป็น Azure OpenAI ต้องกรอก Endpoint และชื่อ Deployment Model ด้วย)
6. กด **Connect**
7. กำหนด **Model ที่ใช้ในแต่ละงาน** เช่น รุ่นสำหรับ "ทำความเข้าใจคำขอของผู้ใช้" (Tableau แนะนำ `gpt-5-mini` หรือ `gpt-4o-mini` สำหรับงานนี้)
8. เปิดใช้งานฟีเจอร์ที่ต้องการ: **Tableau Agent สำหรับ Web Authoring** และ/หรือ **Tableau Agent สำหรับ Tableau Prep**
9. กด **Save**

> [!IMPORTANT]
> บน Tableau Server การตั้งค่านี้เป็นแบบ**เปิดทั้ง Site** — ไม่สามารถเลือกเปิดเฉพาะกลุ่มผู้ใช้ได้เหมือนบน Cloud และ**ไม่ผ่าน Einstein Trust Layer** จึงไม่มี PII Masking ในตัว ควรตรวจสอบนโยบายความปลอดภัยข้อมูลของ LLM Provider ที่เลือกใช้ให้รอบคอบก่อนเปิดใช้งานจริง และควรตั้งรอบหมุนเวียน (Rotate) API Key เป็นประจำตามหลัก Security Best Practice

📎 อ้างอิง: [Turn on AI in Your Tableau Server Site — Tableau Help](https://help.tableau.com/current/server/en-us/sites_gai_server.htm)

---

## 🔑 สิทธิ์ผู้ใช้งาน (Permissions) ที่เกี่ยวข้อง

| บทบาท | ทำอะไรได้เกี่ยวกับ Pulse/Agent |
|---|---|
| **Server/Site Administrator** | เปิด/ปิดฟีเจอร์ AI ทั้งหมดในระดับ Site, เชื่อมต่อ LLM/Salesforce Org |
| **Creator** | สร้าง/แก้ไข/ลบ Metric Definition ใน Pulse, ใช้ Tableau Agent เต็มรูปแบบ (ถ้าเปิดสิทธิ์ไว้) |
| **Explorer (can publish)** | สร้าง/แก้ไข Metric Definition ได้เช่นกัน, ใช้ Tableau Agent ได้ตามสิทธิ์ที่ได้รับ |
| **Viewer** | ดู Metric และ Insight ใน Pulse ได้, ใช้ Tableau Agent ใน Dashboard ได้เฉพาะกรณีที่ Admin เปิดสิทธิ์ **AI Access** และ **Full Data Query** ให้ |

---

## 📚 ลิงก์อ้างอิงทางการทั้งหมด

- [Set Up Your Site for Tableau Pulse — Tableau Help](https://help.tableau.com/current/online/en-us/pulse_set_up.htm)
- [Configure Site & Permissions for Tableau Pulse — Trailhead](https://trailhead.salesforce.com/content/learn/modules/tableau-pulse-fundamentals/configure-your-site-and-permissions)
- [Turn On AI in Your Tableau Cloud Site — Tableau Help](https://help.tableau.com/current/online/en-us/setup_tabAI_site_setting.htm)
- [Turn on AI in Your Tableau Server Site — Tableau Help](https://help.tableau.com/current/server/en-us/sites_gai_server.htm)
- [Build Tableau Prep flows with Tableau Agent — Tableau Help](https://help.tableau.com/current/prep/en-us/prep_einstein.htm)
- [Tableau Agent FAQ — Tableau Help](https://help.tableau.com/current/online/en-us/web_author_einstein_faq.htm)
- [AI in Tableau Features — Tableau Help](https://help.tableau.com/current/tableau/en-us/tableau_gai_solutions.htm)

---

*จัดทำเพื่อเผยแพร่ความรู้เกี่ยวกับการเปิดใช้งานฟีเจอร์ AI ของ Tableau — ขั้นตอนอาจเปลี่ยนแปลงตามเวอร์ชันของ Tableau กรุณาตรวจสอบ Release Notes ล่าสุดหรือปรึกษา Partner ที่ได้รับการรับรองก่อนดำเนินการจริงในระบบ Production*

---

### 📖 อ่านต่อ

⬅️ ทบทวนความแตกต่างของแต่ละ Edition ก่อนได้ที่ [เปรียบเทียบ Tableau Editions](./01-tableau-editions-comparison-th.md)

🏠 [กลับหน้าแรก](./README.md)

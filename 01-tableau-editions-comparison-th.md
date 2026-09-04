# 📊 เปรียบเทียบ Tableau Editions: Standard vs Enterprise vs Premium (Cloud+ / Tableau+)

> คู่มือฉบับย่อ อธิบายความแตกต่างของแพ็กเกจ Tableau ในปี 2026 พร้อมคำแนะนำว่าองค์กรแบบไหนควรเลือกแพ็กเกจใด

[![Tableau](https://img.shields.io/badge/Tableau-2026-E97627?logo=tableau&logoColor=white)](https://www.tableau.com)
[![Language](https://img.shields.io/badge/ภาษา-ไทย-blue)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

🏠 [หน้าแรก](./README.md) &nbsp;|&nbsp; 📄 กำลังอ่าน: **เปรียบเทียบ Edition** &nbsp;|&nbsp; ➡️ [คู่มือเปิดใช้งาน Pulse/Agent](./02-tableau-pulse-agent-setup-guide-th.md)

---

## 📑 สารบัญ

- [ภาพรวม: Tableau มีอะไรให้เลือกบ้าง](#ภาพรวม-tableau-มีอะไรให้เลือกบ้าง)
- [ตารางเปรียบเทียบหลัก](#-ตารางเปรียบเทียบหลัก)
- [รายละเอียดแต่ละ Edition](#-รายละเอียดแต่ละ-edition)
  - [🟢 Standard Edition](#-standard-edition)
  - [🔵 Enterprise Edition](#-enterprise-edition)
  - [🟣 Premium (Cloud+ / Server+ / Tableau+ Bundle)](#-premium-cloud--server--tableau-bundle)
- [🗂️ Data Management คืออะไร](#️-data-management-คืออะไร)
- [🛡️ Advanced Management คืออะไร](#️-advanced-management-คืออะไร)
- [⚡ Tableau Pulse vs Pulse Premium](#-tableau-pulse-vs-pulse-premium)
- [🤖 Tableau Agent คืออะไร](#-tableau-agent-คืออะไร)
- [เหมาะกับใคร?](#-เหมาะกับใคร)
- [ประโยชน์ที่ได้รับในแต่ละระดับ](#-ประโยชน์ที่ได้รับในแต่ละระดับ)
- [ข้อควรรู้ก่อนตัดสินใจ](#️-ข้อควรรู้ก่อนตัดสินใจ)
- [อ้างอิง](#-อ้างอิง)

---

## ภาพรวม: Tableau มีอะไรให้เลือกบ้าง

Tableau แบ่งการใช้งานออกเป็น 2 มิติหลัก:

1. **รูปแบบการติดตั้ง (Deployment)** — เลือกระหว่าง **Tableau Cloud** (Salesforce โฮสต์ให้ทั้งหมด) หรือ **Tableau Server** (องค์กรดูแล Infrastructure เอง) ทั้งสองแบบมีโครงสร้าง Edition เหมือนกัน
2. **ระดับแพ็กเกจ (Edition)** — แบ่งเป็น 3 ระดับ: **Standard → Enterprise → Premium** (Cloud+ / Server+ / Tableau+ Bundle) แต่ละระดับปลดล็อกฟีเจอร์เพิ่มขึ้น โดยราคาต่อ License ก็เพิ่มขึ้นตามไปด้วย

> [!NOTE]
> ทุก Edition ต้องมี **Creator License อย่างน้อย 1 ที่นั่ง** เสมอ และไม่สามารถผสม Edition ต่างระดับในองค์กรเดียวกันได้ (ต้องเลือก Edition เดียวสำหรับทั้ง Deployment)

### ประเภทผู้ใช้งาน (License Role) — เหมือนกันทุก Edition

| Role | ทำอะไรได้ |
|---|---|
| **Viewer** | ดู Dashboard, โต้ตอบพื้นฐาน, รับ Data-driven Alert |
| **Explorer** | แก้ไข Workbook เดิม, ดาวน์โหลดข้อมูลเต็ม, จัดการผู้ใช้/เนื้อหาบางส่วน |
| **Creator** | สร้าง Workbook/Data Flow ใหม่, เชื่อมต่อข้อมูล, ใช้ Tableau Desktop และ Tableau Prep Builder ได้เต็มรูปแบบ |

---

## 📋 ตารางเปรียบเทียบหลัก

| หัวข้อ | 🟢 Standard | 🔵 Enterprise | 🟣 Premium (Cloud+/Tableau+) |
|---|---|---|---|
| **ราคา (Creator)** | ~$75/user/เดือน | ~$115/user/เดือน | ติดต่อฝ่ายขาย (Custom Quote) |
| **ราคา (Explorer)** | ~$42/user/เดือน | ~$70/user/เดือน | ติดต่อฝ่ายขาย |
| **ราคา (Viewer)** | ~$15/user/เดือน | ~$35/user/เดือน | ติดต่อฝ่ายขาย |
| **จำนวน Site รองรับ** | สูงสุด 3 sites | สูงสุด 10 sites | ขยายได้มากกว่า + Environment เพิ่มเติม (Server+) |
| **Tableau Desktop / Prep Builder** | ✅ (สำหรับ Creator) | ✅ | ✅ |
| **Tableau Pulse (AI Insight พื้นฐาน)** | ✅ | ✅ | ✅ พร้อม **Pulse Premium** |
| **Data Management** (Catalog, Prep Conductor, Lineage) | ❌ | ✅ | ✅ |
| **Advanced Management** (Content Migration, API Control, Activity Log) | ❌ | ✅ | ✅ |
| **Tableau Agent** (AI สร้างกราฟด้วยภาษาธรรมชาติ) | ❌ | บางส่วน* | ✅ เต็มรูปแบบ (Cloud) |
| **Agentforce Skills** (Concierge, Inspector, Data Pro) | ❌ | ❌ | ✅ |
| **Data Cloud Credits** | ❌ | ❌ | ✅ (เช่น 250,000 เครดิต/ปี) |
| **eLearning** | ❌ | ✅ | ✅ |
| **ระดับ Support** | Standard Success | Standard Success + eLearning | Premier Success (24/7, ตอบเร็ว, มี TAM) |
| **Capacity-based Licensing (Viewer Block)** | ✅ | ✅ | ✅ |
| **เหมาะกับ** | ทีมเริ่มต้น/ขนาดกลาง | องค์กรขนาดใหญ่ที่ต้อง Governance | องค์กรที่ต้องการ AI เต็มรูปแบบ + Support สูงสุด |

> [!IMPORTANT]
> ราคาข้างต้นอ้างอิงจาก Tableau Cloud (ข้อมูลเปิดเผยต่อสาธารณะ กลางปี 2026) เป็น**ราคาโดยประมาณ** สำหรับใช้เปรียบเทียบเชิงโครงสร้างเท่านั้น ราคาจริงและเงื่อนไขสัญญาอาจเปลี่ยนแปลง ควรตรวจสอบกับ Tableau หรือ Partner ที่ได้รับการรับรองในประเทศไทยก่อนตัดสินใจซื้อ
>
> \* **Tableau Agent บน Enterprise** ใช้ได้เต็มรูปแบบบน **Tableau Server** (ตั้งแต่ 2025.3) แต่ต้องเชื่อมต่อ LLM ของตัวเอง — ส่วนบน **Tableau Cloud** ต้องอัปเกรดเป็น Cloud+/Tableau+ เท่านั้นถึงจะใช้ได้ ดูรายละเอียดที่หัวข้อ [🤖 Tableau Agent คืออะไร](#-tableau-agent-คืออะไร)

---

## 🔍 รายละเอียดแต่ละ Edition

### 🟢 Standard Edition

Edition พื้นฐานที่มีครบสำหรับการเริ่มต้นทำ Self-Service Analytics อย่างมีธรรมาภิบาล (Governance) ในระดับหนึ่ง

**สิ่งที่ได้รับ:**
- การสร้าง วิเคราะห์ และแชร์ Dashboard แบบเต็มรูปแบบ
- Tableau Desktop และ Tableau Prep Builder (สำหรับ Creator)
- Tableau Pulse สำหรับ Insight พื้นฐานแบบอัตโนมัติ
- รองรับสูงสุด 3 Sites
- Standard Success (คู่มือ, บทเรียนออนไลน์แบบ Self-guided)

**ข้อจำกัด:**
- ไม่มี Data Management (ไม่มี Data Catalog / Lineage / Prep Conductor)
- ไม่มี Advanced Management (Activity Log, Content Migration Tool)
- ไม่มี eLearning แบบมีผู้สอน

---

### 🔵 Enterprise Edition

ออกแบบมาสำหรับองค์กรที่ข้อมูลซับซ้อนขึ้น ผู้ใช้งานเยอะขึ้น และต้องการ Governance ระดับองค์กร

**สิ่งที่เพิ่มจาก Standard:**
- **Data Management** — Data Catalog, Data Lineage, Prep Conductor (Automate การเตรียมข้อมูล)
- **Advanced Management** — Activity Log, Content Migration Tool, API Control ระดับสูง
- รองรับสูงสุด 10 Sites
- eLearning แบบมีโครงสร้างหลักสูตร
- Capacity-based Viewer Block (เปิดให้ผู้ใช้ดู Dashboard ได้ไม่จำกัดจำนวนบัญชี โดยคิดตามการใช้งานพร้อมกัน)

> [!TIP]
> จากข้อมูลตลาด องค์กรขนาดกลาง-ใหญ่ส่วนใหญ่ที่ต้องการ Governance หรือ Tableau Pulse แบบเต็มรูปแบบ มักจบที่ Enterprise Edition เพราะ Standard ไม่เพียงพอสำหรับความต้องการด้าน Compliance และการบริหารจัดการผู้ใช้จำนวนมาก

---

### 🟣 Premium (Cloud+ / Server+ / Tableau+ Bundle)

ระดับสูงสุด เน้น **Agentic Analytics** — ให้ AI ช่วยวิเคราะห์ ตอบคำถาม และดำเนินการแทนผู้ใช้ได้มากขึ้น

**สิ่งที่เพิ่มจาก Enterprise:**
- **Tableau Agent** — สร้างและวิเคราะห์ Visualization ด้วยภาษาธรรมชาติ ผ่าน Einstein Trust Layer แบบเต็มรูปแบบ พร้อม Zero Data Retention และ PII Masking อัตโนมัติ (ดูรายละเอียดที่หัวข้อ [🤖 Tableau Agent คืออะไร](#-tableau-agent-คืออะไร))
- **Pulse Premium Features** — Conversational Analytics พร้อมอ้างอิงแหล่งข้อมูล (Citation) และ Insight เชิงลึก
- **Agentforce Skills** — ชุดความสามารถ AI สำเร็จรูป 3 แบบ: Concierge (ตอบคำถาม), Inspector (เฝ้าระวังข้อมูลผิดปกติ), Data Pro (เตรียมข้อมูลอัตโนมัติ)
- **Data Cloud Credits** — โควตาสำหรับเชื่อมต่อ Salesforce Data Cloud (เช่น 250,000 เครดิต/ปี)
- **Premier Success** — Technical Account Manager ส่วนตัว, Support 24/7 แบบเร่งด่วน
- Environment เพิ่มเติมสำหรับ Server+ (1 Production + สูงสุด 6 Non-production สำหรับทดสอบ)

**ข้อควรพิจารณา:**
- ไม่มีราคาสาธารณะ ต้องคุยกับทีมขายโดยตรง
- เหมาะกับองค์กรที่ผูกกับ Salesforce Ecosystem อยู่แล้ว (Sales Cloud / Service Cloud / Data Cloud)
- มีค่าใช้จ่ายแปรผัน (Data Cloud Credits) ที่ Standard/Enterprise ไม่มี

---

## 🗂️ Data Management คืออะไร

**Data Management** คือชุดฟีเจอร์ที่ช่วยให้ข้อมูลใน Tableau "น่าเชื่อถือ ค้นหาง่าย และดูแลรักษาได้เป็นระบบ" เริ่มมีให้ใช้ตั้งแต่ระดับ **Enterprise** ขึ้นไป ประกอบด้วย 3 ส่วนหลัก:

| ฟีเจอร์ | ทำอะไรได้ | ประโยชน์ที่ได้ |
|---|---|---|
| 🔎 **Tableau Catalog** | ค้นหาและติดตามข้อมูลทั้งหมดที่ถูกใช้ใน Tableau, ดู Data Lineage (ข้อมูลมาจากไหน ไปอยู่ Dashboard ไหนบ้าง), แจ้งเตือนคุณภาพข้อมูล (Data Quality Warning) | รู้ผลกระทบก่อนแก้ไขข้อมูลต้นทาง ลดปัญหา "แก้ตารางเดียว Dashboard พังทั้งบริษัท" |
| ⚙️ **Tableau Prep Conductor** | ตั้งเวลาและติดตามการรัน Flow เตรียมข้อมูล (Prep Flow) อัตโนมัติ พร้อมแจ้งเตือนเมื่อ Flow ทำงานล้มเหลว | ไม่ต้องมานั่งกดรันข้อมูลเองทุกวัน มั่นใจว่าข้อมูลที่ใช้วิเคราะห์เป็นข้อมูลล่าสุดเสมอ |
| 🔐 **Virtual Connections & Data Policies** | สร้างจุดเชื่อมต่อข้อมูลกลางที่แชร์ใช้ร่วมกันได้ พร้อมกำหนด Row-Level Security (RLS) ไว้ที่ระดับ Connection เดียว | ตั้งสิทธิ์การเห็นข้อมูลครั้งเดียว ใช้ได้กับทุก Dashboard ที่เชื่อมต่อ ไม่ต้องตั้งซ้ำทีละไฟล์ |

> [!NOTE]
> Data Management ไม่ได้ขายแยกเป็น Add-on อีกต่อไปแล้ว (ตั้งแต่ 16 ก.ย. 2024) ปัจจุบันจะได้ใช้ก็ต่อเมื่อซื้อ **Enterprise Edition** หรือ **Tableau+** เท่านั้น

---

## 🛡️ Advanced Management คืออะไร

**Advanced Management** คือชุดเครื่องมือสำหรับ "ผู้ดูแลระบบ" (Admin) เพื่อบริหารจัดการ Deployment ขนาดใหญ่ให้ปลอดภัยและตรวจสอบย้อนหลังได้ เริ่มมีให้ใช้ตั้งแต่ระดับ **Enterprise** ขึ้นไปเช่นกัน:

| ฟีเจอร์ | ทำอะไรได้ | ประโยชน์ที่ได้ |
|---|---|---|
| 📦 **Content Migration Tool (CMT)** | ย้าย Workbook, Data Source, Project, User และสิทธิ์การเข้าถึง ระหว่าง Dev → Production หรือระหว่าง Site/Server แบบไม่ต้องเขียนโค้ด ทำเป็นแผนย้ายที่ตั้งเวลารันซ้ำได้ | ลดความผิดพลาดจากการย้ายไฟล์ด้วยมือ ย้าย Dashboard นับร้อยไฟล์เสร็จในไม่กี่คลิก |
| 📝 **Activity Log & Admin Insights** | บันทึกทุกกิจกรรมของผู้ใช้แบบละเอียด (ใครดู/แก้/ดาวน์โหลดอะไร เมื่อไหร่) พร้อม Dashboard สำเร็จรูปวิเคราะห์อัตราการใช้งาน | ใช้เป็นหลักฐานตรวจสอบ (Audit) ตอบโจทย์ Compliance และเห็นว่า Dashboard ไหนถูกใช้จริง อันไหนควรเลิกใช้ |
| 🖥️ **Resource Monitoring Tool** (เฉพาะ Tableau Server) | ติดตามการใช้ทรัพยากรฮาร์ดแวร์ (CPU/RAM) ของ Server แจ้งเตือนก่อนระบบมีปัญหา | ป้องกัน Server ล่มจากการใช้งานหนัก วางแผนขยาย Infrastructure ได้ล่วงหน้า |
| 🔑 **Customer-Managed Encryption Keys (CMEK)** | จัดการ Encryption Key สำหรับเข้ารหัสข้อมูลด้วยตัวเอง (สร้าง/หมุนเวียน/ลบ Key ได้) | ตอบโจทย์นโยบายความปลอดภัยข้อมูลระดับองค์กร โดยเฉพาะกลุ่มการเงิน/ประกันภัย/สุขภาพ |

> [!NOTE]
> เช่นเดียวกับ Data Management — Advanced Management ไม่ได้ขายแยกเป็น Add-on อีกต่อไป (ตั้งแต่ 16 ก.ย. 2024) ต้องซื้อผ่าน **Enterprise Edition** หรือ **Tableau+** เท่านั้น

---

## ⚡ Tableau Pulse vs Pulse Premium

**Tableau Pulse** คือฟีเจอร์ AI ที่ "ส่ง Insight มาหาผู้ใช้" แทนที่จะให้ผู้ใช้ไปเปิดหา Dashboard เอง — มากับทุก Edition ของ Tableau Cloud โดยไม่มีค่าใช้จ่ายเพิ่ม ส่วน **Pulse Premium** เป็นความสามารถขั้นสูงกว่า ที่มีเฉพาะใน **Tableau+ Bundle** เท่านั้น

| ความสามารถ | 🔹 Tableau Pulse (มาตรฐาน) | 🔸 Pulse Premium (Tableau+ เท่านั้น) |
|---|---|---|
| หน้าสรุป Metric ส่วนตัว (Personalized Homepage) | ✅ | ✅ |
| แจ้งเตือนความผิดปกติอัตโนมัติ (Anomaly Detection) | ✅ | ✅ |
| สรุปเหตุผลเบื้องหลัง Insight ด้วยภาษาธรรมชาติ | ✅ (พื้นฐาน) | ✅ (ละเอียดขึ้น พร้อม Citation อ้างอิงแหล่งข้อมูล) |
| **Enhanced Q&A / Discover** — ถามคำถามข้ามหลาย Metric พร้อมกัน | ❌ | ✅ |
| **Dynamic Sorting & Grouping** — จัดกลุ่ม/เรียง Metric อัตโนมัติตามความเกี่ยวข้อง | ❌ | ✅ |
| **Metric Goals & Threshold Tracking** — ติดตามเทียบกับเป้าหมาย ไม่ใช่แค่ค่าสิ้นงวด | ❌ | ✅ |
| กำหนดความถี่ Digest ได้ยืดหยุ่น (Digest Cadence) | จำกัด | ✅ ปรับได้ตามรอบข้อมูล Refresh |
| แจ้งเตือนนอกรอบ (Off-cycle Alert) เมื่อ Metric ผิดปกติกะทันหัน | ❌ | ✅ (สูงสุด 1 ครั้ง/วัน) |
| กรอง/เปรียบเทียบ Metric ตามภูมิภาค/สินค้า ด้วยภาษาธรรมชาติ | ❌ | ✅ |
| ระยะเวลาข้อมูลย้อนหลังที่ใช้วิเคราะห์ | มาตรฐาน | ยาวขึ้น + โมเดล AI ขั้นสูงกว่า |
| ใช้งานร่วมกับ Salesforce Data Cloud / Einstein Trust Layer | พื้นฐาน | เต็มรูปแบบ (ต้องเชื่อม Salesforce Org) |

> [!TIP]
> สรุปง่าย ๆ: **Pulse มาตรฐาน** เหมาะกับทีมที่ต้องการแค่ "รู้ว่า Metric อะไรผิดปกติ" ส่วน **Pulse Premium** เหมาะกับผู้บริหารที่ต้องการ "คุยกับข้อมูลได้เหมือนคุยกับนักวิเคราะห์" — ถามคำถามซับซ้อนข้ามหลาย Metric แล้วได้คำตอบพร้อมเหตุผลและแหล่งอ้างอิงทันที

---

## 🤖 Tableau Agent คืออะไร

**Tableau Agent** คือผู้ช่วย AI แบบสนทนา (Conversational AI) ที่ทำงานอยู่ในหน้า Web Authoring, Tableau Desktop, Tableau Prep และ (แบบ Beta) บน Dashboard โดยตรง ช่วยให้ผู้ใช้ "คุยกับข้อมูล" ด้วยภาษาธรรมชาติแทนการลาก-วางฟิลด์เอง

### Tableau Agent ทำอะไรได้บ้าง

- 📊 **สร้าง Visualization ด้วยภาษาพูด** — พิมพ์คำถามหรือคำสั่งเป็นภาษาธรรมชาติ แล้วให้ Agent สร้างกราฟ/Dashboard ให้อัตโนมัติ
- 🧮 **สร้างและอธิบาย Calculated Field** — ขอให้ Agent เขียนสูตรคำนวณให้ หรืออธิบายว่าสูตรที่มีอยู่ทำงานอย่างไร
- 🧹 **ช่วยงานใน Tableau Prep** — แนะนำขั้นตอนทำความสะอาด/แปลงข้อมูลด้วยภาษาธรรมชาติ
- 🏷️ **อธิบายเนื้อหาใน Tableau Catalog** — สรุปว่า Project, Workbook หรือ Data Source แต่ละตัวคืออะไร ใช้ทำอะไร
- 💬 **Conversational Analytics บน Dashboard (Beta)** — ถามคำถามเกี่ยวกับข้อมูลได้ทันทีจากหน้า Dashboard โดยไม่ต้องสลับไปหน้าอื่น
- 🔍 **Index ข้อมูลอัตโนมัติทุก Session** — วิเคราะห์โครงสร้างข้อมูล (ชนิดข้อมูล, ชื่อฟิลด์, ตัวอย่างค่า) ก่อนเริ่มตอบคำถาม เพื่อให้คำตอบตรงบริบท

> [!NOTE]
> Tableau Agent มองเห็น**เฉพาะ Data Source ที่ Workbook นั้นเชื่อมต่ออยู่**เท่านั้น ไม่รู้จัก Data Source อื่นในระบบ จึงไม่สามารถตอบคำถามข้าม Data Source หรือคำถามความรู้ทั่วไปได้ และจะเคารพสิทธิ์ Row-Level / Column-Level Security ที่ตั้งไว้เสมอ

### 🔀 ความแตกต่าง: Tableau Cloud vs Tableau Server (On-Premise)

นี่คือสิ่งที่คำว่า **"บางส่วน (ขึ้นกับ Deployment)"** ในตารางเปรียบเทียบหลักหมายถึง — Tableau Agent เปิดใช้งานได้ต่างกันตามรูปแบบการติดตั้ง:

| ประเด็น | ☁️ Tableau Cloud | 🖥️ Tableau Server (On-Premise) |
|---|---|---|
| **Edition ที่ใช้ได้** | ต้องเป็น **Cloud+ Edition หรือ Tableau+ Bundle** เท่านั้น | ใช้ได้ทุก Edition (Standard/Enterprise/Server+) ตั้งแต่เวอร์ชัน 2025.3 เป็นต้นไป |
| **LLM ที่ใช้** | Salesforce เลือก Model ให้อัตโนมัติ (ไม่ต้องตั้งค่าเอง) | องค์กรต้องเชื่อมต่อ LLM ของตัวเอง (Bring Your Own LLM) ผ่าน API Key |
| **ผ่าน Einstein Trust Layer หรือไม่** | ✅ ผ่าน — ได้ Zero Data Retention, PII Masking อัตโนมัติ | ❌ ไม่ผ่าน — ไม่มี PII Masking ในตัว ต้องพึ่งมาตรการความปลอดภัยของ LLM Provider เอง |
| **ค่าใช้จ่าย LLM** | รวมอยู่ใน Tableau+ Bundle แล้ว | แยกบิลตามสัญญาที่องค์กรทำกับ LLM Provider เอง |
| **การตั้งค่า** | เปิดใช้งานได้ทันที ไม่ต้องเตรียมอะไรเพิ่ม | ผู้ดูแลระบบ (Server Admin) ต้องตั้งค่า AI ระดับ Site และใส่ API Key เอง |

> [!IMPORTANT]
> สรุปสั้น ๆ: บน **Cloud** ต้องจ่ายเพิ่มเป็น Tableau+ ถึงจะได้ Agent แต่ได้ระบบความปลอดภัยครบจบในตัว ส่วนบน **Server (On-Premise)** ใช้ได้ตั้งแต่ Edition พื้นฐาน แต่ต้องหา LLM มาเชื่อมเอง และรับผิดชอบเรื่องความปลอดภัยข้อมูลเอง

### 🧠 LLM ที่รองรับ

| Deployment | LLM Provider ที่รองรับ | เลือก Model เองได้ไหม |
|---|---|---|
| **Tableau Cloud** | Salesforce จับคู่กับ Azure OpenAI โดยอัตโนมัติ (เลือก Model ที่ดีที่สุดตาม Performance/ความแม่นยำ/ต้นทุน ให้เอง) | ❌ เลือกเองไม่ได้ — Tableau เป็นผู้เลือกให้ |
| **Tableau Server** (ตั้งแต่ 2025.3) | **OpenAI** | ✅ เลือกได้ (เริ่มต้นรองรับตัวเดียว) |
| **Tableau Server** (ตั้งแต่ 2026.2) | **OpenAI** หรือ **Azure OpenAI** | ✅ เลือกได้ 2 ทางเลือก |

> [!NOTE]
> ปัจจุบัน Tableau Agent **ยังไม่รองรับการเชื่อมต่อ LLM แบบ Bring-Your-Own-LLM (BYOLLM) กว้าง ๆ** เช่น Amazon Bedrock, Google Gemini, หรือ Anthropic Claude โดยตรง (แม้ระบบ Salesforce/Agentforce โดยรวมจะรองรับผู้ให้บริการเหล่านี้ในฟีเจอร์ AI อื่นก็ตาม) สำหรับ Tableau Agent โดยเฉพาะ รองรับเพียง **OpenAI** และ **Azure OpenAI** เท่านั้น ข้อมูลนี้อาจเปลี่ยนแปลงได้ในอนาคต ควรตรวจสอบ Release Notes ล่าสุดก่อนวางแผน

### 💡 ประโยชน์ที่ได้รับจาก Tableau Agent

- ลดระยะเวลาสร้าง Dashboard จากชั่วโมงเหลือเป็นนาที ด้วยการพิมพ์คำถามแทนการลาก-วางฟิลด์
- ผู้ใช้ที่ไม่ถนัดสูตรคำนวณ สามารถขอให้ Agent เขียน Calculated Field ให้ และอธิบายวิธีทำงานได้ทันที
- ลดภาระทีม Data/BI ที่ต้องคอยตอบคำถามพื้นฐานซ้ำ ๆ จากผู้ใช้ทั่วไป
- องค์กรที่มีข้อจำกัดด้าน Data Residency หรือ Compliance สามารถเลือกใช้ Tableau Server + LLM ของตัวเองเพื่อควบคุมข้อมูลได้เต็มที่ แทนที่จะต้องส่งข้อมูลผ่าน Salesforce Cloud

---

## 🎯 เหมาะกับใคร?

| กลุ่มผู้ใช้ | Edition ที่แนะนำ | เหตุผล |
|---|---|---|
| ทีมเล็ก-กลาง เริ่มต้นทำ Data Visualization, งบจำกัด | 🟢 **Standard** | ครบเครื่องพื้นฐาน ราคาต่อ Seat ต่ำสุด เหมาะเริ่มต้นวิเคราะห์ข้อมูลและแชร์ Dashboard ในทีม |
| องค์กรขนาดใหญ่ มีหลายแผนก ต้องการควบคุมสิทธิ์/ตรวจสอบย้อนหลัง (Audit) | 🔵 **Enterprise** | มี Data Management + Advanced Management รองรับ Compliance และการบริหารผู้ใช้จำนวนมาก |
| ธุรกิจในกลุ่ม Regulated Industry (การเงิน, ประกันภัย, สุขภาพ) ที่ต้องมี Data Lineage/Audit Trail | 🔵 **Enterprise** ขึ้นไป | ฟีเจอร์ Governance ระดับ Enterprise มักเป็นข้อบังคับ ไม่ใช่ตัวเลือก |
| องค์กรที่ใช้ Salesforce อยู่แล้ว และต้องการ AI ช่วยวิเคราะห์แบบ Agentic เต็มรูปแบบ | 🟣 **Premium (Tableau+)** | ต่อยอด Data Cloud, ใช้ Tableau Agent/Agentforce ได้เต็มระบบ พร้อม Support ระดับสูงสุด |
| ทีมที่มีผู้ใช้ระดับ Viewer จำนวนมาก แต่ไม่แน่ใจจำนวนผู้ใช้ที่แน่นอน | ทุก Edition (เลือก **Capacity-based Licensing**) | จ่ายตามปริมาณการใช้งานพร้อมกัน แทนการนับจำนวนบัญชีผู้ใช้ |

---

## 💡 ประโยชน์ที่ได้รับในแต่ละระดับ

- **Standard** → เริ่มต้นเปลี่ยนข้อมูลเป็น Dashboard ที่ใช้งานได้จริงเร็วที่สุด ด้วยต้นทุนต่ำสุด เหมาะกับการพิสูจน์คุณค่า (Proof of Value) ก่อนขยายผล
- **Enterprise** → ลดความเสี่ยงด้าน Data Governance, ตรวจสอบย้อนหลังได้ (Audit Trail), บริหารจัดการผู้ใช้และเนื้อหาจำนวนมากอย่างเป็นระบบ
- **Premium** → เพิ่มความเร็วในการตัดสินใจด้วย AI ที่ตอบคำถามและแจ้งเตือนความผิดปกติแบบอัตโนมัติ ลดภาระการสร้าง Dashboard ด้วยมือ พร้อม Support ระดับสูงสุดเมื่อเกิดปัญหา

---

## ⚠️ ข้อควรรู้ก่อนตัดสินใจ

> [!WARNING]
> - **ไม่สามารถผสม Edition ได้ในองค์กรเดียว** — หากต้องการ Data Management สำหรับผู้ใช้บางกลุ่ม ต้องอัปเกรดผู้ใช้ทั้งหมดในระบบขึ้น Enterprise
> - **ต้นทุนซ่อนเร้น** — ค่าฝึกอบรม Creator, ค่า Infrastructure (กรณีเลือก Tableau Server แบบ Self-hosted), และค่า Implementation ควรถูกนำมารวมคำนวณ Total Cost of Ownership (TCO)
> - **สัญญารายปีเท่านั้น** — Tableau ไม่มีตัวเลือกจ่ายรายเดือน ทุกแพ็กเกจต้องทำสัญญาแบบรายปี
> - หากยังไม่พร้อมซื้อ License แบบทีม สามารถเริ่มต้นด้วย **Tableau Desktop Free Edition** เพื่อวิเคราะห์ไฟล์ในเครื่องก่อนได้ (ไม่รองรับการแชร์ผ่าน Cloud/Server)

---

## 📚 อ้างอิง

- [Tableau Pricing — tableau.com](https://www.tableau.com/pricing)
- [Tableau Cloud Pricing](https://www.tableau.com/pricing/cloud)
- [About Tableau Enterprise — Tableau Help](https://help.tableau.com/current/online/en-us/to_tab_enterprise_features.htm)
- [Understanding License Models — Tableau Help](https://help.tableau.com/current/online/en-us/license_product_keys.htm)
- [Tableau Blog: Expanding Access to Agentic Analytics](https://www.tableau.com/blog/tableau-agentic-analytics-pricing-updates)
- [About Data Management — Tableau Help](https://help.tableau.com/current/online/en-us/dm_overview.htm)
- [Advanced Management — tableau.com](https://www.tableau.com/products/advanced-management)
- [Tableau Pulse — tableau.com](https://www.tableau.com/products/tableau-pulse)
- [Tableau Pulse Release Notes — Tableau Help](https://help.tableau.com/current/online/en-us/pulse_intro.htm)
- [Tableau Agent — tableau.com](https://www.tableau.com/products/tableau-agent)
- [Tableau Agent FAQ — Tableau Help](https://help.tableau.com/current/online/en-us/web_author_einstein_faq.htm)
- [AI in Tableau and Trust — Tableau Help](https://help.tableau.com/current/tableau/en-us/tableau_gai_einstein_trust.htm)
- [Turn on AI in Tableau for your Site (Server) — Tableau Help](https://help.tableau.com/current/server-linux/en-us/sites_gai_server.htm)

---

*จัดทำเพื่อเผยแพร่ความรู้เกี่ยวกับ Tableau Editions — ข้อมูลราคาและฟีเจอร์อาจมีการเปลี่ยนแปลงตามประกาศของ Tableau/Salesforce กรุณาตรวจสอบกับ Partner ที่ได้รับการรับรองก่อนตัดสินใจซื้อจริง*

---

### 📖 อ่านต่อ

➡️ พร้อมเปิดใช้งานจริงแล้ว? ไปที่ [คู่มือเปิดใช้งาน Tableau Pulse & Tableau Agent](./02-tableau-pulse-agent-setup-guide-th.md)

🏠 [กลับหน้าแรก](./README.md)

# 📊 เปรียบเทียบ Tableau Editions: Standard vs Enterprise vs Premium (Cloud+ / Tableau+)

> คู่มือฉบับย่อ อธิบายความแตกต่างของแพ็กเกจ Tableau ในปี 2026 พร้อมคำแนะนำว่าองค์กรแบบไหนควรเลือกแพ็กเกจใด

[![Tableau](https://img.shields.io/badge/Tableau-2026-E97627?logo=tableau&logoColor=white)](https://www.tableau.com)
[![Language](https://img.shields.io/badge/ภาษา-ไทย-blue)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

---

## 📑 สารบัญ

- [ภาพรวม: Tableau มีอะไรให้เลือกบ้าง](#ภาพรวม-tableau-มีอะไรให้เลือกบ้าง)
- [ตารางเปรียบเทียบหลัก](#-ตารางเปรียบเทียบหลัก)
- [รายละเอียดแต่ละ Edition](#-รายละเอียดแต่ละ-edition)
  - [🟢 Standard Edition](#-standard-edition)
  - [🔵 Enterprise Edition](#-enterprise-edition)
  - [🟣 Premium (Cloud+ / Server+ / Tableau+ Bundle)](#-premium-cloud--server--tableau-bundle)
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
| **Tableau Agent** (AI สร้างกราฟด้วยภาษาธรรมชาติ) | ❌ | บางส่วน (ขึ้นกับ Deployment) | ✅ เต็มรูปแบบ |
| **Agentforce Skills** (Concierge, Inspector, Data Pro) | ❌ | ❌ | ✅ |
| **Data Cloud Credits** | ❌ | ❌ | ✅ (เช่น 250,000 เครดิต/ปี) |
| **eLearning** | ❌ | ✅ | ✅ |
| **ระดับ Support** | Standard Success | Standard Success + eLearning | Premier Success (24/7, ตอบเร็ว, มี TAM) |
| **Capacity-based Licensing (Viewer Block)** | ✅ | ✅ | ✅ |
| **เหมาะกับ** | ทีมเริ่มต้น/ขนาดกลาง | องค์กรขนาดใหญ่ที่ต้อง Governance | องค์กรที่ต้องการ AI เต็มรูปแบบ + Support สูงสุด |

> [!IMPORTANT]
> ราคาข้างต้นอ้างอิงจาก Tableau Cloud (ข้อมูลเปิดเผยต่อสาธารณะ กลางปี 2026) เป็น**ราคาโดยประมาณ** สำหรับใช้เปรียบเทียบเชิงโครงสร้างเท่านั้น ราคาจริงและเงื่อนไขสัญญาอาจเปลี่ยนแปลง ควรตรวจสอบกับ Tableau หรือ Partner ที่ได้รับการรับรองในประเทศไทยก่อนตัดสินใจซื้อ

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
- **Tableau Agent** — สร้างและวิเคราะห์ Visualization ด้วยภาษาธรรมชาติ (Powered by Einstein AI)
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

---

*จัดทำเพื่อเผยแพร่ความรู้เกี่ยวกับ Tableau Editions — ข้อมูลราคาและฟีเจอร์อาจมีการเปลี่ยนแปลงตามประกาศของ Tableau/Salesforce กรุณาตรวจสอบกับ Partner ที่ได้รับการรับรองก่อนตัดสินใจซื้อจริง*

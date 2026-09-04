# 📊 Tableau Editions & AI Features Guide (ภาษาไทย)

> คู่มือฉบับภาษาไทย อธิบายความแตกต่างของแพ็กเกจ Tableau (Standard / Enterprise / Premium) และวิธีเปิดใช้งานฟีเจอร์ AI อย่าง Tableau Pulse และ Tableau Agent ทั้งบน Cloud และ On-Premise

[![Tableau](https://img.shields.io/badge/Tableau-2026-E97627?logo=tableau&logoColor=white)](https://www.tableau.com)
[![Language](https://img.shields.io/badge/ภาษา-ไทย-blue)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

---

## 📂 เอกสารในชุดนี้

| # | เอกสาร | อ่านเรื่องอะไร | เหมาะกับใคร |
|---|---|---|---|
| 1️⃣ | **[เปรียบเทียบ Tableau Editions](./01-tableau-editions-comparison-th.md)** | Standard vs Enterprise vs Premium — ราคา, ฟีเจอร์, Data Management, Advanced Management, Tableau Pulse vs Pulse Premium, Tableau Agent | คนที่กำลังเลือกซื้อ/อัปเกรด Edition และต้องเปรียบเทียบงบประมาณกับฟีเจอร์ |
| 2️⃣ | **[คู่มือเปิดใช้งาน Tableau Pulse & Tableau Agent](./02-tableau-pulse-agent-setup-guide-th.md)** | ขั้นตอนเปิดใช้งานจริงทีละสเต็ป ทั้งบน Tableau Cloud และ Tableau Server (On-Premise) พร้อมลิงก์อ้างอิงทางการ | แอดมินระบบ / ผู้ดูแล Tableau ที่พร้อมเปิดใช้งานฟีเจอร์ AI ในองค์กรจริง |

> [!TIP]
> ถ้ายังไม่เคยใช้ Tableau Pulse/Agent มาก่อน แนะนำให้อ่าน **เอกสารที่ 1** เพื่อเข้าใจก่อนว่า Edition ไหนได้ฟีเจอร์อะไรบ้าง แล้วค่อยไปที่ **เอกสารที่ 2** เพื่อลงมือเปิดใช้งานจริง

---

## ⚡ สรุปแบบเร็ว (Quick Summary)

| หัวข้อ | 🟢 Standard | 🔵 Enterprise | 🟣 Premium (Tableau+) |
|---|---|---|---|
| ราคาเริ่มต้น (Creator) | ~$75/เดือน | ~$115/เดือน | ติดต่อฝ่ายขาย |
| Data Management / Advanced Management | ❌ | ✅ | ✅ |
| Tableau Pulse | ✅ (พื้นฐาน) | ✅ (พื้นฐาน) | ✅ + Pulse Premium |
| Tableau Agent (Cloud) | ❌ | ❌ | ✅ |
| Tableau Agent (Server/On-Premise) | ✅* | ✅* | ✅* |

\* บน Server ใช้ได้ทุก Edition ตั้งแต่เวอร์ชัน 2025.3 แต่ต้องเชื่อม LLM ของตัวเอง (OpenAI/Azure OpenAI) — รายละเอียดเต็มดูที่ [เอกสารที่ 1](./01-tableau-editions-comparison-th.md#-tableau-agent-คืออะไร)

👉 ดูตารางเปรียบเทียบแบบละเอียดทั้งหมดได้ที่ [เอกสารที่ 1: เปรียบเทียบ Tableau Editions](./01-tableau-editions-comparison-th.md#-ตารางเปรียบเทียบหลัก)

---

## 🗺️ แนะนำลำดับการอ่าน

```
README.md (หน้านี้)
   │
   ├──▶ 1️⃣ เปรียบเทียบ Editions ─────▶ เข้าใจว่า Edition ไหนเหมาะกับองค์กร
   │                                      │
   │                                      ▼
   └──▶ 2️⃣ คู่มือเปิดใช้งาน  ◀───────── พร้อมแล้ว เปิดใช้งานจริง
```

---

## 📄 License

เผยแพร่ภายใต้ [MIT License](https://opensource.org/licenses/MIT) — ใช้/แก้ไข/แชร์ต่อได้อย่างอิสระ พร้อมให้เครดิตแหล่งที่มา

> ข้อมูลราคาและฟีเจอร์ในเอกสารชุดนี้อ้างอิงจากข้อมูลเปิดเผยต่อสาธารณะของ Tableau/Salesforce ณ ปี 2026 อาจมีการเปลี่ยนแปลงได้ กรุณาตรวจสอบกับ Tableau หรือ Partner ที่ได้รับการรับรองก่อนตัดสินใจซื้อหรือดำเนินการจริง

---
---
title: "แท็กภาพ Docker ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
ArticleTitle: "แท็กภาพ Docker ของ Aspose.Cells Cloud"
linktitle: "แท็กภาพ"
type: docs
url: /docker/tag-list/
description: "ค้นหาแท็กภาพ Docker ล่าสุดของ Aspose.Cells Cloud สำหรับ Windows Server (2016‑2022) และ Linux รับคำสั่งดึงภาพ รายละเอียดสถาปัตยกรรม และบันทึกการอัปเกรดทั้งหมดในที่เดียว"
weight: 30
keywords:
  - "แท็กภาพ Docker ของ Aspose.Cells Cloud"
  - "คำสั่งดึงภาพ Docker"
  - "แท็ก Docker สำหรับ Windows Server"
  - "แท็ก Docker สำหรับ Linux"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud มีภาพ Docker ที่พร้อมใช้งานสำหรับ Windows Server (2016, 2019, 2022) และ Linux  
แต่ละภาพมีการระบุเวอร์ชันด้วย **แท็ก** ซึ่งระบุการวางเวอร์ชันผลิตภัณฑ์และระบบปฏิบัติการเป้าหมาย  
ใช้แท็กด้านล่างเพื่อดึงภาพที่คุณต้องการ และอ้างอิงตัวอย่างการดึงและรันภาพเพื่อเริ่มต้นใช้งานได้อย่างรวดเร็ว

*อัปเดตล่าสุด: 2026-07-01*

**ข้อกำหนดเบื้องต้น:** ตรวจสอบให้แน่ใจว่าได้ติดตั้ง Docker Engine เวอร์ชัน 20.10 หรือใหม่กว่า และคุณมีคีย์ใบอนุญาต Aspose.Cells Cloud ที่ถูกต้อง ภาพเหล่านี้ถูกสร้างขึ้นสำหรับ Windows Server เวอร์ชันที่ระบุหรือ Linux x64

## ภาพสำหรับ Windows Server 2016 ##

แท็ก | สถาปัตยกรรม | Dockerfile | หมายเหตุ
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile ไม่ได้เผยแพร่ – ดูรายละเอียดการสร้างได้จาก [บันทึกการปล่อยเวอร์ชัน](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016) | ไม่มีการวางแผนปล่อยแท็กใหม่สำหรับ Windows Server 2016; นี่คือเวอร์ชันสุดท้ายที่ปล่อยออกมา

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

ทรัพยากรเพิ่มเติม: [ดาวน์โหลด Docker](/cells/docker/downloads/), [บันทึกการปล่อยเวอร์ชัน](/cells/release-notes/), [ข้อกำหนดเบื้องต้น](/cells/docker/prerequisites/)  
ดูรายละเอียดเพิ่มเติมได้ที่ [ภาพรวม Docker](/cells/docker/)

## ภาพสำหรับ Windows Server 2019 ##

แท็ก | สถาปัตยกรรม | Dockerfile | หมายเหตุ
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile ไม่ได้เผยแพร่ – ดูรายละเอียดการสร้างได้จาก [บันทึกการปล่อยเวอร์ชัน](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019) | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

ทรัพยากรเพิ่มเติม: [ดาวน์โหลด Docker](/cells/docker/downloads/), [บันทึกการปล่อยเวอร์ชัน](/cells/release-notes/), [ข้อกำหนดเบื้องต้น](/cells/docker/prerequisites/)  
ดูรายละเอียดเพิ่มเติมได้ที่ [ภาพรวม Docker](/cells/docker/)

## ภาพสำหรับ Windows Server 2022 ##

แท็ก | สถาปัตยกรรม | Dockerfile | หมายเหตุ
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile ไม่ได้เผยแพร่ – ดูรายละเอียดการสร้างได้จาก [บันทึกการปล่อยเวอร์ชัน](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022) | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

ทรัพยากรเพิ่มเติม: [ดาวน์โหลด Docker](/cells/docker/downloads/), [บันทึกการปล่อยเวอร์ชัน](/cells/release-notes/), [ข้อกำหนดเบื้องต้น](/cells/docker/prerequisites/)  
ดูรายละเอียดเพิ่มเติมได้ที่ [ภาพรวม Docker](/cells/docker/)

## ภาพสำหรับ Linux ##

แท็ก | สถาปัตยกรรม | Dockerfile | หมายเหตุ
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile ไม่ได้เผยแพร่ – ดูรายละเอียดการสร้างได้จาก [บันทึกการปล่อยเวอร์ชัน](https://github.com/aspose-cells/dockerfiles/tree/main/linux) | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

ทรัพยากรเพิ่มเติม: [ดาวน์โหลด Docker](/cells/docker/downloads/), [บันทึกการปล่อยเวอร์ชัน](/cells/release-notes/), [ข้อกำหนดเบื้องต้น](/cells/docker/prerequisites/)  
ดูรายละเอียดเพิ่มเติมได้ที่ [ภาพรวม Docker](/cells/docker/)

**บันทึกการเปลี่ยนแปลงเวอร์ชัน**

แท็ก | การเปลี่ยนแปลง
---|---
`ltsc2016.23.5.0` | การปล่อยเวอร์ชันสุดท้ายสำหรับ Windows Server 2016; รวมแพตช์ด้านความปลอดภัยและการปรับปรุงประสิทธิภาพ
`ltsc2019.25.10.0` | อัปเดตเป็น Aspose.Cells เวอร์ชัน 25.10.0; เพิ่มการรองรับสูตรใหม่และแก้ไขข้อบกพร่อง
`ltsc2022.25.10.0` | เหมือนกับแท็ก 2019 แต่ปรับให้เหมาะสมกับ runtime ของ Windows Server 2022
`linux.25.10.0` | ภาพ Linux พื้นฐานพร้อม Aspose.Cells เวอร์ชัน 25.10.0; รวมการอัปเดต dependencies และการปรับแต่งเฉพาะสำหรับ Linux
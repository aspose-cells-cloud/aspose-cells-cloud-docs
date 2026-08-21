---
title: "เรียกใช้คอนเทนเดอร์ Docker ของ Aspose.Cells Cloud – ดึง, กำหนดค่า และเริ่มต้นใช้งาน"
second_title: "เอกสาร"
ArticleTitle: "วิธีการเรียกใช้คอนเทนเดอร์ Docker ของ Aspose.Cells Cloud"
LinkTitle: "คอนเทนเดอร์ Docker"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "เรียนรู้วิธีดึง กำหนดค่า และเรียกใช้คอนเทนเดอร์ Docker ของ Aspose.Cells Cloud บน Windows หรือ Linux รวมถึงไฟล์ YAML สำหรับ Docker Compose การตั้งค่าใบอนุญาต การแมปพอร์ต และเคล็ดลับในการแก้ไขปัญหา"
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker container"
  - "Docker Compose"
  - "license keys"
  - "Excel"
  - "spreadsheet"
  - "cloud API"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

เทคโนโลยี Docker ถูกออกแบบมาเพื่อจัดการกับการปรับใช้แอปพลิเคชันโดยใช้คอนเทนเดอร์ที่มีน้ำหนักเบา นักพัฒนาสามารถใช้คอนเทนเดอร์ Docker เพื่อห่อแอปพลิเคชันพร้อมไลบรารีและไดเรกทอรีที่จำเป็นทั้งหมด แล้วปรับใช้เป็นแพ็กเกจเดียว

ทีมงาน Aspose.Cells Cloud ได้เผยแพร่คอนเทนเดอร์ Docker บน <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> เพื่อความสะดวกให้กับผู้ใช้ Docker

**ข้อกำหนดเบื้องต้น** – ตรวจสอบให้แน่ใจว่า Docker Engine เวอร์ชัน ≥ 20.x ถูกติดตั้งแล้ว และระบบปฏิบัติการของคุณ (Windows 10/Server 2019/2022 หรือการแจกจ่าย Linux ที่รองรับ) มีความเหมาะสม คุณสามารถระบุคีย์ใบอนุญาตเพิ่มเติมเพื่อใช้งานในโหมดใบอนุญาต

- Docker Engine ≥ 20.x ติดตั้งแล้ว  
- ระบบปฏิบัติการที่รองรับ (Windows 10/Server 2019/2022 หรือการแจกจ่าย Linux)  
- คีย์ใบอนุญาต (ไม่บังคับ) เพื่อใช้งานในโหมดใบอนุญาต  

## การกำหนดค่าคอนเทนเดอร์

### ไดเรกทอรีที่ต้องมี (volumes)

| พาธที่เมานต์ในคอนเทนเดอร์ | คำอธิบาย |
| :--- | :--- |
| C:\fonts | โฟลเดอร์ที่มีฟอนต์ที่จะใช้ในการเรนเดอร์เอกสาร |
| C:\data | โฟลเดอร์เก็บไฟล์ |

**ทางเลือกสำหรับ Linux/macOS** – ใช้ `/fonts` และ `/data` ภายในคอนเทนเดอร์ และแมปไปยังไดเรกทอรีบนเครื่องโฮสต์ เช่น `/home/user/fonts` และ `/home/user/data` เมื่อรันคอนเทนเดอร์

### พารามิเตอร์

| ชื่อ | คำอธิบาย |
| :--- | :--- |
| LicensePublicKey | คีย์สาธารณะของใบอนุญาต |
| LicensePrivateKey | คีย์ส่วนตัวของใบอนุญาต |

หากไม่ระบุพารามิเตอร์ **License** แอปพลิเคชันจะทำงานในโหมดทดลองใช้งาน

### 1. ดึงอิมเมจของ Aspose.Cells Cloud

```bash
# ดึงเวอร์ชันเฉพาะของอิมเมจ Aspose.Cells Cloud
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# ดึงอิมเมจ Aspose.Cells Cloud สำหรับ Windows Server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# ดึงอิมเมจ Aspose.Cells Cloud สำหรับ Windows Server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# ดึงอิมเมจ Aspose.Cells Cloud สำหรับ Windows 11
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **หมายเหตุ:** หากต้องการรับเวอร์ชันล่าสุดอยู่เสมอ คุณยังสามารถดึงแท็ก `latest` ได้ด้วยคำสั่ง: `docker pull aspose/cells-cloud:latest`

### 2. การกำหนดค่าสำหรับเครื่องมือ Docker‑Compose

คุณสามารถเขียนการกำหนดค่าต่อไปนี้ลงในไฟล์ **docker‑compose.yml**:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # พอร์ตโฮสต์ 5000 → คอนเทนเดอร์ 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **หมายเหตุ:** การแมปพอร์ต `5000:80` หมายความว่า API จะเข้าถึงได้ที่ `http://localhost:5000`

### 3. เรียกใช้คอนเทนเดอร์ Docker ผ่านบรรทัดคำสั่ง

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**การแก้ไขปัญหา:**  
- **พอร์ตขัดแย้ง:** ตรวจสอบให้แน่ใจว่าพอร์ต 5000 บนเครื่องโฮสต์ว่างอยู่ หรือเปลี่ยนการแมปไปยังพอร์ตที่ไม่ได้ใช้งาน  
- **การโหลดใบอนุญาตล้มเหลว:** ตรวจสอบให้แน่ใจว่าคีย์สาธารณะและส่วนตัวถูกส่งผ่านเป็นตัวแปรสภาพแวดล้อมหรือเมานต์เป็นไฟล์อย่างถูกต้อง  
- **ไม่มีฟอนต์:** หากเอกสารถูกเรนเดอร์ด้วยฟอนต์ที่ไม่ถูกต้อง ให้ตรวจสอบว่าไดเรกทอรีฟอนต์ถูกเมานต์อย่างถูกต้องและมีไฟล์ฟอนต์ที่จำเป็นอยู่  

**ทรัพยากรที่เกี่ยวข้อง:**  
- <a href="/cells/api/">เอกสารอ้างอิง API</a> | <a href="/cells/license/">คู่มือการเปิดใช้งานใบอนุญาต</a> | <a href="/cells/getting-started/">ภาพรวมการเริ่มต้นใช้งาน</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Run Aspose.Cells Cloud Docker Container",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "ดึงอิมเมจ Docker",
      "text": "รันคำสั่ง `docker pull aspose/cells-cloud:<version>` เพื่อดาวน์โหลดอิมเมจที่จำเป็น"
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "สร้างไฟล์ docker‑compose",
      "text": "กำหนดอิมเมจ พอร์ต ไดเรกทอรีที่เมานต์ และตัวแปรสภาพแวดล้อมสำหรับใบอนุญาตในไฟล์ `docker‑compose.yml`"
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "เรียกใช้คอนเทนเดอร์",
      "text": "รันคำสั่ง `docker run` พร้อมตัวแปรสภาพแวดล้อม การเมานต์ไดเรกทอรี และการแมปพอร์ตที่เหมาะสม"
    }
  ]
}
```
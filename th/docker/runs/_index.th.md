---
title: "วิธีการรันคอนเทนเดอร์ Docker ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
ArticleTitle: "วิธีการรันคอนเทนเดอร์ Docker ของ Aspose.Cells Cloud"
linktype: "รันคอนเทนเดอร์"
type: docs
url: /run-aspose-cells-cloud-docker-container/
description: "เรียนรู้วิธีการเปิดใช้งาน Aspose.Cells Cloud ในคอนเทนเดอร์ Docker บน Windows Server 2022 ด้วยคำสั่งแบบทีละขั้นตอนสำหรับโหมดทดลองใช้งาน การเรียกเก็บเงินแบบใช้งานจริง (metered billing) การเรียกเก็บเงินแบบใบอนุญาต (license billing) การตั้งค่าที่จัดเก็บข้อมูล และการตรวจสอบสุขภาพของระบบ"
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, โหมดทดลองใช้งาน, การเรียกเก็บเงินแบบใช้งานจริง, การเรียกเก็บเงินแบบใบอนุญาต, การกำหนดค่าที่จัดเก็บข้อมูล"
---

Aspose.Cells Cloud Docker จัดเตรียมภาพคอนเทนเดอร์ที่พร้อมใช้งานเพื่อโฮสต์ API ของ Aspose.Cells Cloud แบบโลคัลหรือในคลาวด์ส่วนตัว คู่มือนี้แสดงวิธีการเริ่มคอนเทนเดอร์ในสามโหมดการเรียกเก็บเงินที่พบบ่อย ได้แก่ **โหมดทดลองใช้งาน**, **การเรียกเก็บเงินแบบใช้งานจริง** และ **การเรียกเก็บเงินแบบใบอนุญาต** พร้อมทั้งตัวเลือกที่ใช้โทเค็นการเข้าถึง (access token) คำสั่งทั้งหมดเขียนสำหรับ PowerShell บน Windows Server 2022 หากคุณใช้ Linux ให้ปรับเส้นทางโฟลเดอร์ที่ใช้เชื่อมต่อ (volume path) ให้เหมาะสม

**ข้อกำหนดเบื้องต้น**

- Docker Engine เวอร์ชัน 20.10 หรือใหม่กว่า ติดตั้งและรันอยู่  
- PowerShell เวอร์ชัน 5.1 หรือ PowerShell 7+  
- เปิดพอร์ต 5000 ภายในคอนเทนเดอร์ (แมปกับพอร์ตโฮสต์ 47900) และให้แน่ใจว่าไฟร์วอลล์ของโฮสต์อนุญาตให้รับข้อมูลเข้าผ่านพอร์ต 47900  
- สำหรับโหมดการเรียกเก็บเงินแบบใช้งานจริงหรือแบบใบอนุญาต ให้เตรียม `LicensePublicKey`, `LicensePrivateKey` หรือไฟล์ใบอนุญาตไว้ หรือเตรียม `AccessToken` หากใช้โหมดโทเค็น  
- มีโฟลเดอร์ในเครื่อง (เช่น `C:\data`) ที่จะใช้เชื่อมต่อเป็นพื้นที่จัดเก็บข้อมูลสำหรับคอนเทนเดอร์

**เริ่มต้นอย่างรวดเร็ว (โหมดทดลองใช้งาน)**  

รันคำสั่งต่อไปนี้เพื่อเริ่มคอนเทนเดอร์ในโหมดทดลองใช้งาน:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## รันคอนเทนเดอร์ Docker ของ Aspose.Cells Cloud ในโหมดทดลองใช้งาน

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

คอนเทนเดอร์จะรันแบบ foreground และรับฟังบนพอร์ตโฮสต์ **47900** ซึ่งจะส่งต่อไปยังพอร์ตภายในของคอนเทนเดอร์ **5000**

## รันคอนเทนเดอร์ Docker ของ Aspose.Cells Cloud ในโหมดการเรียกเก็บเงินแบบใช้งานจริง

```powershell
# Windows Server 2022
# โหมดการเรียกเก็บเงินแบบใช้งานจริง: ตั้งค่า LicensePublicKey และ LicensePrivateKey ให้เป็นตัวแปรสภาพแวดล้อม
# ใช้การเชื่อมต่อโฟลเดอร์ที่จัดเก็บข้อมูล (โฮสต์ → คอนเทนเดอร์)
#   -v c:/data:c:/data
# ใช้การเชื่อมต่อโฟลเดอร์ฟอนต์ของ Windows เพื่อให้ API สามารถเข้าถึงฟอนต์ของระบบได้
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

คอนเทนเดอร์จะรันแบบ detached mode (`-d`) หลังจากเริ่มต้นแล้ว คุณสามารถตรวจสอบได้ว่าบริการสามารถเข้าถึงได้หรือไม่ด้วยคำสั่ง:

```powershell
curl http://localhost:47900/v3.0/health
```

**ตัวอย่างไฟล์ `storageResource.json`**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## รันคอนเทนเดอร์ Docker ของ Aspose.Cells Cloud ในโหมดการเรียกเก็บเงินแบบใบอนุญาต

```powershell
# Windows Server 2022
# โหมดการเรียกเก็บเงินแบบใบอนุญาต: ระบุไฟล์ใบอนุญาตผ่านตัวแปรสภาพแวดล้อม LicenseFile
# ใช้การเชื่อมต่อโฟลเดอร์ที่จัดเก็บข้อมูล (โฮสต์ → คอนเทนเดอร์)
#   -v c:/data:c:/data
# ใช้การเชื่อมต่อโฟลเดอร์ฟอนต์ของ Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## รันคอนเทนเดอร์ Docker ของ Aspose.Cells Cloud ด้วยโทเค็นการเข้าถึง

```powershell
# Windows Server 2022
# โหมดโทเค็นการเข้าถึง: ตั้งค่า AccessToken ร่วมกับคีย์สำหรับการเรียกเก็บเงินแบบใช้งานจริง (ถ้ามี)
# ใช้การเชื่อมต่อโฟลเดอร์ที่จัดเก็บข้อมูล
#   -v c:/data:c:/data
# ใช้การเชื่อมต่อโฟลเดอร์ฟอนต์ของ Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

หลังจากเริ่มคอนเทนเดอร์แล้ว ให้ยืนยันว่าบริการใช้งานได้โดยใช้คำสั่งตรวจสอบสุขภาพเดียวกับที่แสดงไว้ก่อนหน้านี้

## เอกสารอ้างอิง

- [วิธีการกำหนดค่าที่จัดเก็บข้อมูลของคอนเทนเดอร์ Docker Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/storage/)

---

### การแก้ไขปัญหา

- **การตรวจสอบสุขภาพล้มเหลว** – ตรวจสอบว่าพอร์ต 47900 ไม่ได้ถูกบล็อกโดยไฟร์วอลล์ และคอนเทนเดอร์กำลังรันอยู่ (`docker ps`)  
- **ข้อผิดพลาดเกี่ยวกับใบอนุญาต** – ตรวจสอบให้แน่ใจว่าค่าของ `LicensePublicKey`, `LicensePrivateKey` หรือ `LicenseFile` ถูกต้อง และตัวแปรสภาพแวดล้อมถูกส่งผ่านโดยไม่มีช่องว่างเกิน  
- **ที่จัดเก็บข้อมูลเข้าถึงไม่ได้** – ตรวจสอบให้แน่ใจว่าโฟลเดอร์บนโฮสต์ (`c:/data`) มีอยู่จริง และ Docker มีสิทธิ์ในการอ่าน/เขียนข้อมูลในโฟลเดอร์นี้

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "วิธีการรันคอนเทนเดอร์ Docker ของ Aspose.Cells Cloud",
  "description": "คู่มือแบบทีละขั้นตอนสำหรับการเปิดใช้งาน Aspose.Cells Cloud ในคอนเทนเดอร์ Docker บน Windows Server 2022 ครอบคลุมโหมดทดลองใช้งาน การเรียกเก็บเงินแบบใช้งานจริง การเรียกเก็บเงินแบบใบอนุญาต และโหมดโทเค็นการเข้าถึง",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, โหมดทดลองใช้งาน, การเรียกเก็บเงินแบบใช้งานจริง, การเรียกเก็บเงินแบบใบอนุญาต, การกำหนดค่าที่จัดเก็บข้อมูล"
}
</script>
---
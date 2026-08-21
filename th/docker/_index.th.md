---
title: "คู่มือการใช้งาน Aspose.Cells Cloud บน Docker: โฮสต์แอปพลิเคชัน Aspose.Cells Cloud บนโครงสร้างพื้นฐานส่วนตัวของคุณ"
second_title: "เอกสาร"
ArticleTitle: "คู่มือการใช้งาน Aspose.Cells Cloud บน Docker"
linktype: "docs"
url: /docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: "ปรับใช้ Aspose.Cells Cloud ในรูปแบบคอนเทนเนอร์ Docker บนโครงสร้างพื้นฐานแบบส่วนตัวหรือแบบติดตั้งภายในองค์กร ช่วยให้สามารถประมวลผลไฟล์สเปรดชีต (Excel, PDF, CSV, JSON, Markdown) โดยไม่ต้องใช้คลาวด์สาธารณะของ Aspose"
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Docker Image",
    "Spreadsheet API",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Private Cloud",
    "Deployment",
  ]
weight: 30
---

Aspose.Cells Cloud เป็นบริการประมวลผลสเปรดชีตที่ทำงานบนคลาวด์ รองรับการสร้าง แก้ไข แปลง และจัดการไฟล์ในรูปแบบต่างๆ เช่น Excel คุณสามารถติดตั้งบริการนี้เป็นสภาพแวดล้อมอิสระได้อย่างรวดเร็วด้วยการปรับใช้ผ่าน Docker ซึ่งช่วยลดความซับซ้อนในการจัดการการพึ่งพา (dependency) และการปรับใช้งานข้ามแพลตฟอร์ม

คู่มือนี้จะอธิบายขั้นตอนการดำเนินการทั้งหมดอย่างละเอียด ตั้งแต่การเตรียมสภาพแวดล้อม ไปจนถึงการตรวจสอบการทำงานของบริการ

## การเตรียมสภาพแวดล้อม

ก่อนที่จะปรับใช้คอนเทนเนอร์ Docker ของ Aspose.Cells Cloud คุณต้องตรวจสอบให้แน่ใจว่าสภาพแวดล้อมในเครื่องของคุณตรงตามข้อกำหนดการพึ่งพาต่อไปนี้ เพื่อหลีกเลี่ยงความล้มเหลวในการปรับใช้งานเนื่องจากส่วนประกอบที่ขาดหาย

### ส่วนประกอบการพึ่งพาขั้นพื้นฐาน

- **Docker Engine:** แกนหลักของโปรแกรมรันไทม์สำหรับคอนเทนเนอร์ ซึ่งรับผิดชอบในการสร้างและจัดการคอนเทนเนอร์ ต้องมีเวอร์ชันขั้นต่ำ **18.09.0**
- **ระบบปฏิบัติการ:** ระบบปฏิบัติการหลักที่รองรับ Docker

  | ประเภทระบบปฏิบัติการ | เวอร์ชัน                   |
  | :-------------------- | :------------------------ |
  | Windows               | Windows 10/11             |
  | Windows Server        | 2016 / 2019 / 2022        |
  | Linux                 | CentOS 7+ / Ubuntu 20.04+ |

- **ทรัพยากรฮาร์ดแวร์:** ตรวจสอบให้แน่ใจว่ามีทรัพยากรเพียงพอเพื่อให้บริการทำงานได้อย่างราบรื่น และหลีกเลี่ยงการหยุดทำงานเนื่องจากทรัพยากรไม่เพียงพอ
  - CPU: 2 คอร์ขึ้นไป
  - หน่วยความจำ: 4 GB ขึ้นไป
  - ดิสก์: พื้นที่ว่าง 10 GB

### เงื่อนไขที่จำเป็นก่อนเริ่มต้น

- **ใบอนุญาต Aspose:** ลงทะเบียนบัญชีกับ Aspose อย่างเป็นทางการเพื่อรับใบอนุญาตที่ถูกต้อง (คุณสามารถขอใช้งานเวอร์ชันทดลองใช้ หรือซื้อเวอร์ชันเชิงพาณิชย์) หากไม่มีใบอนุญาต ฟังก์ชันการทำงานของบริการอาจถูกจำกัด กรุณาดูรายละเอียดเพิ่มเติมที่หน้า [ใบอนุญาต](https://purchase.aspose.com/buy)
- **การเชื่อมต่อเครือข่าย:** ตรวจสอบให้แน่ใจว่าสภาพแวดล้อมที่ใช้ปรับใช้งานสามารถเข้าถึง Docker Hub (เพื่อดึงอิมเมจ)

## รับอิมเมจ Docker ของ Aspose.Cells Cloud

อิมเมจของ Aspose.Cells Cloud ถูกจัดเก็บไว้ที่ Docker Hub และสามารถดึงมาใช้งานได้โดยตรงผ่านคำสั่ง `docker pull` โดยไม่จำเป็นต้องสร้างเอง

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## การรันคอนเทนเนอร์ Aspose.Cells Cloud Docker

### พารามิเตอร์ในการรัน

| ชื่อพารามิเตอร์            | คำอธิบาย                                                                                   | หมายเหตุ                                                      |
| --------------------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------ |
| LicensePublicKey            | ตั้งค่าคีย์สาธารณะของใบอนุญาตเมื่อใช้โหมดการเรียกเก็บเงินแบบ Metered                      | ใช้งานได้เฉพาะเมื่อใช้โหมดการเรียกเก็บเงินแบบ Metered        |
| LicensePrivateKey           | ตั้งค่าคีย์ส่วนตัวของใบอนุญาตเมื่อใช้โหมดการเรียกเก็บเงินแบบ Metered                      | ใช้งานได้เฉพาะเมื่อใช้โหมดการเรียกเก็บเงินแบบ Metered        |
| storagesCredentialsFilePath | ตำแหน่งไฟล์การกำหนดค่าหน่วยจัดเก็บข้อมูล ไฟล์เริ่มต้นคือ `./storageResource.json`         |                                                              |
| LicenseFile                 | ตั้งค่าไฟล์ใบอนุญาตเมื่อใช้โหมดการเรียกเก็บเงินแบบ LicenseFile                           | ใช้งานได้เฉพาะเมื่อใช้โหมดการเรียกเก็บเงินแบบ LicenseFile    |
| AccessToken                 | โทเคนสำหรับการเข้าถึง API                                                                 | หากไม่ระบุ (ว่างเปล่า) จะไม่ต้องตรวจสอบโทเคน               |

### คำสั่งในการรัน

การรันคอนเทนเนอร์ในโหมดทดลองใช้มีความง่ายดายดังนี้:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

สำหรับการใช้งานแบบเต็มรูปแบบ คุณควรขอ [ใบอนุญาตแบบ Metered](https://purchase.aspose.com/faqs/licensing/metered/) และติดตั้งโฟลเดอร์จัดเก็บไฟล์จากเครื่องแม่ข่าย ตัวอย่างคำสั่งในการรันในกรณีนี้มีดังนี้:

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### อ้างอิง API – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### พอร์ตที่เปิดใช้งาน

| พอร์ต | คำอธิบาย                                     | จำเป็น |
| ----- | -------------------------------------------- | ------ |
| 5000  | โฟลเดอร์ที่เก็บฟอนต์ที่ใช้ในการเรนเดอร์เอกสาร | ใช่    |

### โฟลเดอร์ที่ต้องเมานต์ (Volumes)

| ตำแหน่งเมานต์ในคอนเทนเนอร์ | คำอธิบาย                                     | จำเป็น | หมายเหตุ                                                        |
| --------------------------- | -------------------------------------------- | ------ | --------------------------------------------------------------- |
| C:\fonts                    | โฟลเดอร์ที่เก็บฟอนต์ที่ใช้ในการเรนเดอร์เอกสาร | ไม่จำเป็น | ช่วยแก้ปัญหาสเปรดชีต/Excel ที่เกิดจากฟอนต์ที่ขาดหายไป        |
| C:\data                     | โฟลเดอร์จัดเก็บไฟล์                         | ไม่จำเป็น | เพิ่มพื้นที่จัดเก็บสำหรับจัดการและเข้าถึงไฟล์ได้ง่ายขึ้น       |

## เอกสารอ้างอิง

- [ฟังก์ชันหลักของคอนเทนเนอร์ Aspose.Cells Cloud Docker](https://docs.aspose.cloud/cells/docker-container-features/)
- [วิธีการตั้งค่าหน่วยจัดเก็บข้อมูลสำหรับคอนเทนเนอร์ Aspose.Cells Cloud Docker](https://docs.aspose.cloud/cells/docker/storage/)
- [วิธีการรันคอนเทนเนอร์ Aspose.Cells Cloud Docker](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
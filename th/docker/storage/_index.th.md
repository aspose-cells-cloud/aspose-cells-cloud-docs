---
title: "วิธีตั้งค่าตำแหน่งที่จัดเก็บข้อมูลสำหรับคอนเทนเนอร์ Docker ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
ArticleTitle: "การกำหนดค่าที่จัดเก็บข้อมูลคอนเทนเนอร์ Docker ของ Aspose.Cells Cloud"
linktype: "docs"
url: /th/docker/storage/
description: "กำหนดค่าตำแหน่งที่จัดเก็บข้อมูลสำหรับคอนเทนเนอร์ Docker ของ Aspose.Cells Cloud โดยใช้ไฟล์การกำหนดค่า JSON, PowerShell หรือ Bash"
weight: 30
keywords: "Aspose.Cells, Docker, container storage, การกำหนดค่า JSON, PowerShell, Bash"
---

**สรุป**: คู่มือนี้แสดงวิธีการกำหนดค่าตำแหน่งที่จัดเก็บข้อมูลสำหรับคอนเทนเนอร์ Docker ของ Aspose.Cells Cloud บนระบบ Windows และ Linux โดยใช้ไฟล์การกำหนดค่า JSON และคำสั่ง Docker run

## การกำหนดค่าที่จัดเก็บข้อมูลเริ่มต้น ##

**ข้อกำหนดเบื้องต้น**: ตรวจสอบให้แน่ใจว่าติดตั้ง Docker Engine เวอร์ชัน 20.10 ขึ้นไปแล้ว มีคีย์ใบอนุญาต Aspose.Cells Cloud ที่ถูกต้อง (`LicensePublicKey` และ `LicensePrivateKey`) และโฟลเดอร์บนโฮสต์ที่คุณต้องการใช้เป็นพื้นที่จัดเก็บข้อมูล (เช่น `c:/data` บน Windows หรือ `/data` บน Linux) มีอยู่แล้วและมีสิทธิ์การเข้าถึงที่เหมาะสม

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## ตำแหน่งเริ่มต้น ##

- **windows**

```powershell
c:\app\storageResource.json
```

- **linux**

```bash
/app/storageResource.json
```

## การกำหนดค่าที่จัดเก็บข้อมูลแบบกำหนดเอง ##

ระบุโปรไฟล์ที่จัดเก็บข้อมูลแบบกำหนดเองเมื่อคุณต้องการใช้โฟลเดอร์อื่นสำหรับข้อมูลของ Aspose.Cells Cloud

```bash
docker run -d \
  -v c:/data:c:/data \   # ผูกเชื่อมโยงโฟลเดอร์บนโฮสต์เป็นพื้นที่จัดเก็บข้อมูลของคอนเทนเนอร์
  -p 47900:5000 \        # แมปพอร์ต API
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*ตัวอย่างบน Linux*:

```bash
docker run -d \
  -v /data:/data \   # ผูกเชื่อมโยงโฟลเดอร์บนโฮสต์เป็นพื้นที่จัดเก็บข้อมูลของคอนเทนเนอร์
  -p 47900:5000 \    # แมปพอร์ต API
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**เอกสารอ้างอิง**:

- [วิธีการรันคอนเทนเนอร์ Docker ของ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [คุณสมบัติของคอนเทนเนอร์ Docker](https://docs.aspose.cloud/cells/docker/container-features/)
- [การดาวน์โหลดภาพ Docker ของ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/download-image/)
- [การจัดการแท็กของคอนเทนเนอร์](https://docs.aspose.cloud/cells/docker/manage-tags/)
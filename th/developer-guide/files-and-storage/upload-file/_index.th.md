---
title: "API อัปโหลดไฟล์ของ Aspose.Cells Cloud – อินเทอร์เฟซสำหรับการอัปโหลดไฟล์อย่างรวดเร็วลงในคลาวด์"
second_title: "เอกสาร"
ArticleTitle: "API อัปโหลดไฟล์ของ Aspose.Cells Cloud – อินเทอร์เฟซสำหรับการอัปโหลดไฟล์อย่างรวดเร็วลงในคลาวด์"
linktitle: "อัปโหลดไฟล์"
type: docs
url: /th/upload-file/
keywords: "Aspose.Cells, การอัปโหลดไฟล์, Excel API, พื้นที่จัดเก็บข้อมูลบนคลาวด์, REST API"
description: "คู่มือการอัปโหลดไฟล์ด้วย Aspose.Cells Cloud API ครอบคลุมพารามิเตอร์คำขอ, โค้ดสถานะ HTTP, การจัดการข้อผิดพลาด และตัวอย่างโค้ด"
weight: 100
---

**API อัปโหลดไฟล์ (uploadFile)** ช่วยให้นักพัฒนาสามารถอัปโหลดไฟล์ไปยังพื้นที่จัดเก็บข้อมูลบนคลาวด์โดยตรงเพื่อนำไปประมวลผลด้วย Aspose Cells

## **Aspose Cells API: อัปโหลดไฟล์**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเค็น JWT</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์คำขอของ **uploadFile** API มีดังนี้

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | Path/Query String/HTTP Body | คำอธิบาย                                                                                     |
| :------------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------- |
| UploadFiles    | ไฟล์   | FormData                    | อัปโหลดไฟล์ไปยังพื้นที่จัดเก็บข้อมูลบนคลาวด์                                               |
| path           | สตริง | Path                        | เส้นทางปลายทางในพื้นที่จัดเก็บข้อมูลบนคลาวด์ ระบุเส้นทางที่ไฟล์จะถูกอัปโหลด                 |
| storageName    | สตริง | Query                       | ชื่อของพื้นที่จัดเก็บข้อมูลที่ไฟล์จะถูกอัปโหลด                                               |

### **การตอบกลับ**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["ผลลัพธ์ของการอัปโหลดไฟล์"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["รายชื่อไฟล์ที่อัปโหลดแล้ว"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["รายชื่อข้อผิดพลาด"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

API จะส่งกลับโค้ดสถานะ HTTP ดังนี้:

| โค้ดสถานะ                      | คำอธิบาย                                               |
| ----------------------------- | ----------------------------------------------------- |
| **200 OK**                    | อัปโหลดไฟล์เรียบร้อยแล้ว                              |
| **400 Bad Request**           | พารามิเตอร์ไม่ถูกต้องหรือคำขอมีรูปแบบผิดพลาด         |
| **401 Unauthorized**          | ไม่มีโทเค็นการรับรองความถูกต้องหรือโทเค็นไม่ถูกต้อง   |
| **403 Forbidden**             | ไม่มีสิทธิ์เพียงพอสำหรับพื้นที่จัดเก็บข้อมูลที่ระบุ     |
| **500 Internal Server Error** | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์อย่างไม่คาดคิด          |

## วิธีการใช้ API อัปโหลดไฟล์ผ่าน SDK

### ข้อมูลจำเพาะ OpenAPI

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) มีคำอธิบายโดยละเอียดของ API ช่วยให้นักพัฒนาสามารถเรียกใช้งาน API ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK จะช่วยเพิ่มประสิทธิภาพการพัฒนา เนื่องจากจัดการรายละเอียดระดับล่างให้โดยอัตโนมัติ ช่วยให้นักพัฒนาสามารถมุ่งเน้นไปที่งานหลักของโปรเจกต์ได้ โปรดเยี่ยมชม [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud อย่างครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้งานบริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**ดูเพิ่มเติม**

- [API ดาวน์โหลดไฟล์](/download-file/) – ดึงไฟล์จากพื้นที่จัดเก็บข้อมูลบนคลาวด์
- [API คัดลอกไฟล์](/copy-file/) – คัดลอกไฟล์ภายในพื้นที่จัดเก็บข้อมูลบนคลาวด์
- [API ลบไฟล์](/delete-file/) – ลบไฟล์ออกจากพื้นที่จัดเก็บข้อมูลบนคลาวด์

---
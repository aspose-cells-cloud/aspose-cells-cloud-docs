---
title: "รับจำนวนหน้าจากไฟล์ Excel"
second_title: "เอกสาร"
linktype: "หน้า"
type: docs
url: /th/get-page-count-from-an-excel-file/
aliases: [  /th/workbook/page-count/ , /th/workbook/get/page-count/ ]
keywords: "Aspose.Cells, API บนคลาวด์, จำนวนหน้าของ Excel, การแบ่งหน้าในสมุดงาน"
description: "ดึงจำนวนหน้าที่สามารถพิมพ์ได้ทั้งหมดในสมุดงาน Excel ผ่าน Aspose.Cells Cloud REST API (v3.0) ประกอบด้วยรูปแบบคำขอ พารามิเตอร์ที่จำเป็น ตัวอย่าง cURL โครงสร้างการตอบกลับ การจัดการข้อผิดพลาด และตัวอย่างโค้ด SDK สำหรับหลายภาษา"
weight: 10
version: "v3.0"
ArticleTitle: "รับจำนวนหน้าจากไฟล์ Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้จะส่งคืน **จำนวนหน้า** ของสมุดงาน

## ความปลอดภัยและการพิสูจน์ตัวตน
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การพิสูจน์ตัวตนด้วย JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง | จำเป็น | คำอธิบาย                                   |
| ---------------- | ----------- | -------- | ------ | ------------------------------------------ |
| name             | string      | path     | ใช่    | ชื่อของเอกสาร Excel                        |
| folder           | string      | query    | ไม่จำเป็น | โฟลเดอร์ที่เก็บเอกสารไว้                   |
| storageName      | string      | query    | ไม่จำเป็น | ชื่อของพื้นที่จัดเก็บที่ต้องการใช้งาน       |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) กำหนด API แบบโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึง Aspose.Cells REST API ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้จุดปลายทางด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/YourFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*แทน `YourFile.xlsx` ด้วยชื่อสมุดงานที่คุณต้องการสอบถาม*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### โครงสร้างการตอบกลับ

| สถานะ HTTP | ประเภทข้อมูล | คำอธิบาย                                         |
| ---------- | ----------- | ------------------------------------------------ |
| 200        | integer     | จำนวนหน้าที่สามารถพิมพ์ได้ทั้งหมดในสมุดงาน (เช่น `13`) |
| 4xx‑5xx    | JSON        | วัตถุข้อผิดพลาด (ดูส่วน _การจัดการข้อผิดพลาด_)      |

## ครอบครัวของ Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## การจัดการข้อผิดพลาด

| สถานะ HTTP | คำอธิบาย                                     | ตัวอย่าง JSON Body                                                                          |
| ---------- | ------------------------------------------- | ------------------------------------------------------------------------------------------ |
| 401        | JWT token ไม่ถูกต้องหรือขาดหาย               | `{ "Code": "InvalidAuthenticationToken", "Message": "Access token is missing or invalid." }` |
| 404        | ไม่พบสมุดงานที่ระบุ                          | `{ "Code": "FileNotFound", "Message": "The requested file does not exist." }`               |
| 400        | คำขอไม่ถูกต้อง – ขาดพารามิเตอร์ที่จำเป็น    | `{ "Code": "BadRequest", "Message": "Required parameter 'name' is missing." }`             |
| 500        | ข้อผิดพลาดภายในเซิร์ฟเวอร์                   | `{ "Code": "InternalError", "Message": "An unexpected error occurred." }`                  |
---
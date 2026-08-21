---
title: "นำเข้าอาเรย์สตริง 2 มิติลงในเวิร์กชีต Excel"
second_title: "เอกสาร"
linktitle: "นำเข้าอาเรย์สตริง 2 มิติ"
type: docs
url: /th/import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-string-array-into-excel-worksheet/",
    "/import-2dimension-string-array-into-worksheet/",
    "/import-data/-2dimension-string-array/",
    "/import-data/2dimension-string-array/",
    "/import/2dimension-string-array/",
  ]
keywords: "Aspose.Cells Cloud, นำเข้าอาเรย์สตริง 2 มิติ, Excel, REST API, SDK"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อนำเข้าอาเรย์สตริงสองมิติลงในเวิร์กชีต Excel รวมถึงรูปแบบคำขอ รายละเอียดพารามิเตอร์ และตัวอย่างโค้ด SDK สำหรับ C#, PHP และ Ruby"
weight: 20
---

REST API นี้ **นำเข้าอาเรย์สตริงสองมิติ** ลงในเวิร์กชีต Excel

คำขอคือคำขอ HTTP ที่มีเนื้อหาแบบมัลติพาร์ต (ดูที่ [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)) ส่วนแรกของเนื้อหาแบบมัลติพาร์ตจะประกอบด้วยข้อมูล `Import2DimensionStringArrayOption` และส่วนที่สองจะประกอบด้วยไฟล์ข้อมูล

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเคน JWT</a>

พารามิเตอร์สำคัญมีรายละเอียดในตารางด้านล่าง:

### **Import2DimensionStringArrayOption**

| ชื่อพารามิเตอร์     | ประเภท              | คำอธิบาย                                                                      |
| -------------------- | ------------------- | ----------------------------------------------------------------------------- |
| FirstRow             | int                 | ดัชนีเริ่มต้นที่ 0 ของแถวที่การนำเข้าเริ่มต้น                                 |
| FirstColumn          | int                 | ดัชนีเริ่มต้นที่ 0 ของคอลัมน์ที่การนำเข้าเริ่มต้น                             |
| Data                 | String[,]           | อาเรย์สองมิติที่มีค่าสตริงที่จะนำเข้า                                         |
| DestinationWorksheet | string              | ชื่อของเวิร์กชีตที่จะรับข้อมูลที่นำเข้า                                       |
| IsInsert             | string (true/false) | หากเป็น **true** ข้อมูลจะถูกแทรกและเซลล์ที่มีอยู่จะเลื่อนไปตามที่จำเป็น   |
| ImportDataType       | string              | ระบุประเภทข้อมูล สำหรับการดำเนินการนี้ให้ใช้ `TwoDimensionStringArray`      |
| Source               | FileSource          | บ่งชี้ตำแหน่งไฟล์ข้อมูลเมื่อพารามิเตอร์ `BatchData` เป็นค่าว่าง (null)       |

### ตัวอย่างเนื้อหาคำขอ

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
}
```

### การตอบกลับ

```json
{
  "Status":"OK",
  "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                                                 |
|------|-------------------------------|--------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                   | กรองข้อมูลสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ                |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)           |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)| โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                           |
| 413  | ข้อมูลส่งมาเกินขนาด (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                              |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                              |

## วิธีใช้ API PostImportData ด้วย SDK

### ข้อกำหนด PostImportData API

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่รวดเร็วที่สุดในการผสานรวมฟังก์ชันนี้ SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณได้ ดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
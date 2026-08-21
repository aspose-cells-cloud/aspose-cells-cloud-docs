---
title: "นำชุดค่าจำนวนเต็มเข้าสู่แผ่นงาน Excel"
linktitle: "นำชุดค่าจำนวนเต็มเข้าสู่แผ่นงาน"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, นำชุดค่าจำนวนเต็มเข้าสู่แผ่นงาน, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "เรียนรู้วิธีการนำชุดค่าจำนวนเต็มเข้าสู่แผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud ซึ่งประกอบด้วยไวยากรณ์คำขอพารามิเตอร์ ตัวอย่างโค้ดสำหรับ SDK หลายภาษา และรายละเอียดของคำตอบ"
weight: 30
ArticleTitle: "นำชุดค่าจำนวนเต็มเข้าสู่แผ่นงาน Excel – API ของ Aspose.Cells Cloud"
---

REST API นี้นำชุดค่าจำนวนเต็มเข้าสู่แผ่นงาน Excel

คำขอต้องเป็น HTTP **POST** ที่มีเนื้อหาแบบมัลติพาร์ต (ดูที่ [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)) ส่วนแรกของเนื้อหาแบบมัลติพาร์ตจะประกอบด้วย JSON payload **ImportIntegerArrayOption** และส่วนที่สองจะประกอบด้วยไฟล์ข้อมูลต้นทาง (เช่น ไฟล์ CSV หรือไฟล์ Excel แบบไบนารี)

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

จุดสิ้นสุดทั้งสองจุดรับ payload แบบมัลติพาร์ตแบบเดียวกัน จุดสิ้นสุดแรกดำเนินการนำเข้าข้อมูลแบบทั่วไป ในขณะที่จุดสิ้นสุดที่สองมุ่งเป้าไปที่สมุดงานเฉพาะที่ระบุด้วย `{name}`

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเค็น JWT</a>

### **พารามิเตอร์ของคำขอ**

### ImportIntegerArrayOption

| ชื่อพารามิเตอร์         | ชนิดข้อมูล | คำอธิบาย                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | ดัชนีแบบเริ่มต้นที่ 0 ของแถวแรกที่จะใส่ข้อมูล                                                                                                                                                |
| **FirstColumn**          | int        | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์แรกที่จะใส่ข้อมูล                                                                                                                                            |
| **IsVertical**           | boolean    | `true` สำหรับแทรกชุดค่าแบบแนวตั้ง (ลงตามคอลัมน์); `false` สำหรับแทรกชุดค่าแบบแนวนอน (ข้ามตามแถว)                                                                                          |
| **Data**                 | Integer[]  | ชุดค่าจำนวนเต็มที่จะนำเข้า                                                                                                                                                                    |
| **DestinationWorksheet** | string     | ชื่อของแผ่นงานที่จะรับข้อมูล                                                                                                                                                                   |
| **IsInsert**             | boolean    | `true` สำหรับแทรกแถว/คอลัมน์ก่อนการเขียนข้อมูล; `false` สำหรับเขียนทับเซลล์ที่มีอยู่                                                                                                         |
| **ImportDataType**       | string     | ชนิดของข้อมูลที่จะนำเข้า ค่าที่ใช้ได้: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`         |
| **Source**               | FileSource | ระบุตำแหน่งของไฟล์ข้อมูลเมื่อพารามิเตอร์ **BatchData** เป็น `null`                                                                                                                             |

#### ตัวอย่างเนื้อหาคำขอ

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### คำตอบ

คำขอที่สำเร็จจะส่งกลับ **HTTP 200** พร้อม payload JSON ที่คล้ายกับ:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

รหัสสถานะที่เป็นไปได้:

| รหัส | ความหมาย                               |
| ---- | --------------------------------------- |
| 200  | การนำเข้าสำเร็จ                        |
| 400  | คำขอไม่ถูกต้อง – ขาดข้อมูลหรือข้อมูลไม่ถูกต้อง |
| 401  | ไม่มีสิทธิ์ – โทเค็นไม่ถูกต้องหรือไม่มีโทเค็น |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์              |

## วิธีใช้ API PostImportData ร่วมกับ SDK

### ข้อกำหนด API PostImportData

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST โดยตรงผ่านเว็บเบราว์เซอร์

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมฟังก์ชันนี้ SDK ซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นที่ตรรกะทางธุรกิจของคุณได้ ดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
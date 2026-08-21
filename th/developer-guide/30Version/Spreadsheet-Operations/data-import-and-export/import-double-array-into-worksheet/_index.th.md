---
title: "นำเข้าอาร์เรย์แบบ double ลงในเวิร์กชีต Excel"
second_title: "เอกสาร"
linktitle: "นำเข้าอาร์เรย์แบบ double"
type: docs
url: /th/import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, นำเข้าอาร์เรย์แบบ double, Excel API, SDK บนคลาวด์"
description: "เรียนรู้วิธีการนำเข้าอาร์เรย์แบบ double ลงในเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วยข้อมูลเกี่ยวกับการยืนยันตัวตน รูปแบบคำขอ พารามิเตอร์ ตัวอย่าง XML/JSON และรายละเอียดคำตอบ"
weight: 20
ArticleTitle: "นำเข้าอาร์เรย์แบบ double ลงในเวิร์กชีต Excel – คู่มือ Aspose.Cells Cloud"
---

REST API นี้ **นำเข้าข้อมูลอาร์เรย์แบบ double** ลงในเวิร์กชีต Excel

> **ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเคน JWT ที่ถูกต้องก่อนเรียกใช้ API นี้ ดูคู่มือการยืนยันตัวตนสำหรับรายละเอียดเพิ่มเติม

คุณจะส่งคำขอ HTTP ที่มีเนื้อหาแบบ **multipart** (ดูที่ [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html))  
ส่วนแรกของเนื้อหาแบบ multipart จะมีข้อมูล **ImportDoubleArrayOption** และส่วนที่สองจะมีไฟล์ข้อมูล

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

#### **ImportDoubleArrayOption**

| ชื่อพารามิเตอร์     | ชนิดข้อมูล | คำอธิบาย                                                                                                   |
| -------------------- | ---------- | ---------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | ดัชนีแบบเริ่มต้นที่ 0 ของแถวแรกที่ข้อมูลจะถูกวางลง                                                          |
| FirstColumn          | int        | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์แรกที่ข้อมูลจะถูกวางลง                                                       |
| IsVertical           | boolean    | `true` / `false` – กำหนดว่าจะแทรกอาร์เรย์แบบแนวตั้ง (`true`) หรือแนวนอน (`false`)                          |
| Data                 | Double[]   | อาร์เรย์ของค่าแบบ double ที่จะนำเข้า                                                                          |
| DestinationWorksheet | string     | ชื่อของเวิร์กชีตปลายทาง                                                                                     |
| IsInsert             | boolean    | `true` / `false` – หากเป็น `true` ข้อมูลจะถูกแทรก หากเป็น `false` เซลล์ที่มีอยู่จะถูกเขียนทับ                     |
| ImportDataType       | string     | ชนิดข้อมูลที่นำเข้า (เช่น `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`)                    |
| Source               | FileSource | ระบุตำแหน่งไฟล์ข้อมูลเมื่อพารามิเตอร์ `BatchData` มีค่าเป็น null                                              |

#### ตัวอย่าง (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### ตัวอย่าง (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### คำตอบ

คำขอที่สำเร็จจะส่งกลับ **HTTP 200** พร้อมข้อมูล JSON ที่มีลักษณะดังนี้:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

โค้ดสถานะที่เป็นไปได้:

| โค้ด | ความหมาย                                       |
| ---- | --------------------------------------------- |
| 200  | การนำเข้าสำเร็จ                               |
| 400  | คำขอไม่ถูกต้อง – ข้อมูลหายไปหรือไม่ถูกต้อง         |
| 401  | ไม่ได้รับอนุญาต – โทเคนไม่ถูกต้องหรือหายไป          |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์                       |

### การจัดการข้อผิดพลาด

เมื่อเกิดข้อผิดพลาด API จะส่งกลับวัตถุ JSON ที่มีโค้ดข้อผิดพลาดและข้อความอธิบาย ตัวอย่างสำหรับคำขอที่ไม่ได้รับอนุญาต:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการดำเนินการนำเข้าที่เกี่ยวข้อง ดูที่หน้าเอกสาร “นำเข้าอาร์เรย์แบบ double สองมิติ” และ “นำเข้าอาร์เรย์จำนวนเต็ม”

## วิธีใช้ API PostImportData ร่วมกับ SDK

### ข้อกำหนด API PostImportData

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบเปิดเผย และช่วยให้คุณดำเนินการ REST ผ่านเว็บเบราว์เซอร์โดยตรง

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับล่างให้ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud แบบครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
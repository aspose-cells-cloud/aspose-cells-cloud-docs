---
title: "นำข้อมูลจำนวนมากเข้าสู่แผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "นำข้อมูลจำนวนมาก"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, Cloud API, นำข้อมูลจำนวนมาก, Excel, CSV, JSON, XML, arrays"
description: "เรียนรู้วิธีการนำข้อมูลจำนวนมาก (CSV, JSON, XML, arrays) เข้าสู่แผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API รวมถึงตัวอย่างการรับรองความถูกต้อง, การร้องขอ/การตอบกลับ, ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด"
weight: 19
ArticleTitle: "นำข้อมูลจำนวนมากเข้าสู่แผ่นงาน Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

REST API นี้ **นำข้อมูลจำนวนมาก** เข้าสู่แผ่นงาน Excel โดยรับคำร้องแบบมัลติพาร์ต โดยส่วนแรกจะมีวัตถุ **ImportBatchDataOption** และส่วนที่สองจะส่งไฟล์ข้อมูลจริง (CSV, JSON, XML เป็นต้น)

การดำเนินการนี้ใช้คำร้อง HTTP แบบมัลติพาร์ต (ดูที่ [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html))

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเคน JWT</a>

### ImportBatchDataOption

| ชื่อพารามิเตอร์         | ประเภท             | คำอธิบาย                                                                                                                                                                                     |
| ------------------------ | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**            | `List<CellValue>` | คอลเลกชันของค่าเซลล์ที่จะเขียนโดยตรง                                                                                                                                          |
| **DestinationWorksheet** | `string`          | ชื่อของแผ่นงานที่ข้อมูลจะถูกนำเข้า                                                                                                                                             |
| **IsInsert**             | `bool`            | เมื่อตั้งค่าเป็น `true` ข้อมูลจะถูกแทรกและเซลล์ที่มีอยู่จะถูกเลื่อนไป; เมื่อตั้งค่าเป็น `false` ข้อมูลจะเขียนทับเซลล์ที่มีอยู่ |
| **ImportDataType**       | `string`          | รูปแบบของข้อมูลที่จะนำเข้า ค่าที่อนุญาต: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData` |
| **Source**               | `FileSource`      | ระบุตำแหน่งของไฟล์ข้อมูลเมื่อ **BatchData** เป็น `null`                                                                                                                         |

### CellValue

| ชื่อพารามิเตอร์ | ประเภท   | คำอธิบาย                                          |
| --------------- | -------- | ------------------------------------------------- |
| **rowIndex**    | `int`    | ดัชนีแถว (เริ่มต้นที่ 0) ของเซลล์เป้าหมาย         |
| **columnIndex** | `int`    | ดัชนีคอลัมน์ (เริ่มต้นที่ 0) ของเซลล์เป้าหมาย     |
| **type**        | `string` | ประเภทข้อมูลของค่า (เช่น `int`, `double`, `string`) |
| **value**       | `string` | ค่าที่จะเขียนลงในเซลล์                           |
| **style**       | `Style`  | ข้อมูลรูปแบบเพิ่มเติมสำหรับเซลล์ (ไม่บังคับ)       |

### FileSource

| ชื่อพารามิเตอร์    | ประเภท   | คำอธิบาย                                                           |
| ------------------ | -------- | ------------------------------------------------------------------ |
| **FileSourceType** | `string` | แหล่งที่มาของไฟล์: `InMemoryFiles`, `CloudFileSystem`, หรือ `RequestFiles` |
| **FilePath**       | `string` | เส้นทางหรือตัวระบุของไฟล์ภายในแหล่งที่มาที่เลือก                     |

### ตัวอย่าง (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### การตอบกลับ

```json
{
  "Status":"OK",
  "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ                    |
| 400  | คำร้องขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                          |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                               |
| 413  | ข้อมูลในส่วนร่างคำร้องใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                              |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                         |

## วิธีใช้ API PostImportData ร่วมกับ SDK

### ข้อกำหนด API PostImportData

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบเปิดเผย เพื่อให้คุณสามารถดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมฟังก์ชันนี้ SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นที่ตรรกะทางธุรกิจของคุณ ดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) สำหรับรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---
title: "นำเข้าอาเรย์จำนวนเต็มสองมิติลงในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "นำเข้าอาเรย์จำนวนเต็มสองมิติ"
type: docs
url: /th/import-a-2D-integer-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-integer-array-into-excel-worksheet/",
    "/import-2dimension-integer-array-into-worksheet/",
    "/import-data/2dimension-integer-array/",
    "/import/2dimension-integer-array/",
  ]
keywords: "Aspose.Cells Cloud, นำเข้าอาเรย์จำนวนเต็มสองมิติ, แผ่นงาน Excel, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API ช่วยให้คุณสามารถนำเข้าอาเรย์จำนวนเต็มสองมิติลงในแผ่นงาน Excel ได้ มี SDK ให้ใช้งานสำหรับ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift"
weight: 20
---

REST API นี้ **นำเข้าอาเรย์จำนวนเต็มสองมิติ** ลงในแผ่นงาน Excel

คำขอเป็นคำขอ HTTP ที่มีเนื้อหาแบบมัลติพาร์ต (ดูที่ [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)) โดยส่วนแรกของเนื้อหาแบบมัลติพาร์ตจะประกอบด้วยข้อมูล `Import2DimensionIntegerArrayOption` และส่วนที่สองจะประกอบด้วยไฟล์ข้อมูล

พารามิเตอร์ที่สำคัญมีรายละเอียดดังตารางต่อไปนี้:

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### **Import2DimensionIntegerArrayOption**

| ชื่อพารามิเตอร์     | ประเภท     | คำอธิบาย                                                                                                                                                                                        |
| -------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| FirstRow             | int        | ดัชนีแบบเริ่มที่ 1 ของแถวแรกที่ข้อมูลจะถูกวาง                                                                                                                                                    |
| FirstColumn          | int        | ดัชนีแบบเริ่มที่ 1 ของคอลัมน์แรกที่ข้อมูลจะถูกวาง                                                                                                                                                 |
| Data                 | Integer[,] | อาเรย์จำนวนเต็มสองมิติที่มีค่าที่ต้องการนำเข้า                                                                                                                                                    |
| DestinationWorksheet | string     | ชื่อของแผ่นงานปลายทาง                                                                                                                                                                           |
| IsInsert             | string     | `"true"` สำหรับการแทรกข้อมูล (เลื่อนเซลล์ที่มีอยู่) , `"false"` สำหรับการเขียนทับเซลล์ที่มีอยู่                                                                                                  |
| ImportDataType       | string     | ระบุรูปแบบข้อมูล ค่าที่รองรับ: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`                     |
| Source               | FileSource | ระบุตำแหน่งของไฟล์ข้อมูลเมื่อพารามิเตอร์ `BatchData` เป็นค่า `null`                                                                                                                               |

### **ตัวอย่าง**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
}
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
| 200  | สำเร็จ (OK)                | กรองข้อมูลสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ     |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)          |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                           |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                          |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                   |

## วิธีใช้ PostImportData API ด้วย SDK

### ข้อมูลจำเพาะของ PostImportData API

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### การใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ กรุณาตรวจสอบที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud อย่างละเอียด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
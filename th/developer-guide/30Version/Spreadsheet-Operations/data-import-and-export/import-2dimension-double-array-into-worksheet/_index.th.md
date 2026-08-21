---
title: "นำเข้าอาเรย์แบบสองมิติแบบ double ลงในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "นำเข้าอาเรย์แบบสองมิติแบบ double"
type: docs
url: /import-a-2d-double-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-double-array-into-excel-worksheet/",
    "/import-2dimension-double-array-into-worksheet/",
    "/import-data/2dimension-double-array/",
    "/import/2dimension-double-array/",
  ]
keywords: "นำเข้าอาเรย์แบบสองมิติแบบ double, Excel, Aspose Cells Cloud, REST API, สเปรดชีต, การนำเข้าข้อมูล"
description: "เรียนรู้วิธีนำเข้าอาเรย์แบบสองมิติแบบ double ลงในแผ่นงาน Excel ผ่าน Aspose.Cells Cloud REST API ซึ่งประกอบด้วยรูปแบบคำขอ พารามิเตอร์ และตัวอย่างโค้ด SDK"
weight: 20
---

REST API นี้ **นำเข้าอาเรย์แบบสองมิติแบบ double** ลงในแผ่นงาน Excel

คำขอนี้เป็น HTTP `POST` ที่มีเนื้อหาแบบ multipart (ดูที่ [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)) ส่วนแรกของเนื้อหาแบบ multipart ประกอบด้วยข้อมูล **Import2DimensionDoubleArrayOption** และส่วนที่สองจะเป็นไฟล์ข้อมูลต้นทาง

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

พารามิเตอร์สำคัญมีรายละเอียดในตารางด้านล่าง:

### Import2DimensionDoubleArrayOption

| ชื่อพารามิเตอร์         | ประเภท         | คำอธิบาย                                                                                                             |
| ------------------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | `int`        | ดัชนีแถว (เริ่มที่ 1) ที่เริ่มการนำเข้าข้อมูล                                                                           |
| **FirstColumn**          | `int`        | ดัชนีคอลัมน์ (เริ่มที่ 1) ที่เริ่มการนำเข้าข้อมูล                                                                        |
| **Data**                 | `Double[,]`  | อาเรย์แบบสองมิติของค่า double ที่จะถูกนำเข้า                                                                           |
| **DestinationWorksheet** | `string`     | ชื่อของแผ่นงานที่จะรับข้อมูล                                                                                          |
| **IsInsert**             | `string`     | `"true"` สำหรับการแทรกแถว, `"false"` สำหรับการเขียนทับเซลล์ที่มีอยู่                                                 |
| **ImportDataType**       | `string`     | ประเภทของข้อมูลที่นำเข้า (เช่น `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData` เป็นต้น) |
| **Source**               | `FileSource` | ระบุตำแหน่งไฟล์ข้อมูลเมื่อพารามิเตอร์ `BatchData` เป็นค่าว่าง                                                         |

**ตัวอย่าง**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### คำตอบ

```json
{
  "Status":"OK",
  "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | กรองข้อมูลสำเร็จ; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์สูญหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | JWT token ไม่ถูกต้องหรือสูญหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error       | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ PostImportData API ด้วย SDK

### 仕様 PostImportData API

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) กำหนด API ที่เข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมฟังก์ชันนี้ SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นที่ตรรกะทางธุรกิจของคุณได้ ดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
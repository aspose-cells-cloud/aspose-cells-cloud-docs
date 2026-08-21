---
title: "การนำเข้าอาร์เรย์สตริงลงในแผ่นงาน Excel – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktitle: "นำเข้าอาร์เรย์สตริง"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, นำเข้าอาร์เรย์สตริง, Excel REST API, การอัปโหลดแบบมัลติพาร์ต, การนำเข้าข้อมูลลงในแผ่นงาน, SDK บนคลาวด์"
description: "เรียนรู้วิธีการนำเข้าอาร์เรย์สตริงลงในแผ่นงาน Excel ผ่าน Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) รวมถึงรูปแบบคำขอ พารามิเตอร์ และตัวอย่าง SDK"
weight: 40
ArticleTitle: "การนำเข้าอาร์เรย์สตริงลงในแผ่นงาน Excel – Aspose.Cells Cloud"
---

การนำเข้าอาร์เรย์สตริงลงในแผ่นงาน Excel เป็นงานที่พบได้บ่อยเมื่อต้องการเติมข้อมูลแบบรายการลงในสมุดงาน กระบวนการนี้มีประโยชน์ในกรณีต่างๆ เช่น การโหลดค่าการตั้งค่า การถ่ายโอนข้อมูลจากแหล่งภายนอก หรือการเริ่มต้นแผ่นงานด้วยคอลเลกชันสตริงที่กำหนดไว้ล่วงหน้า

**ข้อกำหนดเบื้องต้น:**  
- โทเคน JWT ที่ถูกต้องซึ่งได้รับผ่านกระบวนการยืนยันตัวตนของ Aspose.Cells Cloud  
- สมุดงานที่มีอยู่ (หรือสามารถสร้างใหม่ได้) ในพื้นที่จัดเก็บของ Aspose Cloud  
- เวอร์ชัน SDK ที่เหมาะสมซึ่งรองรับโมเดล `ImportStringArrayOption`

API นี้เป็น REST API ที่ใช้สำหรับการนำเข้าข้อมูลแบบอาร์เรย์สตริงลงในแผ่นงาน Excel

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบใช้โทเคน JWT ดูรายละเอียดเพิ่มเติมได้ที่ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนสำหรับคำขอ REST API</a>

### **พารามิเตอร์ของคำขอ**

คำขอใช้เนื้อหา HTTP แบบมัลติพาร์ต (ดูเพิ่มเติมได้ที่ [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html))  
ส่วนแรกของเนื้อหาแบบมัลติพาร์ตจะมีข้อมูลส่วน Payload ของ **ImportStringArrayOption** ส่วนที่สองจะเป็นไฟล์ข้อมูลต้นทาง

พารามิเตอร์สำคัญมีรายละเอียดดังตารางต่อไปนี้:

<caption>พารามิเตอร์ของ ImportStringArrayOption</caption>
### **ImportStringArrayOption**

| ชื่อพารามิเตอร์      | ชนิดข้อมูล | คำอธิบาย                                                                                                                                                                                                 |
| --------------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | ดัชนีแถวเริ่มต้น (นับจาก 1) ที่จะวางข้อมูล                                                                                                                                                               |
| FirstColumn          | int        | ดัชนีคอลัมน์เริ่มต้น (นับจาก 1) ที่จะวางข้อมูล                                                                                                                                                          |
| IsVertical           | boolean    | `true` สำหรับการแทรกข้อมูลตามแนวตั้ง; `false` สำหรับการแทรกข้อมูลตามแนวนอน                                                                                                                            |
| Data                 | String[]   | อาร์เรย์สตริงที่ต้องการนำเข้า                                                                                                                                                                            |
| DestinationWorksheet | string     | ชื่อแผ่นงานที่จะรับข้อมูล                                                                                                                                                                               |
| IsInsert             | boolean    | `true` สำหรับการแทรกแถว/คอลัมน์ (เลื่อนเซลล์ที่มีอยู่); `false` สำหรับการเขียนทับเซลล์ที่มีอยู่                                                                                                        |
| ImportDataType       | string     | ชนิดของข้อมูลที่นำเข้า (เช่น `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`)                           |
| Source               | FileSource | ระบุตำแหน่งของไฟล์ข้อมูลเมื่อ `BatchData` เป็นค่าว่าง (เช่น `CloudFileSystem`, `LocalFile`) จำเป็นหากไม่ได้ระบุ `BatchData`                                                                              |

### ตัวอย่าง

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### คำตอบ

หากคำขอสำเร็จ จะได้รับ **HTTP 200** พร้อม JSON payload ดังนี้:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

รหัสสถานะที่เป็นไปได้มีดังนี้:

| รหัส | ความหมาย                                   |
| ---- | ------------------------------------------ |
| 200  | การนำเข้าสำเร็จ                            |
| 400  | คำขอไม่ถูกต้อง – ข้อมูลขาดหายหรือไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – โทเคนไม่ถูกต้องหรือขาดหาย |
| 500  | ข้อผิดพลาดภายในของเซิร์ฟเวอร์               |


## วิธีการใช้ API PostImportData ร่วมกับ SDK

### ข้อมูลจำเพาะ API PostImportData

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---
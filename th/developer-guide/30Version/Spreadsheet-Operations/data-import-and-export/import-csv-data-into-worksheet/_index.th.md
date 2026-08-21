---
title: "นำเข้าข้อมูล CSV ลงในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "นำเข้าข้อมูล CSV"
type: docs
url: /import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "นำเข้าข้อมูล CSV, Excel, Aspose.Cells Cloud, REST API, สเปรดชีต, การนำเข้า CSV"
description: "Aspose.Cells Cloud REST API ช่วยให้สามารถนำเข้าข้อมูล CSV ลงในแผ่นงาน Excel ได้ ซึ่ง SDK ที่รองรับได้แก่ Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift"
weight: 19
---

REST API นี้ **นำเข้าข้อมูล CSV** ลงในแผ่นงาน Excel

คำขอเป็น HTTP request ที่มีเนื้อหาแบบ multipart (ดูที่ [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)) โดยส่วนแรกของเนื้อหาแบบ multipart จะประกอบด้วยข้อมูล `ImportCSVDataOption` และส่วนที่สองจะประกอบด้วยไฟล์ CSV

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a>

พารามิเตอร์สำคัญมีรายละเอียดดังตารางต่อไปนี้

### ImportCSVDataOption

| ชื่อพารามิเตอร์   | ชนิดข้อมูล                 | คำอธิบาย                                                               |
| ------------------ | -------------------------- | ------------------------------------------------------------------------ |
| SeparatorString    | string                     | อักขระที่ใช้แยกฟิลด์ในไฟล์ CSV (เช่น `,` หรือ `;`)                    |
| ConvertNumericData | string (`true`/`false`)    | ระบุว่าสตริงตัวเลขควรแปลงเป็นค่าตัวเลขหรือไม่                          |
| FirstRow           | int                        | ดัชนีแบบเริ่มต้นที่ 1 ของแถวแรกที่ข้อมูลจะถูกวางไว้                     |
| FirstColumn        | int                        | ดัชนีแบบเริ่มต้นที่ 1 ของคอลัมน์แรกที่ข้อมูลจะถูกวางไว้                 |
| SourceFile         | string                     | ชื่อไฟล์ CSV ต้นทางที่จะนำเข้า                                          |
| CustomParsers      | List\<CustomParserConfig\> | คอลเลกชันการตั้งค่าตัวแปลงแบบกำหนดเองสำหรับคอลัมน์เฉพาะ              |

### CustomParserConfig

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                                           |
| -------------- | ------ | ------------------------------------------------------------------ |
| ColumnIndex    | int    | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์ที่ตัวแปลงแบบกำหนดเองนี้ใช้ได้   |
| ParseMethod    | string | วิธีการแปลงสำหรับคอลัมน์นั้น (เช่น `ToString`, `ToDate`, `ToNumber`) |
| CustomStyle    | string | รูปแบบแบบกำหนดเอง (เช่น รูปแบบตัวเลข) ที่ใช้กับเซลล์ที่แปลงแล้ว   |

**ตัวอย่าง**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### คำตอบ

```json
{
  "Status":"OK",
  "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                                       |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองสำเร็จ คำตอบจะมีรายละเอียดของการดำเนินการ           |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)         |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                   |
| 413  | ข้อมูลในส่วนของ payload ใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                               |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                        |
## วิธีใช้ PostImportData API ด้วย SDK

### ข้อกำหนด PostImportData API

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) กำหนด API ที่เปิดให้เข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถใช้ REST interaction ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นที่ตรรกะทางธุรกิจของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells ด้วย SDK ภาษา PHP:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}

---
---
title: "นำเข้าข้อมูลลงในไฟล์ Excel และส่งออกข้อมูลจากไฟล์ Excel"
second_title: "เอกสาร"
linktitle: "การนำเข้าและส่งออกข้อมูล"
type: docs
url: /th/data-import-and-export/
keywords: "Aspose.Cells Cloud, นำเข้าข้อมูล, ส่งออก Excel, API, CSV, JSON, รูปภาพ, อาเรย์"
description: "เรียนรู้วิธีการนำเข้าข้อมูลจาก CSV, JSON, อาเรย์ และรูปภาพลงในไฟล์ Excel รวมทั้งส่งออกเวิร์กบุ๊ก แผนภูมิ และรูปร่างต่างๆ ไปยัง PDF, PNG และรูปแบบอื่นๆ โดยใช้ API ของ Aspose.Cells Cloud (เวอร์ชัน 3.0)"
weight: 25
---

Aspose.Cells Cloud API รองรับการนำเข้าข้อมูลจากแหล่งข้อมูลที่หลากหลาย และสามารถส่งออกเวิร์กบุ๊ก แผนภูมิ และวัตถุอื่นๆ ของ Excel ไปยังรูปแบบต่างๆ เช่น **XLSX**, **CSV**, **PDF**, **HTML**, **PNG** และอื่นๆ อีกมากมาย ทำให้การจัดการและการแบ่งปันข้อมูลเป็นเรื่องง่ายและมีประสิทธิภาพ

**เวอร์ชัน API:** **v3.0** – อัปเดตล่าสุด: **2024‑03‑15**

### คู่มือเริ่มต้นใช้งานอย่างรวดเร็ว

1. **เตรียมพาร์ทของข้อมูล (payload)** – สร้างเนื้อหา JSON ที่อธิบายตัวเลือกการนำเข้าหรือส่งออก (เช่น `ImportCSVDataOption`, `ExportOptions`)
2. **ส่งคำขอ (request)** – ใช้ `curl`, Postman หรือ SDK เพื่อเรียกเอ็นด์พอยต์ที่เหมาะสม (`POST /cells/import` หรือ `POST /cells/export`)
3. **จัดการกับการตอบกลับ (response)** – เมื่อสำเร็จ คุณจะได้รับไฟล์ที่ประมวลผลแล้ว (ข้อมูลไบนารีหรือ Base64) ในกรณีเกิดข้อผิดพลาด ให้ตรวจสอบโค้ดสถานะ HTTP และข้อความแสดงข้อผิดพลาดที่ส่งกลับมาในเนื้อหา JSON

#### สิ่งที่จำเป็นก่อนเริ่มใช้งาน

- บัญชี Aspose Cloud ที่ใช้งานได้และโทเคน JWT ที่ถูกต้อง
- เวิร์กบุ๊กเป้าหมายต้องมีอยู่ในตำแหน่งพื้นที่เก็บข้อมูลที่ระบุ (สำหรับ API แบบใช้พื้นที่เก็บข้อมูล)
- ส่วนหัว `Content-Type` ที่ถูกต้อง (`multipart/form-data` สำหรับการอัปโหลดไฟล์, `application/json` สำหรับเนื้อหา JSON)

## วิธีการนำเข้าข้อมูลจากแหล่งข้อมูลต่างๆ

การนำเข้าข้อมูลลงในไฟล์ Excel เกี่ยวข้องกับปัจจัยหลายประการที่ต้องพิจารณาในระหว่างกระบวนการ ความสามารถในการนำเข้าข้อมูลได้หลายรูปแบบและประเภทด้วยคุณภาพระดับมืออาชีพเป็นหนึ่งในคุณสมบัติเด่นของ Aspose.Cells Cloud

### ข้อมูลเกี่ยวกับ API การนำเข้าข้อมูล

API ต่อไปนี้มีให้ใช้งานเพื่อนำเข้าข้อมูลลงในไฟล์ Excel หนึ่งไฟล์หรือหลายไฟล์:

| API                                                                                                | คำอธิบาย                                   |
| :------------------------------------------------------------------------------------------------- | :------------------------------------------ |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | นำเข้าข้อมูลลงในไฟล์ Excel โดยไม่ใช้พื้นที่เก็บข้อมูล |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | นำเข้าข้อมูลลงในไฟล์ Excel ที่จัดเก็บอยู่บนคลาวด์ |

### พารามิเตอร์ของคำขอ

#### โดยไม่ใช้พื้นที่เก็บข้อมูล

| ชื่อพารามิเตอร์ | ประเภท         | ตำแหน่ง | คำอธิบาย                                   |
| :--------------- | :------------- | :------- | :------------------------------------------ |
| file             | ไฟล์           | formData | ไฟล์ที่จะอัปโหลด                            |
| ImportOption     | ImportOptions  | body     | ระบุรูปแบบการนำเข้า (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### โดยใช้พื้นที่เก็บข้อมูล

| ชื่อพารามิเตอร์ | ประเภท         | ตำแหน่ง | คำอธิบาย                      |
| :--------------- | :------------- | :------- | :----------------------------- |
| name             | สตริง (string)  | path     | ชื่อไฟล์ Excel                |
| folder           | สตริง (string)  | query    | ที่อยู่โฟลเดอร์ในพื้นที่เก็บข้อมูล |
| storageName      | สตริง (string)  | query    | ชื่อพื้นที่เก็บข้อมูล         |
| importData       | ImportOptions  | body     | เนื้อหาข้อมูลที่จะนำเข้า      |

#### พารามิเตอร์ของตัวเลือกการนำเข้าข้อมูล

**พารามิเตอร์สำคัญอธิบายไว้ในตารางต่อไปนี้:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>ข้อมูลแบตช์ที่จะนำเข้า</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ระบุว่าจะแทรกข้อมูลหรือไม่ (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>ระบุว่าจะแปลงข้อมูลตัวเลขหรือไม่ (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>ดัชนีของแถวแรก</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>ดัชนีของคอลัมน์แรก</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>ตัวคั่นคอลัมน์</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>การตั้งค่าผู้แปลงผลลัพธ์แบบกำหนดเอง</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>ดัชนีของแถวแรก</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>ดัชนีของคอลัมน์แรก</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>ระบุว่าจะวางรูปภาพในแนวตั้งหรือไม่ (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>ข้อมูลรูปภาพ (สตริงแบบ Base64)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ระบุว่าจะแทรกข้อมูลหรือไม่ (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>ดัชนีของแถวแรก</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>ดัชนีของคอลัมน์แรก</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>อาเรย์จำนวนเต็มสองมิติ</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ระบุว่าจะแทรกข้อมูลหรือไม่ (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>ดัชนีของแถวแรก</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>ดัชนีของคอลัมน์แรก</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>อาเรย์เลขทศนิยมสองมิติ</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ระบุว่าจะแทรกข้อมูลหรือไม่ (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>ดัชนีของแถวแรก</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>ดัชนีของคอลัมน์แรก</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>อาเรย์สตริงสองมิติ</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ระบุว่าจะแทรกข้อมูลหรือไม่ (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>ดัชนีของแถวแรก</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>ดัชนีของคอลัมน์แรก</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>ระบุว่าอาเรย์อยู่ในแนวตั้งหรือไม่ (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>อาเรย์จำนวนเต็มหนึ่งมิติ</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ระบุว่าจะแทรกข้อมูลหรือไม่ (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>ดัชนีของแถวแรก</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>ดัชนีของคอลัมน์แรก</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>ระบุว่าอาเรย์อยู่ในแนวตั้งหรือไม่ (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>อาเรย์เลขทศนิยมหนึ่งมิติ</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ระบุว่าจะแทรกข้อมูลหรือไม่ (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>ดัชนีแถวบนซ้าย</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>ดัชนีคอลัมน์บนซ้าย</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>ดัชนีแถวล่างขวา</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>ดัชนีคอลัมน์ล่างขวา</td></tr>
    <tr><td>Filename</td><td>string</td><td>ชื่อไฟล์ต้นทาง</td></tr>
    <tr><td>Data</td><td>string</td><td>ข้อมูลสตริงที่จะนำเข้า</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>ชื่อชีตเป้าหมาย</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ระบุว่าจะแทรกข้อมูลหรือไม่ (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>ตำแหน่งไฟล์ข้อมูลเมื่อ BatchData เป็นค่าว่าง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>ดัชนีแถวของเซลล์</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>ดัชนีคอลัมน์ของเซลล์</td></tr>
    <tr><td>type</td><td>string</td><td>ประเภทข้อมูลของค่าเซลล์</td></tr>
    <tr><td>value</td><td>string</td><td>ค่าเซลล์</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>นิยามรูปแบบเซลล์</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>พารามิเตอร์</th><th>ประเภท</th><th>คำอธิบาย</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem หรือ RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>ที่อยู่ไฟล์ต้นทาง</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## วิธีการส่งออกวัตถุ Excel ไปยังรูปแบบไฟล์ต่างๆ

หากคุณสร้างไฟล์ Excel 之初ในรูปแบบเช่น **XLS**, **XLSX**, **XLSB** หรือ **CSV** คุณอาจต้องการแปลงเป็นรูปแบบอื่นเพื่อใช้ประโยชน์จากคุณสมบัติเฉพาะ เช่น การส่งออกเป็น **PDF** จะป้องกันไม่ให้ผู้อื่นแก้ไขเนื้อหาโดยไม่ได้รับอนุญาต ทั้งยังช่วยให้อ่านและแบ่งปันได้ง่ายขึ้น

การส่งออกวัตถุ Excel เกี่ยวข้องกับปัจจัยหลายประการ Aspose.Cells Cloud รองรับการส่งออกเวิร์กบุ๊ก แผนภูมิ รูปร่าง และรูปภาพด้วยคุณภาพสูงไปยังรูปแบบต่างๆ:

_รูปแบบที่รองรับเฉพาะการส่งออก_: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS  
_รูปแบบที่รองรับทั้งการนำเข้าและส่งออก_: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

คำขอนี้ใช้เนื้อหาแบบมัลติพาร์ตตามที่กำหนดไว้ใน [RFC 2046] และ [RFC 1341] ส่วนแรกจะมีไฟล์ข้อมูล ส่วนที่สองจะมีตัวเลือกการบันทึก

### ข้อมูลเกี่ยวกับ API การส่งออก

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                                                                   |
| :--------------- | :----- | :------- | :------------------------------------------------------------------------------------------ |
| file             | ไฟล์   | formData | ไฟล์ที่จะอัปโหลด                                                                            |
| objectType       | สตริง (string) | query    | ประเภทวัตถุ (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format           | สตริง (string) | query    | รูปแบบไฟล์เอาต์พุตที่ต้องการ (ดู [รูปแบบไฟล์ที่รองรับ](/cells/supported-file-formats/))     |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) นิยามอินเทอร์เฟซการเขียนโปรแกรมแบบสาธารณะที่ทำให้คุณสามารถโต้ตอบกับ REST API ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL บน command-line เพื่อเรียก API ตัวอย่างต่อไปนี้แสดงคำขอและคำตอบ JSON ที่สอดคล้องกัน

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### โค้ดสถานะ HTTP ที่พบบ่อย

| สถานะ | ความหมาย                                                                 | คำแนะนำในการดำเนินการ                       |
| ----- | ------------------------------------------------------------------------ | ------------------------------------------- |
| 200   | สำเร็จ – ไฟล์ถูกส่งออกแล้ว                                              | ประมวลผลไฟล์ที่ส่งกลับมา                  |
| 400   | คำขอผิดรูปแบบ – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง                        | ตรวจสอบเนื้อหาคำขอและสตริงการค้นหา        |
| 401   | ไม่ได้รับอนุญาต – โทเคน JWT ไม่ถูกต้องหรือหมดอายุ                      | รีเฟรชโทเคนแล้วลองใหม่                    |
| 404   | ไม่พบ – เวิร์กบุ๊กหรือชีตที่ระบุไม่มีอยู่                               | ตรวจสอบชื่อไฟล์และที่อยู่พื้นที่เก็บข้อมูล |
| 500   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดเกิดขึ้นบนเซิร์ฟเวอร์ | ติดต่อฝ่ายสนับสนุนของ Aspose โดยระบุ ID คำขอ |

## วิธีการเรียกใช้ API การนำเข้าและส่งออก

บทความต่อไปนี้อธิบายแต่ละ API อย่างละเอียด และมีตัวอย่าง cURL และ SDK:

- [วิธีการนำเข้าข้อมูลลงในไฟล์ Excel โดยไม่ใช้พื้นที่เก็บข้อมูล](/cells/import/without-using-storage)
- [วิธีการนำเข้าข้อมูลลงในไฟล์ Excel โดยใช้พื้นที่เก็บข้อมูล](/cells/import/with-using-storage)
- [วิธีการนำเข้าข้อมูลแบตช์ลงในชีต Excel](/cells/import-batch-data-into-excel-worksheet/)
- [วิธีการนำเข้าข้อมูล CSV ลงในชีต Excel](/cells/import-CSV-data-into-excel-worksheet/)
- [วิธีการนำเข้ารูปภาพลงในชีต Excel](/cells/import-picture-into-excel-worksheet/)
- [วิธีการนำเข้าอาเรย์จำนวนเต็มลงในชีต Excel](/cells/import-integer-array-into-excel-worksheet/)
- [วิธีการนำเข้าอาเรย์เลขทศนิยมลงในชีต Excel](/cells/import-double-array-into-excel-worksheet/)
- [วิธีการนำเข้าอาเรย์สตริงลงในชีต Excel](/cells/import-string-array-into-excel-worksheet/)
- [วิธีการนำเข้าอาเรย์จำนวนเต็มสองมิติลงในชีต Excel](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [วิธีการนำเข้าอาเรย์เลขทศนิยมสองมิติลงในชีต Excel](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [วิธีการนำเข้าอาเรย์สตริงสองมิติลงในชีต Excel](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [วิธีการส่งออกแผนภูมิ Excel ไปยังรูปแบบไฟล์อื่น](/cells/export-excel-chart-to-different-formats/)
- [วิธีการส่งออก list-object ของ Excel ไปยังรูปแบบไฟล์อื่น](/cells/export-excel-listobject-to-different-formats/)
- [วิธีการส่งออก ole-object ของ Excel ไปยังรูปแบบไฟล์อื่น](/cells/export-excel-ole-object/)
- [วิธีการส่งออกภาพของ Excel ไปยังรูปแบบไฟล์อื่น](/cells/export-excel-picture-to-different-formats/)
- [วิธีการส่งออก rูปร่างของ Excel ไปยังรูปแบบไฟล์อื่น](/cells/export-excel-shape-to-different-formats/)
- [วิธีการส่งออกเวิร์กบุ๊ก Excel ไปยังรูปแบบไฟล์อื่น](/cells/export-excel-to-different-formats/)
- [วิธีการส่งออกชีต Excel ไปยังรูปแบบไฟล์อื่น](/cells/export-excel-worksheet-to-different-formats/)

---
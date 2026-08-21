---
title: "การใช้งานตารางไขว้ด้วยงาน CellsObjectOperate"
type: docs
url: /tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "API ตารางไขว้ของ Aspose Cells, CellsObjectOperate, Excel REST API"
description: "เรียนรู้วิธีการสร้างตารางไขว้ใน Excel โดยใช้งานงาน CellsObjectOperate จาก Aspose.Cells Cloud พร้อมตัวอย่าง cURL, คู่มือพารามิเตอร์ และการอ้างอิง SDK"
weight: 10
---

REST API นี้ **สร้าง** ตารางไขว้โดยใช้งานงาน **CellsObjectOperate**

**PivotTableOperateParameter**

| ชื่อพารามิเตอร์      | ชนิดข้อมูล          | คำอธิบาย                                                                 |
|---------------------|---------------|-----------------------------------------------------------------------------|
| DestCellName        | string        | เซลล์มุมบนซ้ายของตารางไขว้ (เช่น `C1`)                               |
| SourceData          | string        | ช่วงข้อมูลที่ใช้เป็นแหล่งข้อมูล (เช่น `Sheet2!A1:E8`)                |
| TableName           | string        | ชื่อที่กำหนดให้กับตารางไขว้ใหม่                                       |
| UseSameSource       | string        | `true` / `false` – ระบุว่าตารางไขว้ใช้สมุดงานเดียวกันหรือไม่         |
| PivotTableIndex     | integer       | ดัชนีของตารางไขว้เมื่อมีตารางหลายตารางในworksheet                     |
| PivotFieldRows      | integer[]     | ดัชนีเริ่มต้นด้วยศูนย์ของฟิลด์ที่จะวางในพื้นที่แถว                     |
| PivotFieldColumns   | integer[]     | ดัชนีเริ่มต้นด้วยศูนย์ของฟิลด์ที่จะวางในพื้นที่คอลัมน์                  |
| PivotFieldData      | integer[]     | ดัชนีเริ่มต้นด้วยศูนย์ของฟิลด์ที่จะถูกประมวลผลเป็นข้อมูล               |

## REST API

| **API**               | **Type** | **คำอธิบาย** | **ลิงก์ทรัพยากร** |
|-----------------------|----------|-----------------|-------------------|
| /cells/task/runtask   | POST     | รันงาน        | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

### เงื่อนไขเบื้องต้น
ก่อนเรียกใช้งาน API คุณต้อง:

1. สมัครสมาชิกบัญชี Aspose.Cloud และสร้างแอปพลิเคชันเพื่อรับ **client ID** และ **client secret**  
2. ขอ **JWT token** จาก endpoint `/connect/token` โดยใช้ข้อมูลประจำตัวของ client  
3. แนบ token นี้ใน header `Authorization: Bearer <jwt token>` ของทุกคำขอ  

ตอนนี้คุณสามารถใช้เครื่องมือ command-line **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ตัวอย่าง cURL – นำเข้าข้อมูล (ขั้นตอนที่ 1)
curl -v "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -X POST \
  -H "accept: application/xml" \
  -H "Content-Type: application/xml" \
  -H "Authorization: Bearer <jwt token>" \
  -d '
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>Book1.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <BatchData>
            <!-- แถวตัวอย่าง – แสดงเพียงไม่กี่แถวเพื่อความกระชับ -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Sport</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Year</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Quarter</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Sales</value></CellValue>
            <!-- …แถวเพิ่มเติมถูกลบออกเพื่อความชัดเจน… -->
          </BatchData>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>CellsObjectOperate</TaskType>
      <CellsObjectOperateTaskParameter>
        <OperateObject>
          <OperateObjectType>ListObject</OperateObjectType>
          <Position>
            <Workbook>
              <FileSourceType>InMemoryFiles</FileSourceType>
              <FilePath>Book1.xlsx</FilePath>
            </Workbook>
            <SheetName>Sheet1</SheetName>
            <ListObjectIndex>0</ListObjectIndex>
          </Position>
        </OperateObject>

        <PivotTableOperateParameter>
          <OperateType>Add</OperateType>
          <SourceData>=Sheet2!A1:E8</SourceData>
          <DestCellName>C1</DestCellName>
          <TableName>TestPivot</TableName>
          <UseSameSource>true</UseSameSource>
          <PivotTableIndex>0</PivotTableIndex>
          <PivotFieldRows><int>0</int><int>1</int></PivotFieldRows>
          <PivotFieldColumns><int>2</int></PivotFieldColumns>
          <PivotFieldData><int>3</int><int>4</int></PivotFieldData>
        </PivotTableOperateParameter>

        <DestinationWorkbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>Book001.xlsx</FilePath>
        </DestinationWorkbook>
      </CellsObjectOperateTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>OutputStream</DestinationType>
          <InputFile>Book001.xlsx</InputFile>
          <OutputFile>Output/ReportS004.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
สถานะ HTTP ที่เป็นไปได้:
- **200 OK** – สร้างตารางไขว้เรียบร้อยแล้ว ค่าที่ได้รับจะมี `TaskId` ที่สามารถใช้เพื่อสอบถามสถานะของคำขอได้
- **400 Bad Request** – โครงสร้าง XML ไม่ถูกต้องหรือไม่มีพารามิเตอร์ที่จำเป็น
- **401 Unauthorized** – ไม่มีหรือ JWT token ไม่ถูกต้อง
- **500 Internal Server Error** – เกิดข้อผิดพลาดที่ไม่คาดคิดในฝั่งเซิร์ฟเวอร์

ตัวอย่างการตอบกลับที่สำเร็จ (XML):

<?xml version="1.0" encoding="UTF-8"?>
<TaskResponse>
  <TaskId>12345</TaskId>
  <Status>Completed</Status>
  <Result>
    <ResultSource>InMemoryFiles</ResultSource>
    <ResultDestination>Output/ReportS004.xlsx</ResultDestination>
  </Result>
</TaskResponse>
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับ Cloud

การใช้งาน SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และอนุญาตให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดู [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:
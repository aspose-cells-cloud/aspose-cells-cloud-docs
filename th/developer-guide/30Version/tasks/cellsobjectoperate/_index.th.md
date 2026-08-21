---
title: "Aspose.Cells Cloud API – การทำงานกับงาน CellsObjectOperate (REST)"
second_title: "เอกสาร"
type: docs
url: /th/tasks/cells-object-operate/
aliases: [  /th/working-with-cellsobjectoperate-task/ ]
description: "เรียนรู้วิธีใช้งานงาน CellsObjectOperate ใน Aspose.Cells Cloud API พร้อมข้อมูลอ้างอิงพารามิเตอร์ ตัวอย่างคำขอและคำตอบ รวมถึงคำแนะนำด้านแนวทางปฏิบัติที่ดีสำหรับเวิร์กชีต แผนภูมิ และพีชต์แท็บ"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – การทำงานกับงาน CellsObjectOperate (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "งาน CellsObjectOperate"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "การดำเนินการแผนภูมิ"
  - "API พีชต์แท็บ"
  - "API ตัวแบ่งหน้า"
---

**ภาพรวม**  
**CellsObjectOperate** งานนี้ช่วยให้คุณสามารถดำเนินการสร้าง อ่าน แก้ไข และลบ (CRUD) วัตถุ Excel เช่น สมุดงาน เวิร์กชีต แผนภูมิ พีชต์แท็บ รูปร่าง ตัวแบ่งหน้า และอื่นๆ ผ่านคำขอ REST เพียงคำขอกเดียว โดยระบุประเภทของวัตถุด้วย `OperateObjectType` และระบุบล็อกพารามิเตอร์ที่สอดคล้องกัน (เช่น `ChartOperateParameter` สำหรับการดำเนินการที่เกี่ยวกับแผนภูมิ)

---

**OperateObject**

| ชื่อพารามิเตอร์        | ชนิดข้อมูล | คำอธิบาย |
| ----------------------- | ----------- | ----------- |
| OperateObjectType       | string      | ประเภทของวัตถุ Excel ที่จะดำเนินการ ค่าที่อนุญาต: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak` |
| OperateObjectPosition   | object      | คอนเทนเนอร์ที่ระบุตำแหน่งของวัตถุเป้าหมาย (เช่น ชื่อสมุดงาน ชื่อเวิร์กชีต ดัชนีแผนภูมิ) จำเป็นสำหรับการดำเนินการส่วนใหญ่ |

**OperateObjectPosition**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| ---------------- | ----------- | ----------- |
| Workbook         | object      | สมุดงานที่มีวัตถุเป้าหมาย ต้องระบุ `FileName` (สำหรับพื้นที่จัดเก็บบนคลาวด์) หรือ `FileContent` (ข้อมูลที่เข้ารหัส base‑64) |
| SheetName        | string      | ชื่อของเวิร์กชีตที่จะดำเนินการ จำเป็นสำหรับวัตถุระดับเวิร์กชีต (เช่น แผนภูมิ รูปร่าง เป็นต้น) |
| ChartIndex       | integer     | ดัชนีแบบเริ่มต้นที่ 0 ของแผนภูมิภายในเวิร์กชีต (ใช้เมื่อ `OperateObjectType` เป็น `Chart`) |
| ShapeIndex       | integer     | ดัชนีแบบเริ่มต้นที่ 0 ของรูปร่างภายในเวิร์กชีต (ใช้เมื่อ `OperateObjectType` เป็น `Shape`) |
| CellName         | string      | การอ้างอิงเซลล์แบบรูปแบบ A1 (เช่น `A1`) ใช้สำหรับการดำเนินการระดับเซลล์ |
| ListObjectIndex  | integer     | ดัชนีแบบเริ่มต้นที่ 0 ของวัตถุตาราง (ใช้เมื่อ `OperateObjectType` เป็น `ListObject`) |

**ChartOperateParameter**

| ชื่อพารามิเตอร์       | ชนิดข้อมูล | คำอธิบาย |
| --------------------- | ----------- | ----------- |
| ChartIndex            | integer     | ดัชนีของแผนภูมิที่จะแก้ไข จำเป็นเมื่ออัปเดตแผนภูมิที่มีอยู่ |
| ChartType             | string      | ประเภทของแผนภูมิที่จะสร้าง (เช่น `Bar`, `Line`, `Pie`) |
| UpperLeftRow          | integer     | หมายเลขแถวของมุมซ้ายบนของแผนภูมิ (แบบเริ่มต้นที่ 0) |
| UpperLeftColumn       | integer     | หมายเลขคอลัมน์ของมุมซ้ายบนของแผนภูมิ (แบบเริ่มต้นที่ 0) |
| LowerRightRow         | integer     | หมายเลขแถวของมุมขวาล่างของแผนภูมิ |
| LowerRightColumn      | integer     | หมายเลขคอลัมน์ของมุมขวาล่างของแผนภูมิ |
| Area                  | string      | ช่วงข้อมูลสำหรับแผนภูมิ (เช่น `A1:B5`) |
| IsVertical            | string      | `true` หากการจัดวางของแผนภูมิเป็นแนวตั้ง มิฉะนั้น `false` |
| CategoryData          | string      | ช่วงที่ให้ป้ายชื่อแกน X (แกนหมวดหมู่) |
| IsAutoGetSerialName   | string      | `true` เพื่อสร้างชื่อซีรีส์โดยอัตโนมัติ `false` เพื่อใช้ชื่อที่กำหนดเอง |
| Title                 | string      | ข้อความหัวเรื่องที่แสดงบนแผนภูมิ |

**ListObjectOperateParameter**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| ---------------- | ----------- | ----------- |
| ListObject       | object      | วัตถุการตั้งค่าสำหรับการดำเนินการตาราง ประกอบด้วยคุณสมบัติ เช่น `ShowHeader`, `ShowTotal`, และ `Style` |

**PageBreakOperateParameter**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| ---------------- | ----------- | ----------- |
| PageBreakType    | string      | ประเภทของตัวแบ่งหน้า (`Horizontal` หรือ `Vertical`) |
| Index            | integer     | ดัชนีแบบเริ่มต้นที่ 0 ของตัวแบ่งหน้าที่จะลบหรือแก้ไข |
| Row              | integer     | หมายเลขแถวที่จะวางตัวแบ่งหน้าแนวนอน |
| Column           | integer     | หมายเลขคอลัมน์ที่จะวางตัวแบ่งหน้าแนวตั้ง |
| StartIndex       | integer     | ดัชนีเริ่มต้นสำหรับการดำเนินการตัวแบ่งหน้าแบบช่วง |
| EndIndex         | integer     | ดัชนีสิ้นสุดสำหรับการดำเนินการตัวแบ่งหน้าแบบช่วง |

**PageSetupOperateParameter**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| ---------------- | ----------- | ----------- |
| PageSetup        | object      | การตั้งค่าการจัดหน้ากระดาษ (ระยะขอบ ทิศทาง ขนาดกระดาษ เป็นต้น) |

**PivotTableOperateParameter**

| ชื่อพารามิเตอร์   | ชนิดข้อมูล   | คำอธิบาย |
| ----------------- | ------------ | ----------- |
| DestCellName      | string       | เซลล์ซ้ายบนของช่วงปลายทางสำหรับพีชต์แท็บ (เช่น `C5`) |
| SourceData        | string       | ช่วงข้อมูลต้นทางสำหรับพีชต์แท็บ (เช่น `A1:D100`) |
| TableName         | string       | ชื่อที่กำหนดให้กับพีชต์แท็บที่สร้างขึ้น |
| UseSameSource     | string       | `true` เพื่อใช้ช่วงข้อมูลต้นทางที่มีอยู่ `false` เพื่อสร้างช่วงใหม่ |
| PivotTableIndex   | integer      | ดัชนีของพีชต์แท็บที่จะอัปเดต (จำเป็นสำหรับการดำเนินการแก้ไข/ลบ) |
| PivotFieldRows    | integer[]    | คอลเลกชันของดัชนีฟิลด์ที่จะปรากฏในพื้นที่แถว |
| PivotFieldColumns | integer[]    | คอลเลกชันของดัชนีฟิลด์ที่จะปรากฏในพื้นที่คอลัมน์ |
| PivotFieldData    | integer[]    | คอลเลกชันของดัชนีฟิลด์ที่จะปรากฏในพื้นที่ข้อมูล |

**ShapeOperateParameter**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| ---------------- | ----------- | ----------- |
| Shape            | object      | คำนิยามของรูปร่าง (ประเภท ตำแหน่ง ขนาด ข้อความ เป็นต้น) |

**WorkbookSettingsOperateParameter**

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | คำอธิบาย |
| ----------------- | ----------- | ----------- |
| WorkbookSettings  | object      | การตั้งค่าที่ส่งผลต่อสมุดงานทั้งหมด (เช่น โหมดการคำนวณ ความแม่นยำ เป็นต้น) |

**WorksheetOperateParameter**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| ---------------- | ----------- | ----------- |
| Name             | string      | ชื่อปัจจุบันของเวิร์กชีตที่จะดำเนินการ |
| SheetType        | string      | ประเภทของชีต (`Worksheet`, `Chart` เป็นต้น) |
| NewName          | string      | ชื่อใหม่สำหรับเวิร์กชีตเมื่อเปลี่ยนชื่อ |
| MovingRequest    | object      | พารามิเตอร์สำหรับการย้ายเวิร์กชีต (เช่น `FromIndex`, `ToIndex`) |

## API แบบ REST

| API                | ประเภท | คำอธิบาย | ลิงก์ทรัพยากร |
| ------------------ | ------ | ----------- | ------------- |
| /cells/task/runtask| POST   | รันงาน     | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

### สิ่งที่ต้องมีก่อนใช้งาน
- **การยืนยันตัวตน** – ใส่หัวข้อ `Authorization: Bearer <access_token>` ที่ถูกต้อง  
- **พื้นที่จัดเก็บ** – สมุดงานต้นทางต้องถูกจัดเก็บไว้ใน Aspose Cloud Storage หรือจัดส่งเป็นเนื้อหาที่เข้ารหัส base‑64 ในเนื้อหาคำขอ  
- **เวอร์ชัน API** – เอกสารนี้มุ่งเป้าไปที่ **v3.0** ของ Aspose.Cells Cloud API

### ตัวอย่างคำขอ (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

เนื้อหาคำขอเป็นไปตามโครงสร้าง **CellsObjectOperateRequest** ที่นิยามไว้ด้านล่าง:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* นิยามเพิ่มเติมถูกลบออกเพื่อความกระชับ */
  }
}
```

### ตัวอย่างคำตอบ (ความสำเร็จ – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Chart created successfully."
  }
}
```

คำตอบประกอบด้วยฟิลด์ต่อไปนี้:

| ฟิลด์   | ชนิดข้อมูล | คำอธิบาย |
| ------- | ----------- | ----------- |
| Code    | integer     | โค้ดสถานะแบบ HTTP‑like ที่ส่งคืนโดยเครื่องยนต์งาน |
| Status  | string      | สถานะอ่านเข้าใจได้ของมนุษย์ (เช่น `OK`) |
| TaskId  | string      | ตัวระบุของงานแบบอะซิงโครนัส |
| Result  | object      | วัตถุที่เก็บผลลัพธ์เฉพาะของงาน |
| Result.ChartId | integer | ตัวระบุของแผนภูมิที่สร้างหรือแก้ไข |
| Result.Message | string  | ข้อความสั้นอธิบายผลลัพธ์ |

### การจัดการข้อผิดพลาด

| สถานะ HTTP | โค้ดข้อผิดพลาด | คำอธิบาย | วิธีแก้ไขที่แนะนำ |
| ----------- | -------------- | ----------- | ---------------- |
| 400         | InvalidParameter | พารามิเตอร์คำขอหนึ่งตัวหรือมากกว่านั้นขาดหายหรือมีรูปแบบผิด | ตรวจสอบฟิลด์ที่จำเป็นและชนิดข้อมูล |
| 401         | Unauthorized | โทเคนการยืนยันตัวตนไม่ถูกต้องหรือขาดหาย | รีเฟรชโทเคนการเข้าถึงและใส่ไว้ในหัวข้อ `Authorization` |
| 404         | NotFound | สมุดงาน เวิร์กชีต หรือวัตถุที่ระบุไม่มีอยู่จริง | ตรวจสอบ `FileName`, `SheetName` และดัชนีของวัตถุ |
| 500         | ServerError | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ | ลองส่งคำขอใหม่ หากปัญหายังคงอยู่ ติดต่อฝ่ายสนับสนุน |

### กรณีการใช้งานทั่วไป
- **เพิ่มแผนภูมิใหม่** ลงในเวิร์กชีต  
- **เปลี่ยนชื่อเวิร์กชีต** (`OperateObjectType = "Worksheet"` พร้อม `WorksheetOperateParameter.NewName`)  
- **แทรกตัวแบ่งหน้า** (`OperateObjectType = "PageBreak"` พร้อม `PageBreakOperateParameter`)  
- **อัปเดตข้อมูลต้นทางของพีชต์แท็บ** (`OperateObjectType = "PivotTable"` พร้อม `PivotTableOperateParameter.SourceData`)  
- **แก้ไขการตั้งค่าสมุดงาน** เช่น โหมดการคำนวณ (`OperateObjectType = "WorkbookSettings"`)  

---  

*คำอธิบายทั้งหมดได้รับมาจากสเปค OpenAPI ทางการของ Aspose.Cells Cloud*
---
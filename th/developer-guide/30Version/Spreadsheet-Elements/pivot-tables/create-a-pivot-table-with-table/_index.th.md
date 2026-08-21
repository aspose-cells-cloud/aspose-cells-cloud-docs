---
title: "แปลงตารางเป็นตารางพีวีที"
second_title: "เอกสาร"
linktype: แปลง
type: docs
url: /pivot-tables/convert-table-to-pivottable/
aliases:
  [
    "/create-a-pivottable-with-table/",
    "/create-new-pivot-table-with-list-object-as-source-data/",
  ]
keywords: "ตารางพีวีที, วัตถุรายการ, Aspose.Cells Cloud, REST API, แปลงตารางเป็นตารางพีวีที"
description: "เรียนรู้วิธีการสร้างตารางพีวีทีจากวัตถุรายการโดยใช้ Aspose.Cells Cloud REST API รวมถึงรายละเอียดคำขอ ตัวอย่าง cURL และการอ้างอิง SDK"
weight: 60
ArticleTitle: "แปลงตารางเป็นตารางพีวีที – เอกสาร Aspose.Cells Cloud"
---

API นี้ REST สร้าง **ตารางพีวีที** จากวัตถุรายการ

ตารางพีวีทีสรุปข้อมูลจากวัตถุรายการ ช่วยให้คุณสามารถวิเคราะห์และรายงานชุดข้อมูลขนาดใหญ่ได้โดยตรงภายในสมุดงาน

**ข้อกำหนดเบื้องต้น:**  
- เหรียญ JWT bearer ที่ถูกต้องสำหรับการยืนยันตัวตน  
- สมุดงานต้องมีอยู่ในตำแหน่งที่จัดเก็บที่ระบุ  
- แผ่นงานเป้าหมายต้องมีวัตถุรายการที่คุณต้องการสรุป

## API PostWorksheetListObjectSummarizeWithPivotTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| --------------- | ------- | -------- | ------------------------------------------ |
| name            | string  | path     | ชื่อไฟล์สมุดงาน |
| sheetName       | string  | path     | แผ่นงานที่มีวัตถุรายการ |
| listObjectIndex | integer | path     | ดัชนีของวัตถุรายการในแผ่นงาน |
| destsheetName   | string  | query    | ชื่อแผ่นงานปลายทาง |
| request         | object  | body     | ข้อมูล JSON ที่กำหนดตารางพีวีที |
| folder          | string  | query    | ตำแหน่งโฟลเดอร์ที่สมุดงานอยู่ |
| storageName     | string  | query    | ชื่อพื้นที่จัดเก็บ |

เนื้อหาคำขอต้องเป็นไปตามโครงร่าง JSON ที่กำหนดด้านล่าง:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "ชื่อของตารางพีวีทีใหม่" },
    "DestCellName": { "type": "string", "description": "เซลล์มุมซ้ายบนของตารางพีวีที (เช่น \"C1\")" },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "ดัชนีแบบเริ่มต้นที่ 0 ของฟิลด์ที่จะใส่ในแถว"
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "ดัชนีแบบเริ่มต้นที่ 0 ของฟิลด์ที่จะใส่ในคอลัมน์"
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "ดัชนีแบบเริ่มต้นที่ 0 ของฟิลด์ที่จะใช้เป็นฟิลด์ข้อมูล"
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

<a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">ข้อกำหนด OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะและช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*หมายเหตุ: ใช้ปลายทางการผลิต (`api.aspose.cloud`) สำหรับสภาพแวดล้อมจริง เท่านั้น ปลายทาง QA (`api-qa.aspose.cloud`) มีไว้เพื่อการทดสอบเท่านั้น HTTPS จำเป็นสำหรับการเรียกใช้งานทุกครั้งในสภาพแวดล้อมจริง*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                   | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองสำเร็จ การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:
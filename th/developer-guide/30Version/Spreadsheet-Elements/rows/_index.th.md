---
title: "การจัดการแถวใน Excel – API คลาวด์ของ Aspose.Cells"
ArticleTitle: "การจัดการแถวใน Excel – API คลาวด์ของ Aspose.Cells"
second_title: "เอกสาร"
linktype: "docs"
url: /th/rows/
aliases: [  /th/working-with-rows/ ]
keywords: "Aspose.Cells, แถว Excel, REST API, การจัดการสเปรดชีต"
description: "จัดการแถวในไฟล์ Excel โดยใช้ API คลาวด์ของ Aspose.Cells ผ่าน REST API รองรับ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift"
weight: 100
---

## การจัดการแถวในไฟล์ Excel

**อัปเดตล่าสุด: กรกฎาคม 2026**

- [วิธีรับข้อมูลแถวในแผ่นงาน Excel](/cells/rows/get/row/)
- [วิธีเพิ่มแถวว่างในแผ่นงาน Excel](/cells/rows/add/row/)
- [วิธีคัดลอกแถวในแผ่นงาน Excel](/cells/rows/copy/)
- [วิธีซ่อนแถวในแผ่นงาน Excel](/cells/rows/hide/)
- [วิธียกเลิกการซ่อนแถวในแผ่นงาน Excel](/cells/rows/unhide/)
- [วิธีจัดกลุ่มแถวในแผ่นงาน Excel](/cells/rows/group/)
- [วิธียกเลิกการจัดกลุ่มแถวในแผ่นงาน Excel](/cells/rows/ungroup/)
- [วิธีลบแถวจากแผ่นงาน](/cells/rows/delete/)

อ้างอิง API อย่างย่อสำหรับการดำเนินการแถวที่พบบ่อย:

| การดำเนินการ | เมธอด HTTP | ปลายทาง (Endpoint)                                                      | พารามิเตอร์สำคัญ                                   |
|--------------|-------------|--------------------------------------------------------------------------|-----------------------------------------------------|
| [Get Row](https://docs.aspose.cloud/cells/rows/get/row/)     | GET         | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`              | `fileName`, `sheetName`, `rowIndex`                |
| [Add Row](https://docs.aspose.cloud/cells/rows/add/row/)     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows`                         | `rowIndex`, `height`                               |
| [Copy Rows](https://docs.aspose.cloud/cells/rows/copy/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                    | `sourceIndex`, `destinationIndex`, `rowCount`     |
| [Delete Row](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE      | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`              | `fileName`, `sheetName`, `rowIndex`                |
| [Hide Rows](https://docs.aspose.cloud/cells/rows/hide/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                    | `startIndex`, `endIndex`                           |
| [Unhide Rows](https://docs.aspose.cloud/cells/rows/unhide/)  | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                  | `startIndex`, `endIndex`                           |
| [Group Rows](https://docs.aspose.cloud/cells/rows/group/)    | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                   | `startIndex`, `endIndex`                           |
| [Ungroup Rows](https://docs.aspose.cloud/cells/rows/ungroup/)| POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`                 | `startIndex`, `endIndex`                           |

**รายละเอียดคำขอ / การตอบกลับ**

- **Get Row**  
  *คำขอ*: ไม่จำเป็นต้องส่งเนื้อหา (body)  
  *การตอบกลับ (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *ข้อผิดพลาด*: 400 Bad Request (ดัชนีไม่ถูกต้อง), 404 Not Found (ไฟล์หรือแผ่นงานหายไป)

- **Add Row**  
  *เนื้อหาคำขอ (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *การตอบกลับ (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *ข้อผิดพลาด*: 400 Bad Request (พารามิเตอร์หายไปหรือไม่ถูกต้อง), 401 Unauthorized

- **Copy Rows**  
  *เนื้อหาคำขอ (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *การตอบกลับ (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *ข้อผิดพลาด*: 400 Bad Request, 404 Not Found

- **Delete Row**  
  *คำขอ*: ไม่ส่งเนื้อหา (body)  
  *การตอบกลับ (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *ข้อผิดพลาด*: 400 Bad Request, 404 Not Found

- **Hide Rows**  
  *เนื้อหาคำขอ (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *การตอบกลับ (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *ข้อผิดพลาด*: 400 Bad Request

- **Unhide Rows** – เนื้อหาคำขอเหมือนกับ *Hide Rows*; การตอบกลับเหมือนกัน โดยสถานะคือ “Rows unhidden”

- **Group Rows** – เนื้อหาคำขอเหมือนกับ *Hide Rows*; สถานะการตอบกลับคือ “Rows grouped”

- **Ungroup Rows** – เนื้อหาคำขอเหมือนกับ *Hide Rows*; สถานะการตอบกลับคือ “Rows ungrouped”

การดำเนินการทั้งหมดต้องใช้โทเค็นการเข้าถึง OAuth 2.0/JWT ที่ถูกต้อง และเวอร์ชัน SDK ที่เหมาะสม
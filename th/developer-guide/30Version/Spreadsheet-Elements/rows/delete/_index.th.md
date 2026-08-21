---
title: "การจัดการการลบแถวในแผ่นงาน Excel"
second_title: "Document"
linktype: "ลบ"
type: docs
url: /th/rows/delete/
keywords: "Aspose.Cells, delete row, Excel API, REST, cloud, spreadsheet, Excel, SDK"
description: "เรียนรู้วิธีการลบแถวเดียวหรือหลายแถวในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างโค้ดสำหรับ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift"
weight: 20
ArticleTitle: "การจัดการการลบแถวในแผ่นงาน Excel – คู่มือ API ของ Aspose.Cells Cloud"
---

## ประเภทการลบที่มีให้ใช้งาน

ตัวอย่างต่อไปนี้แสดงวิธีการลบแถวว่างหนึ่งแถวหรือหลายแถวจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API

- [วิธีการลบแถวว่างในแผ่นงาน Excel](/cells/rows/delete/row/)
- [วิธีการลบหลายแถวในแผ่นงาน Excel](/cells/rows/delete/rows/)

**ข้อมูลอ้างอิง API**

| รายการ | รายละเอียด |
|---------------------|---------------------------------------------------------------|
| **เมธอด HTTP** | DELETE |
| **จุดปลายทาง (Endpoint)** | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **พารามิเตอร์ในเส้นทาง (Path Parameters)** | `fileName` – ชื่อไฟล์ Excel (จำเป็น)<br>`sheetName` – ชื่อแผ่นงาน (จำเป็น) |
| **พารามิเตอร์คิวรี (Query Parameters)** | `startrow` – ดัชนีของแถวแรกที่ต้องการลบ (จำเป็น)<br>`totalRows` – จำนวนแถวที่ต้องการลบ (จำเป็น)<br>`storage` – ชื่อพื้นที่จัดเก็บบนคลาวด์ (ไม่บังคับ)<br>`folder` – เส้นทางโฟลเดอร์ภายในพื้นที่จัดเก็บ (ไม่บังคับ) |
| **เนื้อความคำขอ (Request Body)** | *ไม่มี* |
| **ตัวอย่างการตอบกลับ (Response Example)** | ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **โค้ดสถานะที่เป็นไปได้ (Possible Status Codes)** | 200 OK – ลบแถวเรียบร้อยแล้ว<br>400 Bad Request – พารามิเตอร์ไม่ถูกต้อง<br>401 Unauthorized – การยืนยันตัวตนล้มเหลว<br>404 Not Found – ไม่พบไฟล์หรือแผ่นงาน<br>500 Internal Server Error – ข้อผิดพลาดที่เกิดจากฝั่งเซิร์ฟเวอร์ |

**ดูเพิ่มเติม**

- [เพิ่มแถว](/cells/rows/add/)
- [ดึงข้อมูลแถว](/cells/rows/get/)
- [คัดลอกแถว](/cells/rows/copy/)
- [ซ่อนแถว](/cells/rows/hide/)
- [ภาพรวมเกี่ยวกับแถว](/cells/rows/)
---
---
---
title: "การใช้งานกราฟใน Excel"
second_title: "เอกสาร"
linktitle: "กราฟ"
type: docs
url: /th/charts/
aliases: [/working-with-charts/]
keywords: "Aspose, Cells, Excel, chart, API, REST, Cloud, spreadsheet"
description: "เรียนรู้วิธีจัดการกราฟใน Excel ด้วย Aspose.Cells Cloud API พร้อมคู่มือแบบทีละขั้นตอน ตัวอย่างโค้ด และการจัดการข้อผิดพลาดสำหรับการดึงข้อมูล กราฟ เพิ่ม กราฟ แก้ไขคุณสมบัติของกราฟ (เช่น หัวเรื่อง แกน และคำอธิบาย) ลบกราฟที่ไม่ต้องการ และแปลงกราฟเป็นรูปภาพสำหรับการรายงานหรือประมวลผลขั้นตอนถัดไป"
weight: 100
ArticleTitle: "การใช้งานกราฟใน Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

## การใช้งานกราฟในไฟล์ Excel

**อัปเดตครั้งล่าสุด:** กรกฎาคม 2026  

กราฟใน Excel คือการแสดงข้อมูลในรูปแบบภาพที่ช่วยให้ผู้ใช้เข้าใจแนวโน้มและรูปแบบของข้อมูลได้อย่างรวดเร็ว  
Aspose.Cells Cloud API ช่วยให้นักพัฒนาสามารถจัดการกราฟเหล่านี้ภายในสมุดงาน Excel ที่เก็บไว้บนคลาวด์ได้อย่างเป็นโปรแกรม โดย API นี้สามารถดึงข้อมูลกราฟที่มีอยู่ สร้างกราฟใหม่ แก้ไขคุณสมบัติของกราฟ (เช่น หัวเรื่อง แกน และคำอธิบาย) ลบกราฟที่ไม่ต้องการ และแปลงกราฟเป็นรูปแบบภาพสำหรับการรายงานหรือการประมวลผลขั้นตอนถัดไป ลิงก์ต่อไปนี้ให้การเข้าถึงหน้ารายละเอียดของการดำเนินการแต่ละประเภทที่เกี่ยวข้องกับกราฟโดยตรง

### ตัวอ้างอิงด่วน

| การดำเนินการ | วิธี HTTP | จุดปลาย (เทมเพลต) | เอกสารประกอบ |
|-----------|-------------|---------------------|---------------|
| ดึงข้อมูลกราฟ | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [ดึงข้อมูลกราฟจากworksheet](/th/cells/get-chart-from-a-worksheet/) |
| เพิ่มกราฟ | POST | `/cells/{file}/worksheets/{sheet}/charts` | [เพิ่มกราฟในworksheet](/th/cells/add-a-chart-in-a-worksheet/) |
| ลบกราฟทั้งหมด | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [ลบกราฟทั้งหมดจากworksheet](/th/cells/delete-all-charts-from-a-worksheet/) |
| ลบกราฟ | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [ลบกราฟจากworksheet](/th/cells/delete-a-chart-from-a-worksheet/) |
| แปลงกราฟเป็นรูปภาพ | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [แปลงกราฟเป็นรูปภาพ](/th/cells/convert-chart-to-image/) |
| ดึงข้อมูลพื้นที่กราฟ | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [ดึงข้อมูลพื้นที่กราฟจากworksheet](/th/cells/get-chart-area-from-a-worksheet/) |
| ดึงข้อมูลรูปแบบการเติมสี | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [ดึงข้อมูลรูปแบบการเติมสีของพื้นที่กราฟจากworksheet](/th/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| ดึงข้อมูลคำอธิบายกราฟ | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [ดึงข้อมูลคำอธิบายกราฟจากworksheet](/th/cells/get-chart-legend-from-a-worksheet/) |
| อัปเดตคำอธิบายกราฟ | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [อัปเดตคำอธิบายกราฟในworksheet](/th/cells/update-chart-legend-in-a-worksheet/) |
| แสดงคำอธิบายกราฟ | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [แสดงคำอธิบายกราฟในworksheet](/th/cells/show-chart-legend-in-a-worksheet/) |
| ซ่อนคำอธิบายกราฟ | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [ซ่อนคำอธิบายกราฟในworksheet](/th/cells/hide-chart-legend-in-a-worksheet/) |
| ดึงข้อมูลหัวเรื่องกราฟ | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [ดึงข้อมูลหัวเรื่องกราฟจากworksheet](/th/cells/get-chart-title-from-a-worksheet/) |
| ตั้งค่าหัวเรื่องกราฟ | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [ตั้งค่าหัวเรื่องกราฟในworksheet ของ Excel](/th/cells/set-chart-title-in-excel-worksheet/) |
| อัปเดตหัวเรื่องกราฟ | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [อัปเดตหัวเรื่องกราฟในworksheet ของ Excel](/th/cells/update-chart-title-in-excel-worksheet/) |
| ลบหัวเรื่องกราฟ | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [ลบหัวเรื่องกราฟในworksheet](/th/cells/delete-chart-title-in-a-worksheet/) |
| อัปเดตคุณสมบัติกราฟ | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [อัปเดตคุณสมบัติกราฟ](/th/cells/charts/properties/update/) |
| ดึงข้อมูลแกนหมวดหมู่ | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [ดึงข้อมูลแกนหมวดหมู่ของกราฟ](/th/cells/charts/category-axis/get/) |
| ดึงข้อมูลแกนค่า | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [ดึงข้อมูลแกนค่าของกราฟ](/th/cells/charts/value-axis/get/) |
| ดึงข้อมูลแกนหมวดหมู่ที่สอง | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [ดึงข้อมูลแกนหมวดหมู่ที่สองของกราฟ](/th/cells/charts/second-category-axis/get/) |
| ดึงข้อมูลแกนค่าที่สอง | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [ดึงข้อมูลแกนค่าที่สองของกราฟ](/th/cells/charts/second-value-axis/get/) |
| อัปเดตแกนหมวดหมู่ | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [อัปเดตแกนหมวดหมู่ของกราฟ](/th/cells/charts/category-axis/update/) |
| อัปเดตแกนค่า | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [อัปเดตแกนค่าของกราฟ](/th/cells/charts/value-axis/update/) |
| อัปเดตแกนหมวดหมู่ที่สอง | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [อัปเดตแกนหมวดหมู่ที่สองของกราฟ](/th/cells/charts/second-category-axis/update/) |
| อัปเดตแกนค่าที่สอง | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [อัปเดตแกนค่าที่สองของกราฟ](/th/cells/charts/second-value-axis/update/) |

- [ดึงข้อมูลกราฟจากworksheet](/th/cells/get-chart-from-a-worksheet/)
- [เพิ่มกราฟในworksheet](/th/cells/add-a-chart-in-a-worksheet/)
- [ลบกราฟทั้งหมดจากworksheet](/th/cells/delete-all-charts-from-a-worksheet/)
- [ลบกราฟจากworksheet](/th/cells/delete-a-chart-from-a-worksheet/)
- [แปลงกราฟเป็นรูปภาพ](/th/cells/convert-chart-to-image/)
- [ดึงข้อมูลพื้นที่กราฟจากworksheet](/th/cells/get-chart-area-from-a-worksheet/)
- [ดึงข้อมูลรูปแบบการเติมสีของพื้นที่กราฟจากworksheet](/th/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [ดึงข้อมูลคำอธิบายกราฟจากworksheet](/th/cells/get-chart-legend-from-a-worksheet/)
- [อัปเดตคำอธิบายกราฟในworksheet](/th/cells/update-chart-legend-in-a-worksheet/)
- [แสดงคำอธิบายกราฟในworksheet](/th/cells/show-chart-legend-in-a-worksheet/)
- [ซ่อนคำอธิบายกราฟในworksheet](/th/cells/hide-chart-legend-in-a-worksheet/)
- [ดึงข้อมูลหัวเรื่องกราฟจากworksheet](/th/cells/get-chart-title-from-a-worksheet/)
- [ตั้งค่าหัวเรื่องกราฟในworksheet ของ Excel](/th/cells/set-chart-title-in-excel-worksheet/)
- [อัปเดตหัวเรื่องกราฟในworksheet ของ Excel](/th/cells/update-chart-title-in-excel-worksheet/)
- [ลบหัวเรื่องกราฟในworksheet](/th/cells/delete-chart-title-in-a-worksheet/)
- [อัปเดตคุณสมบัติกราฟ](/th/cells/charts/properties/update/)
- [ดึงข้อมูลแกนหมวดหมู่ของกราฟ](/th/cells/charts/category-axis/get/)
- [ดึงข้อมูลแกนค่าของกราฟ](/th/cells/charts/value-axis/get/)
- [ดึงข้อมูลแกนหมวดหมู่ที่สองของกราฟ](/th/cells/charts/second-category-axis/get/)
- [ดึงข้อมูลแกนค่าที่สองของกราฟ](/th/cells/charts/second-value-axis/get/)
- [อัปเดตแกนหมวดหมู่ของกราฟ](/th/cells/charts/category-axis/update/)
- [อัปเดตแกนค่าของกราฟ](/th/cells/charts/value-axis/update/)
- [อัปเดตแกนหมวดหมู่ที่สองของกราฟ](/th/cells/charts/second-category-axis/update/)
- [อัปเดตแกนค่าที่สองของกราฟ](/th/cells/charts/second-value-axis/update/)
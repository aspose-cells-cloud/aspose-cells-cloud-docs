---
---
title: "การใช้งานช่วงข้อมูลใน Excel"
second_title: "เอกสาร"
linktype: "ช่วงข้อมูล"
type: docs
url: /ranges/
aliases: [/working-with-ranges/]
keywords: "Aspose.Cells, ช่วงข้อมูล Excel, REST API, SDK, .NET, Java, Python, ผสานเซลล์, คัดลอกช่วงข้อมูล, ตั้งค่าค่าในช่วงข้อมูล"
description: "เรียนรู้วิธีการดึงข้อมูล แก้ไข จัดรูปแบบ ผสาน เคลื่อนย้าย และคัดลอกช่วงข้อมูลใน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างโค้ด SDK สำหรับ .NET, Java, Python และอื่นๆ"
weight: 100
ArticleTitle: "การใช้งานช่วงข้อมูลใน Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

**ช่วงข้อมูล (range)** หมายถึง เซลล์เดียว ทั้งแถว ทั้งคอลัมน์ กลุ่มของเซลล์ที่อยู่ติดกัน หรือช่วงข้อมูลแบบสามมิติ (3-D) ที่ครอบคลุมหลายเวิร์กชีต

## การใช้งานช่วงข้อมูลในไฟล์ Excel

Aspose.Cells Cloud REST API มีจุดปลายทาง (endpoints) สำหรับการจัดการช่วงข้อมูลแต่ละประเภทอย่างเฉพาะเจาะจง รายการต่อไปนี้เชื่อมโยงไปยังตัวอย่างการใช้งานแบบละเอียด และระบุเมธอดและจุดปลายทาง HTTP ที่เกี่ยวข้องไว้ให้ใช้อ้างอิงอย่างรวดเร็ว

- [ดึงข้อมูลช่วงที่ตั้งชื่อไว้ในเวิร์กบุ๊ก](/cells/get-named-ranges-inside-the-workbook/) – ดึงข้อมูลช่วงที่ตั้งชื่อไว้ทั้งหมดในเวิร์กบุ๊ก พร้อมทั้งที่อยู่และขอบเขตของแต่ละช่วง **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`
- [ดึงข้อมูลเซลล์ตามช่วงที่ตั้งชื่อไว้](/cells/get-cells-data-based-on-named-range/) – ดึงค่าของเซลล์ทั้งหมดที่อยู่ในช่วงที่ตั้งชื่อไว้ที่ระบุ **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`
- [ปรับความสูงของแถวในช่วงข้อมูล](/cells/cells/change-heights-of-rows-inside-the-range/) – ปรับความสูงของแต่ละแถวที่อยู่ในช่วงข้อมูลที่กำหนด **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`
- [ปรับความกว้างของคอลัมน์ในช่วงข้อมูล](/cells/cells/change-widths-of-columns-inside-the-range/) – ปรับความกว้างของคอลัมน์ที่ตัดกับช่วงข้อมูลทั้งหมด **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`
- [ผสานเซลล์หลายเซลล์ให้เป็นเซลล์เดียว](/cells/combines-a-range-of-cells-into-a-single-cell/) – ผสานเซลล์ที่เลือกให้เป็นเซลล์เดียว โดยรักษาค่าจากเซลล์บนซ้ายไว้ **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`
- [คัดลอกช่วงข้อมูลภายในเวิร์กชีตพร้อมตัวเลือกการวาง](/cells/copy-range-in-a-worksheet-with-paste-options/) – คัดลอกช่วงต้นทางไปยังช่วงปลายทางพร้อมตัวเลือกการวางแบบต่างๆ (ค่า รูปแบบ สูตร เป็นต้น) **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`
- [ตั้งค่ารูปแบบของช่วงข้อมูล](/cells/set-the-style-of-the-range/) – ใช้รูปแบบตัวอักษร พื้นหลัง เส้นขอบ และการจัดตำแหน่งให้กับเซลล์ทุกเซลล์ในช่วงข้อมูล **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`
- [ยกเลิกการผสานเซลล์ที่ถูกผสานไว้ในช่วงข้อมูล](/cells/unmerge-merged-cells-of-the-range/) – ยกเลิกการผสานที่ทำไว้ก่อนหน้า คืนค่าเซลล์เดิมแต่ละเซลล์กลับมา **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`
- [ย้ายช่วงที่ตั้งชื่อไว้พร้อมกับเวิร์กชีตของ Excel](/cells/move-a-named-ranged-with-a-excel-worksheet/) – ย้ายช่วงที่ตั้งชื่อไว้ไปยังที่อยู่ใหม่ภายในเวิร์กชีตเดียวกัน หรือไปยังเวิร์กชีตอื่น **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`
- [ตั้งค่าค่าของช่วงข้อมูลในเวิร์กชีต Excel](/cells/ranges/set-value/) – เขียนค่าเดียวหรืออาร์เรย์ของค่าลงในช่วงข้อมูลที่ระบุ **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`

คำร้องขอและคำตอบทั้งหมดอยู่ในรูปแบบ JSON ต้องใส่ส่วนหัว `Authorization` พร้อมโทเคนการเข้าถึงของคุณเพื่อการยืนยันตัวตน
---
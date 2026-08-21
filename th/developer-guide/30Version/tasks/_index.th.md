---
title: "งาน (Tasks)"
second title: "เอกสาร"
type: docs
url: /th/tasks/
aliases: [  /th/working-with-tasks/ ]
keywords: "Aspose Cells, Cloud API, งาน Excel, งานแปลง, งาน ImportData, SmartMarker, SaveResult, REST API, อัตโนมัติสเปรดชีต"
description: "สำรวจชุดคุณสมบัติเต็มรูปแบบของ Aspose.Cells Cloud Tasks API: แปลง, ImportData, SaveResult, SmartMarker และอื่นๆ อีกมากมาย เรียนรู้วิธีการใช้งาน พารามิเตอร์ และตัวอย่างโค้ดสำหรับการอัตโนมัติ Excel"
weight: 100
ArticleTitle: "Aspose.Cells Cloud Tasks API"
---

## การทำงานกับงาน (Tasks)

Aspose.Cells Cloud มี **Tasks API** ที่ช่วยให้นักพัฒนาสามารถดำเนินการต่างๆ กับสมุดงาน Excel ได้อย่างหลากหลาย เช่น การแปลงรูปแบบ การนำเข้าข้อมูล การประมวลผลแม่แบบ SmartMarker และการบันทึกผลลัพธ์ งานจะถูกดำเนินการแบบไม่บล็อก (asynchronously): คุณสร้างงาน รันงาน และดึงผลลัพธ์กลับมา

**ข้อกำหนดเบื้องต้น:** บัญชี Aspose Cloud ที่มีคีย์ API ที่ใช้งานได้ รูปแบบไฟล์ Excel ที่รองรับ และเวอร์ชัน Cells API ล่าสุด (v3.0 ขึ้นไป)

- [ไฟล์คำขอการสนับสนุนใน Tasks API](/th/cells/support-request-file-in-task-api/) – ช่วยให้คุณอัปโหลดไฟล์ไปยังพื้นที่จัดเก็บบนคลาวด์ และอ้างอิงไฟล์นั้นในงานถัดไป ทำให้มั่นใจได้ว่าไฟล์พร้อมใช้งานสำหรับการประมวลผล
- [การทำงานกับงาน CellsObjectOperate](/th/cells/working-with-cellsobjectoperate-task/) – ดำเนินการกับวัตถุเซลล์ (เช่น แถว, คอลัมน์) ภายในสมุดงาน เช่น การเพิ่ม ลบ หรืออัปเดตค่าเซลล์
- [การทำงานกับงาน Convert](/th/cells/working-with-convert-task/) – แปลงสมุดงานเป็นรูปแบบ PDF, HTML, CSV หรือ JSON โดยมีตัวเลือกสำหรับช่วงหน้ากระดาษ การป้องกันด้วยรหัสผ่าน และการตั้งค่าการแปลงแบบกำหนดเอง
- [การทำงานกับงาน ImportData](/th/cells/working-with-importdata-task/) – นำเข้าข้อมูลจากไฟล์ CSV, JSON หรือ XML ลงในชีตงาน โดยแมปคอลัมน์กับเซลล์ และสามารถระบุแถวและคอลัมน์เริ่มต้นได้ตามต้องการ
- [การทำงานกับงาน SaveResult](/th/cells/working-with-saveresult-task/) – บันทึกผลลัพธ์ของงานที่รันก่อนหน้านี้ (เช่น ไฟล์ที่แปลงแล้ว) กลับไปยังพื้นที่จัดเก็บบนคลาวด์ หรือส่งกลับในคำขอตอบกลับ
- [การทำงานกับงาน SmartMarker](/th/cells/working-with-smartmarker-task/) – ประมวลผลสมุดงานที่มีแท็ก SmartMarker (เช่น `{{Customer.Name}}`) โดยใช้แหล่งข้อมูล JSON เพื่อสร้างรายงานที่เต็มไปด้วยข้อมูล
- [การทำงานกับ WorksheetOperates ใน Tasks API](/th/cells/working-with-worksheetoperates-in-task-api/) – ดำเนินการระดับชีตงาน เช่น การเพิ่ม ลบ หรือเปลี่ยนชื่อชีตงาน ภายในเวิร์กโฟลว์ของงาน

สำหรับข้อมูลรายละเอียดของเมธอดทั้งหมด รวมถึง HTTP verbs, URL ของ endpoint, โครงสร้างคำขอ-คำตอบ, ตารางพารามิเตอร์ และตัวอย่าง payload โปรดดูที่หน้างานแต่ละหน้าที่เชื่อมโยงไว้ด้านบน ข้อมูลอ้างอิง API แบบละเอียดนี้จะช่วยให้นักพัฒนาสามารถผสานรวม Tasks API ได้อย่างรวดเร็วและเชื่อถือได้
---
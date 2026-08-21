---
title: "การใช้งานวัตถุ OLE ใน Excel"
second_title: "เอกสาร"
linktitle: "OleObjects"
type: docs
url: /th/oleobjects/
aliases: [/th/working-with-oleobjects/]
keywords: "OLE, Excel, Aspose.Cells, API, Cloud"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อดึงข้อมูล เพิ่ม แก้ไข ลบ และแปลงวัตถุ OLE ในแผ่นงาน Excel ซึ่งมี SDK ให้ใช้งานในภาษา Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift และ Android"
weight: 100
ArticleTitle: "การใช้งานวัตถุ OLE ใน Excel – คู่มือการดึงข้อมูล เพิ่ม แก้ไข ลบ และแปลงวัตถุ OLE"
---

**วิธีการใช้งานวัตถุ OLE ในแผ่นงาน Excel**

Aspose.Cells Cloud REST API จัดเตรียมชุดการดำเนินการที่สมบูรณ์สำหรับจัดการวัตถุ OLE ด้วยการเขียนโปรแกรม ด้านล่างนี้คือข้อมูลอ้างอิงแบบย่อสำหรับแต่ละการดำเนินการ ซึ่งประกอบด้วย HTTP method, รูปแบบ endpoint, พารามิเตอร์ที่จำเป็น และตัวอย่างการตอบกลับสั้นๆ

- [วิธีการดึงข้อมูลวัตถุ OLE จากแผ่นงาน Excel](/th/cells/oleobjects/get/)
  - **Method:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **พารามิเตอร์:** `fileName` (string), `sheetName` (string), `oleObjectIndex` (integer)  
  - **ตัวอย่างการตอบกลับ:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [วิธีการเพิ่มวัตถุ OLE ลงในแผ่นงาน Excel](/th/cells/oleobjects/add/)
  - **Method:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **พารามิเตอร์:** `fileName`, `sheetName`, `oleObject` (binary หรือ base‑64), `imageFormat` (ไม่บังคับ)  
  - **ตัวอย่างเนื้อหาคำขอ:** multipart/form‑data พร้อมสตรีมไฟล์  
  - **ตัวอย่างการตอบกลับ:** `201 Created` พร้อม header location ของวัตถุ OLE ใหม่

- [วิธีการอัปเดตวัตถุ OLE ที่ระบุในแผ่นงาน Excel](/th/cells/oleobjects/update/)
  - **Method:** `PUT`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **พารามิเตอร์:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (เนื้อหาที่อัปเดต)  
  - **ตัวอย่างการตอบกลับ:** `200 OK` พร้อม metadata ของวัตถุที่อัปเดต

- [วิธีการแปลงวัตถุ OLE เป็นภาพในแผ่นงาน Excel](/th/cells/oleobjects/convert/)
  - **Method:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **พารามิเตอร์:** `fileName`, `sheetName`, `oleObjectIndex`, `format` (เช่น `png`, `jpeg`)  
  - **ตัวอย่างการตอบกลับ:** สตรีมภาพแบบไบนารีของวัตถุ OLE ที่แปลงแล้ว

- [วิธีการล้างวัตถุ OLE ทั้งหมดในแผ่นงาน Excel](/th/cells/oleobjects/clear/)
  - **Method:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **พารามิเตอร์:** `fileName`, `sheetName`  
  - **ตัวอย่างการตอบกลับ:** `204 No Content` ซึ่งระบุว่าวัตถุ OLE ทั้งหมดถูกลบออกแล้ว

- [วิธีการลบวัตถุ OLE ที่ระบุในแผ่นงาน Excel](/th/cells/oleobjects/delete/)
  - **Method:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **พารามิเตอร์:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **ตัวอย่างการตอบกลับ:** `204 No Content` ยืนยันว่าวัตถุดังกล่าวถูกลบแล้ว
---
---
title: "การทำงานกับการจัดรูปแบบตามเงื่อนไขใน Excel"
second_title: "เอกสาร"
linktype: "การจัดรูปแบบตามเงื่อนไข"
type: docs
url: /conditional-formattings/
aliases: [/working-with-conditional-formatting/]
keywords: "Excel, การจัดรูปแบบตามเงื่อนไข, Aspose.Cells Cloud, API"
description: "API ของ Aspose.Cells Cloud สำหรับ Excel มีเอนด์พอยต์ให้ใช้งานเพื่อดึงข้อมูล เพิ่ม แก้ไข และล้างกฎการจัดรูปแบบตามเงื่อนไข ช่วยให้คุณสามารถวิเคราะห์ข้อมูลในชีตงานแบบไดนามิกผ่านการแสดงผลแบบภาพ"
weight: 100
ArticleTitle: "การทำงานกับการจัดรูปแบบตามเงื่อนไขใน Excel – คู่มือ API"
---

การจัดรูปแบบตามเงื่อนไขใน Excel ช่วยให้คุณเน้นสีของเซลล์ตามค่าของเซลล์นั้นๆ

ใช้การจัดรูปแบบตามเงื่อนไขเพื่อช่วยคุณสำรวจและวิเคราะห์ข้อมูลด้วยภาพ ตรวจจับปัญหาที่สำคัญ และระบุรูปแบบหรือแนวโน้ม

การจัดรูปแบบตามเงื่อนไขทำให้ง่ายต่อการเน้นเซลล์หรือช่วงของเซลล์ที่น่าสนใจ เน้นค่าที่ผิดปกติ และแสดงผลข้อมูลด้วยแท่งข้อมูล (data bars), มาตรสี (color scales), และชุดไอคอน (icon sets) ที่สอดคล้องกับความแปรปรวนเฉพาะของข้อมูล

รูปแบบตามเงื่อนไขจะเปลี่ยนลักษณะการแสดงผลของเซลล์ตามเงื่อนไขที่คุณกำหนดไว้ หากเงื่อนไขเป็นจริง เซลล์หรือช่วงเซลล์จะถูกจัดรูปแบบ; หากเงื่อนไขเป็นเท็จ เซลล์หรือช่วงเซลล์จะไม่มีการเปลี่ยนแปลงใดๆ มีเงื่อนไขปริยายมาให้หลายแบบ คุณยังสามารถสร้างเงื่อนไขของตนเองได้ (รวมถึงโดยใช้สูตรที่ให้ผลลัพธ์เป็น **TRUE** หรือ **FALSE**)

API ของ Aspose.Cells Cloud มีชุดของเอนด์พอยต์ให้จัดการกฎการจัดรูปแบบตามเงื่อนไขด้วยการเขียนโค้ด ดำเนินการที่มีอยู่มีดังนี้:

- **ดึงข้อมูลการจัดรูปแบบตามเงื่อนไขของชีตงาน** – ดึงกฎการจัดรูปแบบตามเงื่อนไขทั้งหมดที่ใช้กับชีตงาน  
  - **เมธอด:** `GET`  
  - **เอนด์พอยต์:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **พารามิเตอร์:** `fileName` (สตริง, จำเป็น), `sheetName` (สตริง, จำเป็น), พารามิเตอร์แบบคิวรีแบบไม่บังคับ เช่น `folder`, `storageName`  
  - **ตัวอย่าง cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **ดึงข้อมูลการจัดรูปแบบตามเงื่อนไข** – ส่งคืนกฎการจัดรูปแบบตามเงื่อนไขเฉพาะโดยใช้ตัวระบุของกฎนั้น  
  - **เมธอด:** `GET`  
  - **เอนด์พอยต์:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **พารามิเตอร์:** `index` (จำนวนเต็ม, จำเป็น) ระบุตำแหน่งของกฎ  
  - **ตัวอย่าง cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **เพิ่มพื้นที่เซลล์สำหรับเงื่อนไขการจัดรูปแบบ** – เพิ่มช่วงเซลล์ที่รูปแบบตามเงื่อนไขที่ระบุจะส่งผล  
  - **เมธอด:** `POST`  
  - **เอนด์พอยต์:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **เนื้อหาคำขอ (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **ตัวอย่าง cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **เพิ่มเงื่อนไขสำหรับการจัดรูปแบบ** – นิยามเงื่อนไขใหม่ (เช่น ค่า, สูตร) สำหรับกฎการจัดรูปแบบที่มีอยู่  
  - **เมธอด:** `POST`  
  - **เอนด์พอยต์:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **เนื้อหาคำขอ (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **ตัวอย่าง cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **เพิ่มเงื่อนไขการจัดรูปแบบ** – สร้างกฎการจัดรูปแบบตามเงื่อนไขที่สมบูรณ์ รวมถึงประเภทและรูปแบบ  
  - **เมธอด:** `POST`  
  - **เอนด์พอยต์:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **เนื้อหาคำขอ (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **ตัวอย่าง cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **ล้างการจัดรูปแบบตามเงื่อนไขทั้งหมด** – ลบกฎการจัดรูปแบบตามเงื่อนไขทั้งหมดออกจากชีตงานเป้าหมาย  
  - **เมธอด:** `DELETE`  
  - **เอนด์พอยต์:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **ตัวอย่าง cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **ลบพื้นที่เซลล์ออกจากการจัดรูปแบบตามเงื่อนไข** – ลบพื้นที่เซลล์ที่กำหนดไว้ก่อนหน้านี้ออกจากกฎการจัดรูปแบบตามเงื่อนไข  
  - **เมธอด:** `DELETE`  
  - **เอนด์พอยต์:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **ตัวอย่าง cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **ลบการจัดรูปแบบตามเงื่อนไข** – ลบกฎการจัดรูปแบบตามเงื่อนไขทั้งกฎออกจากชีตงาน  
  - **เมธอด:** `DELETE`  
  - **เอนด์พอยต์:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **ตัวอย่าง cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

ตัวอย่างเหล่านี้แสดงเมธอด HTTP ที่จำเป็น รูปแบบ URL พารามิเตอร์สำคัญ และตัวอย่างเนื้อหาคำขอสำหรับแต่ละการดำเนินการ คุณสามารถใช้ SDK ที่เหมาะสม (C#, Java, Python เป็นต้น) เพื่อเรียกดูตัวอย่างโค้ดที่เขียนด้วยภาษาเฉพาะได้หากต้องการ
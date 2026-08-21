---
title: "ตั้งค่ารูปแบบช่วง – Aspose.Cells Cloud API"
second_title: "เอกสารประกอบ"
linktitle: "ตั้งค่ารูปแบบช่วง"
type: docs
url: /ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: "Aspose.Cells, รูปแบบช่วง, API, Excel, คลาวด์"
description: "เรียนรู้วิธีการตั้งค่ารูปแบบของช่วงเซลล์ในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API รวมถึงขั้นตอนการยืนยันตัวตน รูปแบบคำขอ รายละเอียดการตอบกลับ และตัวอย่าง SDK สำหรับ .NET, Java, Python, Go และอื่นๆ"
weight: 70
---

## **บทนำ**
ตัวอย่างนี้แสดงวิธีการตั้งค่ารูปแบบของช่วงโดยใช้ Aspose.Cells Cloud API คุณสามารถเรียก API จากภาษาโปรแกรมหลายภาษา เช่น .NET, Java, PHP, Ruby, Python, JavaScript (jQuery) และอื่นๆ

## **ข้อมูล API**

| API                                                   | ประเภท | คำอธิบาย                          | ลิงก์ทรัพยากร                                                                                                                                 |
| ----------------------------------------------------- | ------ | ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST   | ตั้งค่ารูปแบบเซลล์ของช่วงที่ตั้งชื่อไว้ | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **ตัวอย่าง cURL**

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

**ข้อกำหนดเบื้องต้น**  
1. รับโทเคนการเข้าถึงผ่านขั้นตอน OAuth2 client-credentials flow (`POST https://api.aspose.cloud/connect/token`)  
2. ใส่เฮเดอร์ `Authorization: Bearer <access_token>` ในทุกคำขอ  

**คำขอ**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*ออบเจกต์ `Range` ระบุเซลล์มุมซ้ายบนและขนาดของช่วง ส่วนออบเจกต์ `Style` ประกอบด้วยตัวเลือกการจัดรูปแบบที่จะใช้*

{{< /tab >}}

{{< tab tabNum="2" >}}

**การตอบกลับ**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**การจัดการข้อผิดพลาด** – เมื่อคำขอไม่สำเร็จ API จะส่งกลับโค้ดสถานะ HTTP ที่เหมาะสม (เช่น 400, 401, 500) พร้อมกับเนื้อหา JSON ที่มีฟิลด์ `Error` และ `Message` ตรวจสอบค่า `Code` โดยค่าที่ไม่ใช่ 200 ควรบันทึกและดำเนินการตามนโยบายการจัดการข้อผิดพลาดของคุณ

{{< /tab >}}

{{< /tabs >}}

## **ซอร์สโค้ด SDK**
สามารถดาวน์โหลด SDK ของ Aspose.Cells Cloud ได้จากหน้านี้: [SDK ที่พร้อมใช้งาน](/cells/available-sdks/)

### **ตัวอย่าง SDK**
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
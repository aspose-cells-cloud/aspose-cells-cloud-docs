---
title: "การลบแถวในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "แถว"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
description: "ใช้ปลายทาง DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} เพื่อลบแถวที่ระบุออกจากแผ่นงาน Excel ผ่าน Aspose.Cells Cloud REST API ประกอบด้วยคำสั่ง cURL ตัวอย่าง SDK และการอ้างอิงพารามิเตอร์แบบเต็ม"
keywords: "Aspose.Cells, ลบแถว, Excel, API, REST, คลาวด์, SDK"
weight: 80
ArticleTitle: "การลบแถวในแผ่นงาน Excel – คู่มือ API ของ Aspose.Cells Cloud"
---

REST API นี้ใช้ลบแถวออกจากแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น**  
- โทเคน JWT สำหรับ **การอนุญาต** ที่ถูกต้อง  
- สมุดงานต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud ที่รองรับ (ค่าเริ่มต้นหรือแบบกำหนดเอง)  
- โฟลเดอร์เป้าหมาย (หากระบุ) ต้องมีอยู่ในพื้นที่จัดเก็บที่เลือก

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **พารามิเตอร์คำขอ**

| พารามิเตอร์        | ชนิดข้อมูล | Path / Query | จำเป็น | คำอธิบาย                                                                                      |
| ------------------ | ---------- | ------------ | ------ | ---------------------------------------------------------------------------------------------- |
| **name**           | string     | path         | ใช่    | ชื่อสมุดงาน                                                                                   |
| **sheetName**      | string     | path         | ใช่    | ชื่อแผ่นงาน                                                                                   |
| **rowIndex**       | integer    | path         | ใช่    | ดัชนีแบบเริ่มต้นที่ 0 ของแถวที่ต้องการลบ                                                      |
| **startrow**       | integer    | query        | ไม่บังคับ | ดัชนีของแถวแรกที่ต้องการลบ (โดยทั่วไปจะเหมือนกับ `rowIndex`)                                   |
| **totalRows**      | integer    | query        | ไม่บังคับ | จำนวนแถวต่อเนื่องที่ต้องการลบ                                                                  |
| **updateReference** | boolean   | query        | ไม่บังคับ | เมื่อตั้งค่าเป็น `true` (ค่าเริ่มต้น) สูตร ช่วงชื่อ และการอ้างอิงอื่นๆ จะถูกปรับปรุงหลังการลบ |
| **folder**         | string     | query        | ไม่บังคับ | โฟลเดอร์ที่เก็บสมุดงาน                                                                        |
| **storageName**    | string     | query        | ไม่บังคับ | ชื่อของบริการพื้นที่จัดเก็บ                                                                   |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่ใช้งานผ่านบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงคำสั่งที่สมบูรณ์และสามารถรันได้

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

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

**รหัสการตอบกลับ HTTP ที่เป็นไปได้**

| รหัส | ความหมาย                             | คำอธิบาย                                                                      |
|------|---------------------------------------|-------------------------------------------------------------------------------|
| 200  | OK (สำเร็จ)                          | ลบแถวเรียบร้อยแล้ว                                                           |
| 400  | Bad Request (คำขอไม่ถูกต้อง)         | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น `rowIndex` ที่ไม่ใช่ตัวเลข)           |
| 401  | Unauthorized (ไม่ได้รับอนุญาต)       | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                               |
| 404  | Not Found (ไม่พบ)                     | สมุดงาน แผ่นงาน หรือแถวที่ระบุไม่มีอยู่                                       |
| 500  | Internal Server Error (ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์; ดูการตอบกลับข้อผิดพลาดเพื่อดูรายละเอียด |

**ตัวอย่างการตอบกลับข้อผิดพลาด**

```json
{
  "Code": 400,
  "Message": "ดัชนีแถวที่ระบุไม่ถูกต้อง"
}
```

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

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

**การดำเนินการที่เกี่ยวข้อง**  
- [เพิ่มแถว](/cells/rows/add/row/)  
- [ลบหลายแถว](/cells/rows/delete/rows/)  
- [รับรายละเอียดแถว](/cells/rows/get/row/)  
---
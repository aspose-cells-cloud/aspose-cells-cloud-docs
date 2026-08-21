---
title: "AutoFitterOptions – คุณสมบัติและคู่มือการใช้งาน | Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "AutoFitterOptions"
type: docs
url: /auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, ปรับขนาดอัตโนมัติใน Excel, ความสูงของแถว, ช่องที่รวม, API"
description: "เรียนรู้วิธีควบคุมการปรับความสูงของแถวอัตโนมัติ การจัดการช่องที่รวม การแสดง/ซ่อนแถว/คอลัมน์ การตั้งค่าภาษา และตัวเลือกการเรนเดอร์ด้วยวัตถุ AutoFitterOptions ใน Aspose.Cells Cloud API"
weight: 79
ArticleTitle: "AutoFitterOptions – คู่มือคุณสมบัติและวิธีใช้งานสำหรับ Aspose.Cells Cloud"
---

# คุณสมบัติของ AutoFitterOptions

วัตถุ `AutoFitterOptions` ช่วยให้คุณปรับแต่งการปรับความสูงของแถวอัตโนมัติที่ดำเนินการโดย Aspose.Cells Cloud ได้อย่างละเอียด คุณสมบัตินี้มีประโยชน์เมื่อคุณต้องการควบคุมการจัดการช่องที่รวม การแสดง/ซ่อนแถว/คอลัมน์ การจัดรูปแบบตามภาษา หรือพฤติกรรมที่เกี่ยวข้องกับการเรนเดอร์อย่างแม่นยำ

**ข้อกำหนดเบื้องต้น** – เพื่อใช้งานตัวเลือกเหล่านี้ คุณต้องยืนยันตัวตนด้วยโทเค็นการเข้าถึง OAuth 2.0 ที่ถูกต้องซึ่งมีขอบเขต **Cells.ReadWrite** การร้องขอจะทำงานได้กับ SDK เวอร์ชันใดก็ตามที่รองรับ API เวอร์ชัน 3.0

| ชื่อ                      | ชนิดข้อมูล | คำอธิบาย                                                                                     | หมายเหตุ                                                                                                       |
| -------------------------- | ----------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | กำหนดวิธีการปรับขนาดอัตโนมัติสำหรับช่องที่รวม                                                         | ค่าที่อนุญาต: `All`, `First`, `None` ค่าเริ่มต้น: `All` ตัวอย่าง JSON: `"AutoFitMergedCellsType":"All"`       |
| **IgnoreHidden**           | **boolean** | เมื่อตั้งค่าเป็น **true** จะละเว้นแถวและคอลัมน์ที่ซ่อนอยู่ระหว่างกระบวนการปรับขนาดอัตโนมัติ                 | ค่าเริ่มต้น: `false` ตัวอย่าง JSON: `"IgnoreHidden":false`                                                       |
| **OnlyAuto**               | **boolean** | ระบุว่าจะปรับขนาดอัตโนมัติเฉพาะแถวที่ไม่ได้ปรับความสูงด้วยตนเองเท่านั้นหรือไม่                             | ค่าเริ่มต้น: `false` ตัวอย่าง JSON: `"OnlyAuto":false`                                                           |
| **DefaultEditLanguage**    | **string**  | ตั้งค่าภาษาสำหรับการแก้ไขเริ่มต้นสำหรับสมุดงาน                                                            | ค่าเริ่มต้น: ภาษาของระบบ (เช่น `"en-US"`) ตัวอย่าง JSON: `"DefaultEditLanguage":"en-US"`                    |
| **MaxRowHeight**           | **double**  | ความสูงสูงสุดของแถว (หน่วยเป็นจุด) ที่ใช้เมื่อปรับขนาดอัตโนมัติ ค่า **0** หมายถึงไม่มีข้อจำกัด               | ค่าเริ่มต้น: `0` ตัวอย่าง JSON: `"MaxRowHeight":0`                                                               |
| **AutoFitWrappedTextType** | **string**  | ควบคุมวิธีการปรับขนาดอัตโนมัติสำหรับข้อความที่ขึ้นบรรทัดใหม่ภายในช่อง                                         | ค่าที่อนุญาต: `All`, `OnlyWrapped`, `None` ค่าเริ่มต้น: `All` ตัวอย่าง JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | ระบุกลยุทธ์การจัดรูปแบบที่ใช้ระหว่างการดำเนินการปรับขนาดอัตโนมัติ                                      | ค่าที่พบบ่อย: `AutoFit`, `PreserveExisting` ค่าเริ่มต้น: `AutoFit` ตัวอย่าง JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | ระบุว่าจะดำเนินการปรับขนาดอัตโนมัติเพื่อวัตถุประสงค์ในการเรนเดอร์ (เช่น PDF, รูปภาพ) หรือไม่                | ค่าที่อนุญาต: `True`, `False` ค่าเริ่มต้น: `False` ตัวอย่าง JSON: `"ForRendering":"False"`                    |

ด้านล่างคือตัวอย่างพาร์ต JSON ที่สามารถส่งไปยัง API ได้เมื่อกำหนดค่า `AutoFitterOptions`

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

คำขอ `cURL` ตัวอย่างที่ใช้ตัวเลือกเหล่านี้กับสมุดงาน:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**การอ้างอิงจุดปลายทาง**

| เมธอด | URL | พารามิเตอร์ที่จำเป็น | คำอธิบาย |
|--------|-----|---------------------|-------------|
| PUT    | `/cells/workbook/autoFitter` | `autoFitterOptions` (เนื้อหา JSON) | ใช้ค่า `AutoFitterOptions` ที่ระบุกับสมุดงานเป้าหมาย |
| GET    | `/cells/workbook/autoFitter` | *ไม่มี* | ดึงการตั้งค่า `AutoFitterOptions` ปัจจุบันของสมุดงาน |

**พารามิเตอร์ร้องขอสำหรับจุดปลายทาง PUT**

| พารามิเตอร์              | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|--------------------------|---------|----------|-------------|
| AutoFitMergedCellsType   | string  | จำเป็น   | วิธีการปรับขนาดอัตโนมัติสำหรับช่องที่รวม (`All`, `First`, `None`) |
| IgnoreHidden             | boolean | ไม่จำเป็น | ระบุว่าจะละเว้นแถว/คอลัมน์ที่ซ่อนอยู่หรือไม่ |
| OnlyAuto                 | boolean | ไม่จำเป็น | ปรับขนาดเฉพาะแถวที่ไม่มีการตั้งค่าความสูงด้วยตนเอง |
| DefaultEditLanguage      | string  | ไม่จำเป็น | ภาษาสำหรับการแก้ไข (เช่น `en-US`) |
| MaxRowHeight             | double  | ไม่จำเป็น | ความสูงสูงสุดของแถวเป็นหน่วยจุด; `0` = ไม่จำกัด |
| AutoFitWrappedTextType   | string  | ไม่จำเป็น | วิธีการจัดการข้อความที่ขึ้นบรรทัดใหม่ (`All`, `OnlyWrapped`, `None`) |
| FormatStrategy           | string  | ไม่จำเป็น | กลยุทธ์การจัดรูปแบบ (`AutoFit`, `PreserveExisting`) |
| ForRendering             | string  | ไม่จำเป็น | ใช้การปรับขนาดอัตโนมัติสำหรับการเรนเดอร์ (`True`, `False`) |

โค้ดการตอบกลับที่พบบ่อย:

- **200 OK** – ดำเนินการเสร็จสมบูรณ์อย่างประสบความสำเร็จ  
- **400 Bad Request** – พาร์ต JSON ไม่ถูกต้องหรือค่าที่ไม่รองรับ  
- **401 Unauthorized** – ไม่มีโทเค็นการยืนยันตัวตนหรือโทเค็นไม่ถูกต้อง  
- **500 Internal Server Error** – เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด

**ตัวอย่างการตอบกลับ GET**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

ตัวอย่างเหล่านี้แสดงวิธีการกำหนดค่าและเรียกใช้โมเดล `AutoFitterOptions` ภายใน Aspose.Cells Cloud API
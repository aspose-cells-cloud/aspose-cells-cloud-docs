---
---
title: "การเพิ่มหรือลบภาพพื้นหลังของแผ่นงาน – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "พื้นหลัง"
type: docs
url: /worksheets/background/
keywords: "Aspose.Cells Cloud, ภาพพื้นหลังของแผ่นงาน, Excel API, เพิ่มภาพพื้นหลัง, ลบภาพพื้นหลังของแผ่นงาน, ตัวอย่าง SDK"
description: "เรียนรู้วิธีการเพิ่มหรือลบภาพพื้นหลังของแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API รวมถึงไวยากรณ์คำขอ ตัวอย่าง SDK สำหรับ Java, .NET, Python, PHP และการจัดการข้อผิดพลาด"
weight: 20
ArticleTitle: "การเพิ่มหรือลบภาพพื้นหลังของแผ่นงานด้วย Aspose.Cells Cloud API"
---

## การทำงานกับพื้นหลังของแผ่นงาน Excel

**ภาพรวม:** พื้นหลังของแผ่นงานคือภาพที่ปรากฏอยู่ด้านหลังของเซลล์ในแผ่นงาน ซึ่งมีประโยชน์สำหรับการสร้างแบรนด์หรือสื่อสัญญาณเชิงภาพ Aspose.Cells Cloud API ช่วยให้คุณสามารถเพิ่มหรือลบภาพพื้นหลังนี้ได้อย่างเป็นโปรแกรม

**ข้อกำหนดเบื้องต้น:**  
- โทเคนการเข้าถึง Aspose.Cells Cloud ที่ถูกต้อง (OAuth 2.0)  
- สมุดงาน Excel ที่ถูกจัดเก็บไว้บนคลาวด์  
- ไฟล์ภาพ (PNG, JPEG, BMP) สำหรับใช้เป็นพื้นหลัง

- **เพิ่มพื้นหลัง** – ตั้งค่าภาพพื้นหลังให้กับแผ่นงาน ดูคู่มืออย่างละเอียดได้ที่ [วิธีการตั้งค่าพื้นหลังในแผ่นงาน Excel](/cells/worksheets/background/add/)  
- **ลบพื้นหลัง** – ลบภาพพื้นหลังที่มีอยู่ออกจากแผ่นงาน ดูคู่มืออย่างละเอียดได้ที่ [วิธีการลบพื้นหลังในแผ่นงาน Excel](/cells/worksheets/background/delete/)

การใช้ภาพพื้นหลังของแผ่นงานสามารถช่วยเสริมแบรนด์ สื่อถึงส่วนที่สำคัญ หรือให้สัญญาณเชิงภาพแก่ผู้ใช้งานสุดท้าย API ของ Aspose.Cells Cloud ทำให้คุณสามารถตั้งค่าหรือล้างภาพพื้นหลังนี้ได้อย่างง่ายดายโดยตรงจากแอปพลิเคชันของคุณ

### การอ้างอิง API

| การดำเนินการ | HTTP Method | Endpoint | พารามิเตอร์เส้นทาง | เนื้อหาคำขอ | การตอบกลับเมื่อสำเร็จ |
|-----------|-------------|----------|----------------|--------------|------------------|
| เพิ่มพื้นหลัง | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – ชื่อไฟล์สมุดงาน<br>`sheetName` – ชื่อแผ่นงานเป้าหมาย | ไฟล์ภาพ (PNG, JPEG, BMP) ในรูปแบบ multipart/form‑data | `200 OK` – พื้นหลังถูกใช้งานแล้ว |
| ลบพื้นหลัง | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – ชื่อไฟล์สมุดงาน<br>`sheetName` – ชื่อแผ่นงานเป้าหมาย | *ไม่มี* | `200 OK` – พื้นหลังถูกลบออกแล้ว |

#### ตัวอย่าง (SDK สำหรับ Java)

```java
// เพิ่มภาพพื้นหลัง
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// ลบภาพพื้นหลัง
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### ตัวอย่าง (SDK สำหรับ Python)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# เพิ่มพื้นหลัง
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# ลบพื้นหลัง
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

สำหรับตัวอย่างในภาษาอื่นๆ (C#, PHP, Ruby) โปรดอ้างอิงที่เอกสาร SDK

**หัวข้อที่เกี่ยวข้อง**  
- เรียนรู้เพิ่มเติมเกี่ยวกับการจัดการแผ่นงานโดยทั่วไป: [ภาพรวมแผ่นงาน](/cells/worksheets/)  
- เข้าใจวิธีการยืนยันตัวตนกับ Aspose.Cells Cloud: [คู่มือการยืนยันตัวตน API](/cells/authentication/)  
- สำรวจองค์ประกอบของสเปรดชีตอื่นๆ เช่น แผนภูมิ ตาราง และสูตร: [ดัชนีองค์ประกอบสเปรดชีต](/cells/elements/)
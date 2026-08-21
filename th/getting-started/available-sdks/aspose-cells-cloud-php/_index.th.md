---
---  
title: "Aspose.Cells Cloud PHP SDK – แปลง ผูก แยก และป้องกันไฟล์ Excel"  
second_title: "เอกสาร"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – แปลง ผูก แยก และป้องกันไฟล์ Excel"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /available-sdks/aspose-cells-cloud-php/  
description: "ดาวน์โหลด Aspose.Cells Cloud PHP SDK (v24.3) เรียนรู้วิธีติดตั้งผ่าน Composer ยืนยันตัวตน แปลง XLSX เป็น PDF/CSV ผูกสมุดงาน ป้องกันแผ่นงาน และอื่นๆ – ทั้งหมดนี้โดยไม่ต้องติดตั้ง Office"  
keywords: "Aspose.Cells, Cloud, PHP, SDK, Excel, แปลง, ผูก, แยก, ป้องกัน"  
weight: 30  
---  

SDK นี้เป็นโอเพนซอร์สและอยู่ภายใต้ใบอนุญาต MIT License คุณสามารถเข้าถึงซอร์สโค้ดไลบรารี PHP สำหรับ Aspose.Cells Cloud ได้ <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">ที่นี่</a>

# **วิธีใช้ Aspose.Cells Cloud SDK สำหรับ PHP**

Aspose.Cells Cloud SDK สำหรับ PHP เป็นไลบรารีที่ทรงพลังซึ่งช่วยให้นักพัฒนาสามารถจัดการและประมวลผลไฟล์ Microsoft Excel โดยใช้ **ภาษาโปรแกรมมิ่ง PHP** ด้วย SDK นี้ คุณสามารถสร้าง แก้ไข และแปลงเอกสาร Excel บนคลาวด์ได้โดยไม่ต้องติดตั้งซอฟต์แวร์หรือพึ่งพาสิ่งที่ติดตั้งเพิ่มเติมบนเครื่องของคุณ

ในบทความนี้ เราจะมาดูวิธีใช้ Aspose.Cells Cloud SDK สำหรับ PHP เพื่อทำงานทั่วไปบางอย่าง เช่น การสร้างสมุดงาน Excel ใหม่ การแทรกข้อมูลลงในเซลล์ และการบันทึกสมุดงานที่แก้ไขแล้วขึ้นคลาวด์

## เริ่มต้นใช้งาน

ก่อนที่คุณจะเริ่มใช้ Aspose.Cells Cloud SDK สำหรับ **PHP** คุณจำเป็นต้องตั้งค่าสภาพแวดล้อมในการพัฒนาและติดตั้งการขึ้นต่อกันที่จำเป็น อ้างอิงไปยัง <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">บทความ</a> บนเว็บไซต์ Aspose เพื่อรับ client ID และ client secret ของคุณ

**ข้อกำหนดเบื้องต้น**

- PHP เวอร์ชัน 7.4 หรือใหม่กว่า  
- ติดตั้ง Composer บนเครื่องพัฒนาของคุณแล้ว  
- มี client ID และ client secret ที่ถูกต้องของ Aspose Cloud  
- เข้าถึงพื้นที่จัดเก็บของ Aspose Cloud ได้ (ค่าเริ่มต้นหรือแบบกำหนดเอง)  

## วิธีติดตั้งแพ็กเกจ PHP สำหรับ Aspose.Cells Cloud

คุณสามารถติดตั้ง Aspose.Cells Cloud SDK สำหรับ PHP ได้ โดยทำตามขั้นตอนดังนี้:

- เพิ่ม Aspose.Cells Cloud เป็นการขึ้นต่อกันในไฟล์ `composer.json` ของคุณ:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- รันคำสั่ง Composer update เพื่อติดตั้ง SDK:

   ```bash
   composer install
   ```

- รวม autoloader ของ Composer ในโค้ด PHP ของคุณ:

   ```php
   require 'vendor/autoload.php';
   ```

## วิธีใช้แพ็กเกจ PHP เพื่อแปลง Xlsx เป็นรูปแบบอื่นๆ

- นำเข้าไลบรารี Aspose.Cells Cloud  
  เริ่มต้นด้วยการนำเข้าแพ็กเกจที่จำเป็นจาก Aspose.Cells Cloud PHP SDK เข้าสู่โปรเจกต์ของคุณ

- ตั้งค่า API Client ด้วยข้อมูลรับรอง  
  ยืนยันตัวตนให้กับ API client ของคุณด้วย client ID และ client secret ของคุณที่ไม่ซ้ำใคร

- กำหนดค่าพารามิเตอร์สำหรับการแปลง  
  กำหนดพารามิเตอร์สำหรับงานแปลง รวมถึงชื่อไฟล์ Excel ต้นทาง รูปแบบผลลัพธ์ที่ต้องการ และเส้นทางโฟลเดอร์จัดเก็บ

- ดำเนินการแปลงสมุดงาน  
  เรียกใช้กระบวนการแปลงด้วยเมธอด `PostConvertWorkbook` และจัดการกับการตอบกลับ

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### การอ้างอิง API สำหรับ `PostConvertWorkbook`

| พารามิเตอร์      | คำอธิบาย                                   | ชนิดข้อมูล | จำเป็น |
|----------------|-----------------------------------------------|-----------|--------|
| `file`         | ชื่อไฟล์ Excel ต้นทาง (เช่น `sample.xlsx`) | string | จำเป็น |
| `format`       | รูปแบบผลลัพธ์ที่ต้องการ (`pdf`, `csv`, `png` เป็นต้น) | string | จำเป็น |
| `storage`      | ชื่อพื้นที่จัดเก็บหรือเส้นทางโฟลเดอร์ที่อยู่กับไฟล์ต้นทาง | string | ไม่จำเป็น |
| `outPath`      | เส้นทางที่ต้องการบันทึกไฟล์ที่แปลงแล้วโดยตรงในพื้นที่จัดเก็บ (ไม่บังคับ) | string | ไม่จำเป็น |

**เมธอด HTTP:** POST  
**จุดปลายทาง (Endpoint):** `/cells/convert/{format}`  

**ตัวอย่างการตอบกลับ (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**รหัสสถานะ (Status Codes)**

- `200` – การแปลงสำเร็จ  
- `400` – คำขอไม่ถูกต้อง (พารามิเตอร์ขาดหายหรือไม่ถูกต้อง)  
- `401` – การยืนยันตัวตนล้มเหลว  
- `500` – ข้อผิดพลาดของเซิร์ฟเวอร์  
---
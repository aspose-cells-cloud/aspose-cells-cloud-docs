---
title: "Aspose.Cells Cloud SDK สำหรับ Perl – แปลง ผสาน แยก ป้องกัน และอื่นๆ"
second_title: "เอกสาร"
ArticleTitle: "Aspose.Cells Cloud SDK สำหรับ Perl – แปลง ผสาน แยก ป้องกัน และอื่นๆ"
linktype: "Aspose.Cells Cloud SDK สำหรับ Perl"
type: docs
url: /th/available-sdks/aspose-cells-cloud-perl/
description: "สำรวจ Aspose.Cells Cloud Perl SDK – ไลบรารีข้ามแพลตฟอร์มที่ช่วยให้คุณสร้าง แปลง ผสาน แยก ป้องกัน ค้นหา และแทนที่ไฟล์ Excel โดยไม่ต้องติดตั้ง Microsoft Office รวมถึงคู่มือการติดตั้ง ตัวอย่างโค้ด และเอกสารอ้างอิง API"
weight: 30
keywords: "Perl, Aspose.Cells Cloud, Excel SDK, การแปลง, PDF, API, การจัดการ Excel, Perl SDK, การประมวลผล Excel บนคลาวด์"
---

_อัปเดตล่าสุด: 30 กรกฎาคม 2569_

SDK นี้เป็นโอเพนซอร์สและอยู่ภายใต้ใบอนุญาต MIT License คุณสามารถเข้าถึงซอร์สโค้ดของไลบรารี Perl สำหรับ Aspose.Cells Cloud ได้ที่ [นี่](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl)

# **วิธีใช้ไลบรารี Perl ของ Aspose.Cells Cloud**

Aspose.Cells Cloud SDK สำหรับ Perl เป็นไลบรารีที่ทรงพลังซึ่งช่วยให้นักพัฒนาสามารถจัดการและประมวลผลไฟล์ Microsoft Excel โดยใช้ภาษา Perl ด้วย SDK นี้ คุณสามารถสร้าง แก้ไข และแปลงเอกสาร Excel บนคลาวด์ โดยไม่จำเป็นต้องติดตั้งซอฟต์แวร์หรือการพึ่งพาเพิ่มเติมใดๆ บนเครื่องของคุณ

ในบทความนี้ เราจะมาสำรวจวิธีใช้ Aspose.Cells Cloud SDK สำหรับ Perl เพื่อดำเนินการบางอย่างที่พบบ่อย เช่น การสร้างสมุดงาน Excel ใหม่ การใส่ข้อมูลลงในเซลล์ และการบันทึกสมุดงานที่แก้ไขแล้วลงบนคลาวด์

## เริ่มต้นใช้งาน

ก่อนที่คุณจะเริ่มใช้ Aspose.Cells Cloud SDK สำหรับ **Perl** คุณจำเป็นต้องตั้งค่าสภาพแวดล้อมการพัฒนาและติดตั้งการพึ่งพาที่จำเป็น โปรดดูคู่มือ **[Aspose.Cells Cloud Quickstart](https://docs.aspose.cloud/cells/quickstart/)** บนเว็บไซต์ Aspose เพื่อรับ client ID และ client secret ของคุณ

## วิธีติดตั้งแพ็กเกจ Perl สำหรับ Aspose.Cells Cloud

**ข้อกำหนดเบื้องต้น**  
- Perl 5.10 หรือใหม่กว่า  
- ติดตั้ง CPAN (Comprehensive Perl Archive Network) แล้ว  
- มี client ID และ client secret ของ Aspose.Cells Cloud ที่ถูกต้อง  

คุณสามารถติดตั้ง Aspose.Cells Cloud SDK สำหรับ Perl ด้วยคำสั่งด้านล่างนี้:

```perl
perl -MCPAN -e shell
install AsposeCellsCloud::CellsApi
```

## วิธีใช้แพ็กเกจ Perl เพื่อแปลง Xlsx เป็นรูปแบบอื่น

- **นำเข้าไลบรารี Aspose.Cells Cloud**  
  เริ่มต้นด้วยการนำเข้าแพ็กเกจที่จำเป็นจาก Aspose.Cells Cloud Perl SDK เข้าสู่โครงการของคุณ

- **ตั้งค่าไคลเอนต์ API ด้วยข้อมูลรับรอง**  
  ยืนยันตัวตนให้ไคลเอนต์ API ของคุณด้วย client ID และ client secret ที่ไม่ซ้ำใครของคุณ

- **เตรียมพารามิเตอร์สำหรับการแปลง**  
  กำหนดพารามิเตอร์สำหรับงานแปลง รวมถึงชื่อไฟล์ต้นทาง รูปแบบเอาต์พุตที่ต้องการ และเส้นทางโฟลเดอร์จัดเก็บ

- **เริ่มกระบวนการแปลงสมุดงาน**  
  เรียกใช้กระบวนการแปลงด้วยเมทอด `PostConvertWorkbook` และจัดการกับการตอบกลับ

ด้านล่างนี้คือคำอธิบายอย่างย่อสำหรับการดำเนินการ `PostConvertWorkbook`:

| วิธี HTTP | จุดปลายทาง                             | พารามิเตอร์ที่จำเป็น                                | ตัวอย่างคำสั่ง (Perl)                                                                                         | ตัวอย่างการตอบกลับ (JSON)                             | โค้ดสถานะที่เป็นไปได้ |
|-----------|----------------------------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|-----------------------|
| POST      | `/cells/convert`                        | `file` (สมุดงานต้นทาง), `outputFormat`, `storage` | ```perl\nmy $result = $api_instance->post_convert_workbook({ file => 'Book1.xlsx', outputFormat => 'pdf', storage => 'MyStorage' });\n``` | `{ "File": "Book1.pdf", "Url": "https://.../Book1.pdf" }` | 200 OK, 400 Bad Request, 401 Unauthorized, 500 Server Error |

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}
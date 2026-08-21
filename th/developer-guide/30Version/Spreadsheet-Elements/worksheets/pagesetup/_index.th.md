---
title: "การตั้งค่าหน้ากระดาษของเวิร์กชีต"
second_title: "เอกสาร"
linktype: "การตั้งค่าหน้ากระดาษ"
type: docs
url: /th/page-setup/
keywords: "Aspose.Cells, pageSetup, worksheet, print settings, margins, orientation, paper size, header, footer, scaling"
description: "เรียนรู้วิธีกำหนดค่าเลย์เอาต์การพิมพ์ของเวิร์กชีต Excel โดยใช้ออบเจกต์ PageSetup ของ Aspose.Cells Cloud รวมถึงรายการคุณสมบัติ ค่าเริ่มต้น ช่วงข้อมูล และตัวอย่างโค้ดสำหรับ C#, Java และ Python"
weight: 20
ArticleTitle: "การตั้งค่าหน้ากระดาษของเวิร์กชีต – กำหนดค่าเลย์เอาต์การพิมพ์ด้วย Aspose.Cells Cloud"
---

# **PageSetup**

การตั้งค่าหน้ากระดาษสำหรับการพิมพ์ใน Excel

## ภาพรวม

ออบเจกต์ **PageSetup** กำหนดตัวเลือกการจัดรูปแบบการพิมพ์สำหรับเวิร์กชีต Excel เช่น ระยะขอบ การวางแนว การปรับขนาด หัวกระดาษ ท้ายกระดาษ และการตั้งค่าอื่นๆ ที่เกี่ยวข้องกับการพิมพ์ การกำหนดคุณสมบัติเหล่านี้ช่วยให้นักพัฒนาสามารถสร้างสมุดงานที่พร้อมพิมพ์ให้ตรงกับรูปลักษณ์และจำนวนหน้าที่ต้องการ

ด้านล่างนี้คือตัวอย่างโค้ดภาษา C# แบบสั้นที่แสดงวิธีการตั้งค่าคุณสมบัติ PageSetup ที่ใช้บ่อยโดยใช้ Aspose.Cells Cloud SDK:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// เริ่มต้นไคลเอนต์ API (แทนที่ด้วยข้อมูลประจำตัวของคุณ)
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// กำหนดค่า PageSetup
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// ใช้การตั้งค่ากับเวิร์กชีตแรกของสมุดงาน
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

โค้ดตัวอย่างนี้ตั้งค่าเวิร์กชีตให้อยู่ในแนวแนวนอน (Landscape) ใช้ขนาดกระดาษ A4 จัดกลางเนื้อหาทั้งแนวนอนและแนวตั้ง และใช้อัตราส่วนการซูมที่ 100%

## คุณสมบัติ

| ชื่อคุณสมบัติ        | ชนิดข้อมูล | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น     | คำอธิบาย                                                                 |
| --------------------- | ----------- | ------------ | ------------ | --------------- | -------------------------------------------------------------------------- |
| BlackAndWhite         | bool        | false        | false        | false           | พิมพ์เวิร์กชีตในโหมดขาวดำ                                                |
| BottomMargin          | float       | true         | false        | 2.54 ซม.         | ขนาดของระยะขอบด้านล่างเป็นเซนติเมตร                                     |
| CenterHorizontally    | bool        | false        | false        | false           | จัดกลางเวิร์กชีตแนวนอนเมื่อพิมพ์                                          |
| CenterVertically      | bool        | false        | false        | false           | จัดกลางเวิร์กชีตแนวตั้งเมื่อพิมพ์                                          |
| FirstPageNumber       | int         | true         | false        | 1               | หมายเลขหน้าแรกที่ใช้เมื่อพิมพ์เวิร์กชีต                                   |
| FitToPagesTall        | int         | false        | false        | 1               | จำนวนหน้าในแนวตั้งที่เวิร์กชีตจะถูกปรับขนาดให้พอดี                      |
| FitToPagesWide        | int         | false        | false        | 1               | จำนวนหน้าในแนวนอนที่เวิร์กชีตจะถูกปรับขนาดให้พอดี                      |
| FooterMargin          | float       | true         | false        | 2.54 ซม.         | ระยะห่างจากด้านล่างของหน้าถึงท้ายกระดาษ เป็นเซนติเมตร                   |
| HeaderMargin          | float       | true         | false        | 2.54 ซม.         | ระยะห่างจากด้านบนของหน้าถึงหัวกระดาษ เป็นเซนติเมตร                     |
| IsAutoFirstPageNumber | bool        | false        | false        | false           | กำหนดหมายเลขหน้าแรกโดยอัตโนมัติ                                         |
| IsHFAlignMargins      | bool        | false        | false        | true            | เมื่อตั้งค่าเป็น `true` ระยะขอบของหัว/ท้ายกระดาษจะตรงกับระยะขอบของหน้า |
| IsHFDiffFirst         | bool        | false        | false        | false           | ระบุว่าหัว/ท้ายกระดาษของหน้าแรกแตกต่างจากหน้าอื่นๆ                      |
| IsHFDiffOddEven       | bool        | false        | false        | false           | ระบุว่าหัว/ท้ายกระดาษของหน้าคี่แตกต่างจากหน้าคู่                        |
| IsHFScaleWithDoc      | bool        | false        | false        | false           | ปรับขนาดหัวและท้ายกระดาษพร้อมกับเอกสาร (Excel 2007+)**                    |
| IsPercentScale        | bool        | false        | false        | true            | เมื่อตั้งค่าเป็น `false` การปรับขนาดจะถูกควบคุมโดย `FitToPagesWide` และ `FitToPagesTall` |
| LeftMargin            | float       | true         | false        | 2.54 ซม.         | ขนาดของระยะขอบด้านซ้ายเป็นเซนติเมตร                                     |
| Order                 | string      | true         | false        | "DownThenOver"  | ลำดับที่ Excel ใช้ในการเรียงหมายเลขหน้าเมื่อพิมพ์เวิร์กชีตขนาดใหญ่       |
| Orientation           | string      | false        | false        | "Portrait"      | การวางแนวหน้า: **Landscape** หรือ **Portrait**                           |
| PaperSize             | string      | true         | false        | "A4"            | ขนาดกระดาษที่ใช้ในการพิมพ์                                                |
| PrintArea             | string      | true         | false        | (ไม่มี)          | ช่วงของเซลล์ที่จะพิมพ์ (เช่น `"A1:D20"`)                                 |
| PrintComments         | string      | true         | false        | "NoComments"    | วิธีการพิมพ์คำอธิบายประกอบร่วมกับเวิร์กชีต                              |
| PrintCopies           | int         | true         | false        | 1               | จำนวนสำเนาที่จะพิมพ์                                                     |
| PrintDraft            | bool        | false        | false        | false           | พิมพ์เวิร์กชีตในโหมดร่าง (ไม่มีกราฟิก)                                   |
| PrintErrors           | string      | true         | false        | "Display"       | ชนิดของข้อผิดพลาดที่แสดงเมื่อพิมพ์                                        |
| PrintGridlines        | bool        | false        | false        | false           | พิมพ์เส้นตารางของเซลล์                                                  |
| PrintHeadings         | bool        | false        | false        | false           | พิมพ์หัวเรื่องแถวและคอลัมน์                                              |
| PrintQuality          | int         | true         | false        | 600             | การตั้งค่าคุณภาพการพิมพ์ (จุดต่อนิ้ว)                                    |
| PrintTitleColumns     | string      | true         | false        | (ไม่มี)          | คอลัมน์ที่จะทำซ้ำที่ด้านซ้ายของแต่ละหน้าที่พิมพ์                        |
| PrintTitleRows        | string      | true         | false        | (ไม่มี)          | แถวที่จะทำซ้ำที่ด้านบนของแต่ละหน้าที่พิมพ์                              |
| RightMargin           | float       | true         | false        | 2.54 ซม.         | ขนาดของระยะขอบด้านขวาเป็นเซนติเมตร                                     |
| TopMargin             | float       | true         | false        | 2.54 ซม.         | ขนาดของระยะขอบด้านบนเป็นเซนติเมตร                                      |
| Zoom                  | int         | false        | false        | 100             | ตัวคูณการปรับขนาดเป็นเปอร์เซ็นต์ (10–400%)                               |
| Header                | object      | true         | false        | (ไม่มี)          | การกำหนดค่าส่วนหัวกระดาษ                                                 |
| Footer                | object      | true         | false        | (ไม่มี)          | การกำหนดค่าส่วนท้ายกระดาษ                                                |

## ออบเจกต์ที่เกี่ยวข้อง

- **Header** – กำหนดค่าส่วนหัวของเวิร์กชีต  
- **Footer** – กำหนดค่าส่วนท้ายของเวิร์กชีต  
- **PrintOptions** – การตั้งค่าเพิ่มเติมที่เกี่ยวข้องกับการพิมพ์ เช่น ตัวแบ่งหน้าและพื้นที่การพิมพ์
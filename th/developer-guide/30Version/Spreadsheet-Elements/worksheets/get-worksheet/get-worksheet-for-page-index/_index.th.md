---
title: "ส่งออกหน้าสมุดงาน – ข้อมูลอ้างอิง API ของ Aspose.Cells Cloud"
ArticleTitle: "ส่งออกหน้าสมุดงาน – ข้อมูลอ้างอิง API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
linktitle: "หน้า"
type: docs
url: /worksheets/page-to-different-formats/
aliases: [/get-worksheet-for-page-index/]
keywords: "Aspose.Cells Cloud, การส่งออกหน้าสมุดงาน, PDF, PNG, CSV, REST API, การยืนยันตัวตนด้วย JWT, รูปแบบไฟล์"
description: "เรียนรู้วิธีการส่งออกหน้าสมุดงานที่ระบุไปยังรูปแบบต่างๆ เช่น PDF, PNG, CSV และอื่นๆ โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างคำสั่ง cURL, คู่มือพารามิเตอร์ และโค้ดตัวอย่าง SDK สำหรับหลายภาษา"
weight: 240
---

การส่งออกหน้าสมุดงานที่ระบุนั้นมีประโยชน์เมื่อคุณต้องการภาพถ่ายแบบพิมพ์ของรายงาน ภาพแผนภูมิ หรือข้อมูลที่ดึงมาโดยไม่ต้องดาวน์โหลดสมุดงานทั้งหมด เอ็นด์พอยต์นี้ช่วยให้คุณดึงหน้าเดียวในรูปแบบที่เหมาะสมที่สุดกับกระบวนการทำงานในขั้นตอนถัดไปของคุณ

API [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) ช่วยให้คุณแปลงหน้าที่ระบุของสมุดงานไปยังรูปแบบไฟล์ต่างๆ ได้ รูปแบบที่รองรับ: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## API สำหรับการสื่อสารแบบ REST

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

> **ข้อกำหนดเบื้องต้น** – คุณต้องมีโทเคน JWT ที่ถูกต้องสำหรับการยืนยันตัวตน และสมุดงานต้องถูกจัดเก็บไว้ในโฟลเดอร์คลาวด์ที่คุณระบุด้วยพารามิเตอร์ `folder`

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**การตอบกลับ** – บริการจะส่งกลับหน้าที่ร้องขอในรูปแบบที่เลือก สำหรับรูปแบบภาพ (png, jpeg, gif เป็นต้น) ส่วนเนื้อหาในส่วนตอบกลับจะเป็นข้อมูลไบนารีของภาพ ส่วนสำหรับรูปแบบเอกสาร (pdf, xls, csv เป็นต้น) ส่วนเนื้อหาในส่วนตอบกลับจะเป็นเนื้อหาไฟล์ การเรียกที่สำเร็จจะส่งกลับโค้ด HTTP 200

*ตัวอย่างการตอบกลับแบบ PNG (ข้อความ base64 ตัวอย่างสั้นๆ):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**พารามิเตอร์**

| พารามิเตอร์            | ชนิดข้อมูล | คำอธิบาย                                                                 | ค่าเริ่มต้น |
| ---------------------- | ---------- | ------------------------------------------------------------------------ | ---------- |
| `format`               | string     | รูปแบบไฟล์ผลลัพธ์ (เช่น `pdf`, `png`, `csv`)                             | `pdf`      |
| `verticalResolution`   | integer    | ความละเอียดแนวตั้งของภาพที่เรนเดอร์ (DPI)                               | `100`      |
| `horizontalResolution` | integer    | ความละเอียดแนวนอนของภาพที่เรนเดอร์ (DPI)                               | `100`      |
| `pageIndex`            | integer    | ดัชนีของหน้าสมุดงานที่ต้องการส่งออก (เริ่มต้นที่ 0 = หน้าแรก)           | `0`        |
| `folder`               | string     | โฟลเดอร์ที่เก็บไว้ในพื้นที่จัดเก็บบนคลาวด์ซึ่งสมุดงานต้นฉบับอยู่        | —          |

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                    | คำอธิบาย                                                    |
|-----|-----------------------------|-------------------------------------------------------------|
| 200 | คำขอสำเร็จ (OK)            | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือหายไป                               |
| 413 | ข้อมูลในส่วนของคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                    |
| 500 | ข้อผิดพลาดภายในของเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนฝั่งเซิร์ฟเวอร์                  |

**ข้อผิดพลาดที่เป็นไปได้**

- **401 ไม่ได้รับอนุญาต (Unauthorized)** – โทเคน JWT ไม่ถูกต้องหรือหายไป
- **404 ไม่พบ (Not Found)** – สมุดงานหรือชีตที่ระบุไม่มีอยู่จริง
- **400 คำขอไม่ถูกต้อง (Bad Request)** – ค่าพารามิเตอร์ไม่ถูกต้อง (เช่น `format` ที่ไม่รองรับ)
- **500 ข้อผิดพลาดภายในของเซิร์ฟเวอร์ (Internal Server Error)** – เกิดปัญหาที่ไม่คาดคิดในฝั่งเซิร์ฟเวอร์

## ชุด SDK สำหรับคลาวด์ (Cloud SDK Family)

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ กรุณาตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
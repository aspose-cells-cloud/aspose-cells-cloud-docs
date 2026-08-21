---
title: "ส่งออกพื้นที่ของแผ่นงานเป็น PNG, PDF, CSV – API ของ Aspose.Cells Cloud"
secondtitle: "เอกสาร"
linktitle: "พื้นที่"
type: docs
url: /th/worksheets/area-to-different-formats/
aliases: [  /th/get-worksheet-for-area/ ]
keywords: "Aspose.Cells, ส่งออกพื้นที่แผ่นงาน, PNG, PDF, CSV, การแปลง Excel, REST API, SDK"
description: "เรียนรู้วิธีส่งออกช่วงของเซลล์ที่ระบุจากแผ่นงาน Excel ไปยังรูปแบบ PNG, PDF, CSV และอื่นๆ อีกกว่า 20 รูปแบบ ผ่าน API แบบ REST หรือ SDK ของ Aspose.Cells Cloud (C#, Java, Python, …)"
weight: 230
ArticleTitle: "ส่งออกพื้นที่แผ่นงานเป็น PNG, PDF, CSV ด้วย API ของ Aspose.Cells Cloud – คู่มือฉบับสมบูรณ์"
---

API [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) ช่วยให้คุณแปลงพื้นที่ที่ระบุของแผ่นงานเป็นรูปแบบไฟล์ต่างๆ รูปแบบที่รองรับ: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

คู่มือนี้แสดงวิธีส่งออก **ช่วงของเซลล์ที่ระบุ** จากแผ่นงาน Excel ไปยัง PNG, PDF, CSV และรูปแบบอื่นๆ อีกกว่า 20 รูปแบบ โดยใช้ Aspose.Cells Cloud API สำหรับการดำเนินการที่เกี่ยวข้อง เช่น การส่งออกทั้งแผ่นงานหรือการแปลงสมุดงาน โปรดดูที่หน้า **[ส่งออกทั้งแผ่นงาน](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** และ **[แปลงสมุดงานเป็น PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)**

## API REST

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้โดยสาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงผ่านเบราว์เซอร์เว็บ

### พารามิเตอร์ของคำขอ

| พารามิเตอร์            | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                    |
|------------------------|------------|--------|----------------------------------------------|
| `name`                 | ข้อความ    | ใช่    | ชื่อไฟล์สมุดงาน                             |
| `sheetName`            | ข้อความ    | ใช่    | ชื่อแผ่นงานเป้าหมาย                         |
| `format`               | ข้อความ    | ใช่    | รูปแบบเอาต์พุตที่ต้องการ (png, pdf, csv, …)  |
| `area`                 | ข้อความ    | ไม่บังคับ | ช่วงของเซลล์ที่ต้องการส่งออก (เช่น `B3:K8`) |
| `verticalResolution`  | จำนวนเต็ม | ไม่บังคับ | DPI แนวตั้งสำหรับรูปแบบภาพแบบเรสเตอร์      |
| `horizontalResolution`| จำนวนเต็ม | ไม่บังคับ | DPI แนวนอนสำหรับรูปแบบภาพแบบเรสเตอร์      |
| `folder`               | ข้อความ    | ไม่บังคับ | โฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์ที่มีไฟล์   |
| `storage`              | ข้อความ    | ไม่บังคับ | ชื่อของบริการจัดเก็บข้อมูล                   |

### การตอบกลับที่ประสบความสำเร็จ

* **200 OK** – ส่งคืนไฟล์ที่ร้องขอในรูปแบบไบนารี (PNG, PDF, CSV, เป็นต้น)

### การตอบกลับข้อผิดพลาด

| โค้ดสถานะ | คำอธิบาย                                     |
|------------|----------------------------------------------|
| 400        | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง |
| 401        | ไม่ได้รับอนุญาต – โทเคนการยืนยันตัวตนขาดหายหรือไม่ถูกต้อง |
| 404        | ไม่พบ – สมุดงานหรือแผ่นงานที่ระบุไม่มีอยู่จริง |
| 500        | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

**ตัวอย่างข้อมูลส่วนข้อผิดพลาด**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "พารามิเตอร์ 'area' มีรูปแบบไม่ถูกต้อง รูปแบบที่คาดไว้: B3:K8."
  }
}
```

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

ภาพที่แปลงแล้ว (PNG แบบไบนารี)

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณมุ่งเน้นไปที่ตรรกะของโครงการของคุณ โปรดดูที่ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
---
title: "รับการแบ่งหน้าแนวตั้ง"
second_title: "เอกสาร"
linktype: "รับการแบ่งหน้าแนวตั้ง"
type: docs
url: /th/page-breaks/get-vertical-page-breaks/
aliases: [  /th/get-vertical-page-breaks-inside-worksheet/ ]
keywords: "Aspose.Cells, การแบ่งหน้าแนวตั้ง, Excel API, สเปรดชีตบนคลาวด์, REST API"
description: "ดึงการแบ่งหน้าแนวตั้งจากWorksheets ใน Excel ผ่าน Aspose.Cells Cloud REST API (v3.0) ประกอบด้วย HTTPS endpoint, พารามิเตอร์ที่จำเป็น, ตัวอย่าง cURL, รายละเอียดการตอบกลับ, การจัดการข้อผิดพลาด และตัวอย่าง SDK"
weight: 20
---

REST API นี้ดึง **การแบ่งหน้าแนวตั้ง** จากWorksheets

## Rest Api

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### พารามิเตอร์สำหรับคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                           | จำเป็น |
| ---------------- | --------- | -------- | -------------------------------------------------- | ------ |
| `name`           | string    | path     | ชื่อไฟล์ Excel                                    | ใช่    |
| `sheetName`      | string    | path     | ชื่อWorksheets ที่ต้องการอ่านการแบ่งหน้า          | ใช่    |
| `folder`         | string    | query    | โฟลเดอร์ในพื้นที่จัดเก็บที่มีไฟล์                  | ไม่ใช่ |
| `storageName`    | string    | query    | ชื่อของพื้นที่จัดเก็บ Aspose Cloud ที่จะใช้งาน     | ไม่ใช่ |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST interaction ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้ **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### รายละเอียดการตอบกลับ

| ฟิลด์                   | ชนิดข้อมูล | คำอธิบาย                                                                 |
| ----------------------- | ---------- | ------------------------------------------------------------------------ |
| `VerticalPageBreakList` | array      | คอลเลกชันของวัตถุการแบ่งหน้าแนวตั้ง                                     |
| `Column`                | int        | ดัชนีคอลัมน์ (เริ่มต้นที่ 0) ที่เกิดการแบ่งหน้า                          |
| `StartRow`              | int        | แถวแรกของช่วงการแบ่งหน้า (เริ่มต้นที่ 0)                                |
| `EndRow`                | int        | แถวสุดท้ายของช่วงการแบ่งหน้า (เริ่มต้นที่ 0 โดยทั่วไปคือ `1048575` สำหรับแถวสุดท้าย) |
| `link.Href`             | string     | URL อ้างอิงตนเองของทรัพยากร (HTTPS)                                      |
| `Code`                  | int        | HTTP status code ที่บริการส่งคืนกลับมา                                   |
| `Status`                | string     | คำอธิบายข้อความของ HTTP status                                          |

### การจัดการข้อผิดพลาด

| HTTP Code | ความหมาย             | สาเหตุที่พบบ่อย                             |
| --------- | -------------------- | -------------------------------------------- |
| 401       | ไม่ได้รับอนุญาต       | ไม่มี JWT token หรือ token ไม่ถูกต้อง         |
| 404       | ไม่พบ                 | ไฟล์หรือWorksheets ที่ระบุไม่มีอยู่จริง       |
| 400       | คำขอไม่ถูกต้อง       | พารามิเตอร์ query ไม่ถูกต้องหรือมีรูปแบบผิด   |
| 500       | ข้อผิดพลาดของเซิร์ฟเวอร์ | สภาพแวดล้อมภายในเซิร์ฟเวอร์ผิดปกติUnexpected |

ตรวจสอบฟิลด์ `Code` และ `Status` ใน JSON response เพื่อดูรายละเอียดเพิ่มเติม

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนากับ Aspose.Cells Cloud SDK ช่วยซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) สำหรับรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}
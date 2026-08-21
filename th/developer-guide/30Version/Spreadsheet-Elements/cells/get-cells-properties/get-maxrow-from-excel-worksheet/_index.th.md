---
title: "รับค่า MaxRow จากเวิร์กชีต Excel"
type: docs
url: /get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "ดึงหมายเลขแถวสูงสุดในเวิร์กชีต Excel – API ของ Aspose.Cells Cloud"
keywords: "Aspose.Cells, Excel, MaxRow, REST API, Cloud SDK, สเปรดชีต, เวิร์กชีต, GetMaxRow"
description: "เรียนรู้วิธีดึงหมายเลขแถวสูงสุดของเวิร์กชีตในไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วยไวยากรณ์คำขอ โครงสร้างการตอบกลับ ตัวอย่าง SDK และหมายเหตุการใช้งาน"
---

API REST นี้จะส่งคืน **หมายเลขแถวสูงสุด** ในเวิร์กชีต Excel เมื่อพารามิเตอร์ `cellOrMethodName` ถูกตั้งค่าเป็น `maxrow`

- **ตัวอย่าง cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **ใช้ SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะของโครงการของคุณได้ กรุณาตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่มีทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**อ้างอิง API**

| รายการ | รายละเอียด |
|------|---------|
| **เมธอด** | `GET` |
| **จุดปลายทาง (Endpoint)** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **พารามิเตอร์ในเส้นทาง (Path Parameters)** | `fileName` – ชื่อไฟล์ Excel (จำเป็น) <br> `sheetName` – ชื่อเวิร์กชีต (จำเป็น) |
| **พารามิเตอร์การสืบค้น (Query Parameters)** | `folder` – เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บ (ไม่บังคับ) <br> `storageName` – ชื่อพื้นที่จัดเก็บ (ไม่บังคับ) |
| **การตอบกลับเมื่อสำเร็จ** | `200 OK` <br> ```json { "MaxRow": integer } ``` |
| **การตอบกลับเมื่อเกิดข้อผิดพลาด** | `400 Bad Request` – พารามิเตอร์ไม่ถูกต้อง <br> `401 Unauthorized` – การยืนยันตัวตนล้มเหลว <br> `404 Not Found` – ไม่พบไฟล์หรือเวิร์กชีต |

**ข้อกำหนดเบื้องต้น**

- โทเคนการยืนยันตัวตนที่ถูกต้องของ Aspose Cloud  
- สมุดบันทึกเป้าหมายต้องถูกอัปโหลดลงในพื้นที่จัดเก็บของ Aspose Cloud หรือเข้าถึงได้ผ่าน URL สาธารณะ  

**หมายเหตุ**

- การดำเนินการนี้มีให้ใช้งานในเวอร์ชัน API **v3.0** ขึ้นไป  
- ค่า `MaxRow` ที่ส่งคืนมาจะสอดคล้องกับดัชนีแถวที่ใช้งานสูงสุด (เริ่มต้นที่ 1) สำหรับเวิร์กชีตที่ว่างเปล่า ค่าที่ได้มักจะเป็น `1`  

ตัวอย่าง SDK ต่อไปนี้แสดงวิธีการเรียกใช้การดำเนินการในภาษาการเขียนโปรแกรมต่างๆ
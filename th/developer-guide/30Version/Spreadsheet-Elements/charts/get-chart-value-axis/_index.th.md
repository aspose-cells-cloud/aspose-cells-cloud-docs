---
title: "รับค่าแกนค่าของแผนภูมิ"
type: docs
url: /th/charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, แกนค่าของแผนภูมิ, REST API, Excel, Cloud SDK, รับค่าแกนค่าของแผนภูมิ
description: "Aspose.Cells Cloud REST API – ดึงข้อมูลแกนค่าของแผนภูมิในสมุดงาน Excel"
ArticleTitle: "รับค่าแกนค่าของแผนภูมิ - Aspose.Cells Cloud REST API"
---

API REST นี้ดึงข้อมูลแกนค่าของแผนภูมิ โดยเป็นส่วนหนึ่งของ **Aspose.Cells Cloud REST API** และทำงานกับสมุดงาน Excel ที่จัดเก็บไว้ในคลาวด์

สำหรับการดำเนินการที่เกี่ยวข้อง โปรดดูที่เอนด์พอยต์ **[รับแกนหมวดหมู่ของแผนภูมิ](/charts/category-axis/get/)**

## API GetChartValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                          |
| -------------- | ------- | -------- | ------------------------------------------------- |
| name           | string  | path     | ชื่อไฟล์ Excel (รวมนามสกุลด้วย)                   |
| sheetName      | string  | path     | ชื่อแผ่นงานที่มีแผนภูมิ                           |
| chartIndex     | integer | path     | ดัชนีของแผนภูมิ (เริ่มต้นที่ 0) ภายในแผ่นงาน      |
| folder         | string  | query    | โฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์ที่ไฟล์ตั้งอยู่   |
| storageName    | string  | query    | ชื่อของบริการพื้นที่จัดเก็บ (เช่น Aspose Cloud)    |

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณโต้ตอบกับ REST API ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
 -X GET \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Values",
    "Format": {
      "NumberFormat": "General",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**โค้ดสถานะ HTTP ที่เป็นไปได้**

| โค้ด | คำอธิบาย                                               |
|------|--------------------------------------------------------|
| 200  | สำเร็จ – ข้อมูลแกนค่าถูกส่งกลับมา                     |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ที่จำเป็นหายไปหรือไม่ถูกต้อง |
| 401  | ไม่มีสิทธิ์ – โทเคนยืนยันตัวตนหายไปหรือไม่ถูกต้อง    |
| 404  | ไม่พบ – สมุดงาน แผ่นงาน หรือแผนภูมิที่ระบุไม่มีอยู่จริง |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

คำตอบจะประกอบด้วยออบเจกต์ `ValueAxis` ที่มีรายละเอียด เช่น ค่า `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title` และ `Format` ในการใช้งานแบบเต็มรูปแบบ อาจมีข้อมูลการจัดรูปแบบเพิ่มเติมให้ด้วย

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นไปที่งานหลักของโครงการได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}
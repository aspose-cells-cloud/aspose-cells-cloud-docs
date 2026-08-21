---
---
title: "รับค่าแกนค่าที่สองของแผนภูมิ"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, แกนค่าที่สองของแผนภูมิ, Excel, REST API, คลาวด์, API, แกนแผนภูมิ Excel
description: ดึงค่าแกนค่าที่สองของแผนภูมิที่ระบุในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API
ArticleTitle: "รับค่าแกนค่าที่สองของแผนภูมิ – Aspose.Cells Cloud API"
---

API นี้ของ REST ใช้ดึงค่าแกนค่าที่สองของแผนภูมิ

## API GetChartSecondValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                     |
| ---------------- | --------- | -------- | --------------------------------------------- |
| name             | string    | path     | ชื่อไฟล์ Excel                               |
| sheetName        | string    | path     | ชื่อของแผ่นงานที่มีแผนภูมิ                   |
| chartIndex       | integer   | path     | ดัชนีแบบเริ่มต้นที่ 0 ของแผนภูมิ              |
| folder           | string    | query    | โฟลเดอร์ที่เก็บไฟล์ไว้                       |
| storageName      | string    | query    | ชื่อของพื้นที่จัดเก็บบน Aspose Cloud         |

**ข้อกำหนดเบื้องต้น**: ต้องระบุโทเค็น JWT ที่ถูกต้องซึ่งได้รับผ่านกระบวนการ OAuth2 ของ Aspose Cloud ในส่วนหัว `Authorization` ของทุกคำขอ

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API บนคลาวด์ด้วย cURL จุดปลายทางทั้งหมดของ Aspose Cloud ต้องใช้ HTTPS

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
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
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Second Value Axis"
  }
}
```

**ฟิลด์ของการตอบกลับ**

- **Code** – รหัสสถานะ HTTP ของการดำเนินการ (เช่น `200` สำหรับความสำเร็จ)  
- **Status** – คำอธิบายสถานะในรูปแบบข้อความ (`"OK"` สำหรับความสำเร็จ)  
- **Axis** – อ็อบเจกต์ที่เก็บรายละเอียดของแกนค่าที่สอง:  
  - **AxisId** – ตัวระบุของแกน  
  - **IsVisible** – ค่าบูลีนที่บ่งชี้ว่าแสดงแกนหรือไม่  
  - **MinimumScale** – ค่าน้อยสุดที่แสดงบนแกน  
  - **MaximumScale** – ค่ามากสุดที่แสดงบนแกน  
  - **MajorUnit** – ช่วงระหว่างเส้นขีดใหญ่  
  - **MinorUnit** – ช่วงระหว่างเส้นขีดเล็ก  
  - **Title** – ข้อความหัวเรื่องของแกน

**การตอบกลับข้อผิดพลาด** (ไม่ใช่ 200)

- `400 Bad Request` – พารามิเตอร์ไม่ถูกต้องหรือคำขอผิดรูปแบบ  
- `401 Unauthorized` – ไม่มีหรือโทเค็น JWT ไม่ถูกต้อง  
- `404 Not Found` – ไฟล์ แผ่นงาน หรือแผนภูมิที่ระบุไม่มีอยู่  
- `500 Internal Server Error` – ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
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
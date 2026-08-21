---
title: "ลบแผนภูมิทั้งหมดออกจากเวิร์กชีต"
type: docs
url: /th/charts/clear/
aliases: [  /th/delete-all-charts-from-a-worksheet/ ]
weight: 30
keywords: "Aspose.Cells, Cloud, delete, all charts, worksheet, REST API, DELETE, SDK"
description: "เรียนรู้วิธีการลบแผนภูมิทั้งหมดในเวิร์กชีตโดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ซึ่งประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL, โค้ดตัวอย่าง SDK, ขั้นตอนการตรวจสอบสิทธิ์ และการจัดการข้อผิดพลาด"
ArticleTitle: "ลบแผนภูมิทั้งหมดออกจากเวิร์กชีตโดยใช้ Aspose.Cells Cloud API"
---

REST API นี้จะลบแผนภูมิทั้งหมดออกจากเวิร์กชีตที่ระบุ

**พื้นฐาน** – การลบแผนภูมิทั้งหมดออกจากเวิร์กชีตเป็นสิ่งที่มีประโยชน์เมื่อคุณต้องการรีเซ็ตเลย์เอาต์เชิงภาพของแผ่นงาน แทนที่การนำเสนอข้อมูลที่ล้าสมัย หรือเตรียมสมุดงานให้พร้อมใช้งานอีกครั้งโดยไม่ต้องเก็บข้อมูลแผนภูมิเดิมไว้

ก่อนเรียก API โปรดตรวจสอบให้แน่ใจว่ามีเงื่อนไขต่อไปนี้:

- มี JWT token ที่ถูกต้องสำหรับการตรวจสอบสิทธิ์  
- ไฟล์สมุดงานมีอยู่ในตำแหน่งที่จัดเก็บและโฟลเดอร์ที่ระบุ  
- คุณกำลังใช้เวอร์ชัน API **v3.0**

## DeleteWorksheetClearCharts API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้ JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                               |
| ---------------- | ------ | -------- | -------------------------------------- |
| name             | string | path     | ชื่อไฟล์สมุดงาน                        |
| sheetName        | string | path     | ชื่อเวิร์กชีต                          |
| folder           | string | query    | โฟลเดอร์ที่จัดเก็บสมุดงาน             |
| storageName      | string | query    | ชื่อของพื้นที่จัดเก็บ (storage)        |

**ส่วนหัวของคำขอ**

| ส่วนหัว          | คำอธิบาย                         |
|-----------------|---------------------------------|
| Authorization   | Bearer `<jwt token>`            |
| Accept          | `application/json`              |
| Content-Type    | `application/json` (ไม่มี body) |

**เนื้อหาของคำขอ (Request Body)**

การดำเนินการ DELETE **ไม่จำเป็นต้องมี** เนื้อหาคำขอ

**การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400 | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized                | JWT token ไม่ถูกต้องหรือขาดหาย                    |
| 413 | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด         |
| 500 | Internal Server Error       | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์          |

*ตัวอย่างการตอบกลับข้อผิดพลาด*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "พารามิเตอร์ไม่ถูกต้อง: ต้องระบุ 'sheetName'"
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "การตรวจสอบสิทธิ์ล้มเหลว: JWT token ไม่ถูกต้อง"
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "ขนาดของเนื้อหาคำขอเกินขนาดสูงสุดที่อนุญาต"
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์"
}
```

## วิธีการใช้ DeleteWorksheetClearCharts API ร่วมกับ SDK

### ข้อมูลจำเพาะของ DeleteWorksheetClearCharts API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถสื่อสารผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่ง (command-line tool) เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```


{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนาเมื่อคุณต้องการ **ลบแผนภูมิทั้งหมด** ออกจากเวิร์กชีต SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกเว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---
title: "อัปเดตแกนค่าที่สองของแผนภูมิ"
ArticleTitle: "อัปเดตแกนค่าที่สองของแผนภูมิ – Aspose.Cells Cloud REST API"
type: docs
url: /th/charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart API, Second Value Axis, Excel, REST, Cloud SDK"
description: "อัปเดตแกนค่าที่สองของแผนภูมิในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างคำขอ โค้ดสถานะการตอบกลับ และข้อกำหนดเบื้องต้น"
---

REST API นี้ใช้สำหรับอัปเดตแกนค่าที่สองของแผนภูมิ

**ข้อกำหนดเบื้องต้น:**  
- โทเค็น JWT ที่ใช้งานได้ (ดูเพิ่มเติมได้ที่[คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/cells/authentication/))  
- ไฟล์ Excel เป้าหมายต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud (ระบุ `folder` และ `storageName` (ถ้ามี))  
- ใช้เวอร์ชัน API v3.0; ตรวจสอบให้แน่ใจว่า URL ฐานคือ `https://api.aspose.cloud/v3.0`

## API PostChartSecondValueAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบใช้โทเค็น <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>

### พารามิเตอร์คำขอ

| พารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| -------------- | ------- | -------- | ------------------------------------------------- |
| name           | string  | path     | ชื่อไฟล์ Excel |
| sheetName      | string  | path     | ชื่อแผ่นงานที่มีแผนภูมิ |
| chartIndex     | integer | path     | ดัชนีของแผนภูมิที่ต้องการแก้ไข (เริ่มต้นที่ 0) |
| axis           | object  | body     | การตั้งค่าสำหรับแกนค่าที่สอง |
| folder         | string  | query    | ตำแหน่งโฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่ |
| storageName    | string  | query    | ชื่อของบริการพื้นที่จัดเก็บ |

**ตัวอย่างเนื้อหาคำขอ (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Secondary Axis"
  }
}
```

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์สูญหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือสูญหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | Internal Server Error       | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์โดยไม่คาดคิด |

**ดูเพิ่มเติม:**  
- [รับแกนค่าที่สองของแผนภูมิ](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [อัปเดตแกนค่าของแผนภูมิ](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่[repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ตัวอย่าง C# สำหรับอัปเดตแกนค่าที่สอง
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// ตัวอย่าง Java สำหรับอัปเดตแกนค่าที่สอง
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// ตัวอย่าง PHP สำหรับอัปเดตแกนค่าที่สอง
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# ตัวอย่าง Ruby สำหรับอัปเดตแกนค่าที่สอง
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# ตัวอย่าง Python สำหรับอัปเดตแกนค่าที่สอง
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// ตัวอย่าง Android (Java) – เหมือนกับตัวอย่าง Java ด้านบน
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// ตัวอย่าง Swift สำหรับอัปเดตแกนค่าที่สอง
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# ตัวอย่าง Perl สำหรับอัปเดตแกนค่าที่สอง
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// ตัวอย่าง Go สำหรับอัปเดตแกนค่าที่สอง
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}
---
title: "รับหัวเรื่องของแผนภูมิจากแผ่นงาน"
type: docs
url: /th/charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "หัวเรื่องแผนภูมิ"
  - "Excel"
  - "REST API"
  - "รับหัวเรื่องแผนภูมิ"
  - "cURL"
  - "SDK"
  - "การอัตโนมัติแผนภูมิ Excel"
  - "GET chart title"
description: "เรียนรู้วิธีดึงหัวเรื่องของแผนภูมิจากแผ่นงานในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึง endpoint, พารามิเตอร์, การยืนยันตัวตน, ตัวอย่างโค้ด cURL และ SDK"
ArticleTitle: "รับหัวเรื่องของแผนภูมิจากแผ่นงาน"
---

REST API นี้ใช้สำหรับดึงหัวเรื่องของแผนภูมิที่จัดเก็บอยู่ในแผ่นงานของสมุดงาน Excel

**ข้อกำหนดเบื้องต้น**: เพื่อเรียก endpoint นี้ คุณต้องมีโทเคน JWT หรือ OAuth2 ของ Aspose.Cells Cloud ที่ถูกต้องพร้อมขอบเขตสิทธิ์ `Cells.Read` สมุดงานต้องถูกอัปโหลดไว้ยังตำแหน่งที่จัดเก็บที่ระบุไว้แล้ว

## API GetWorksheetChartTitle

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                        |
| ---------------- | ---------- | -------- | ------------------------------------------------ |
| name             | string     | path     | ชื่อไฟล์สมุดงาน                                |
| sheetName        | string     | path     | ชื่อแผ่นงานที่มีแผนภูมิ                        |
| chartIndex       | integer    | path     | ดัชนีของแผนภูมิ (เริ่มต้นที่ 0)                 |
| folder           | string     | query    | เส้นทางโฟลเดอร์ที่จัดเก็บสมุดงาน                |
| storageName      | string     | query    | ชื่อของบริการจัดเก็บข้อมูล                      |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือคำสั่ง **cURL** เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "ยอดขาย Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**ฟิลด์ในคำตอบ**

| ฟิลด์               | คำอธิบาย                                             |
| -------------------- | ------------------------------------------------------ |
| `Title.Text`         | ข้อความที่แสดงเป็นหัวเรื่องของแผนภูมิ                |
| `Title.Font.Name`    | ชื่อตระกูลของฟอนต์ที่ใช้กับหัวเรื่อง (เช่น _Arial_)   |
| `Title.Font.Size`    | ขนาดฟอนต์เป็นจุด (points)                             |
| `Title.Font.IsBold`  | ระบุว่าข้อความหัวเรื่องเป็นตัวหนาหรือไม่              |

**โค้ดสถานะของคำตอบ**

| โค้ด | คำอธิบาย |
|------|----------|
| 200 OK | ดึงหัวเรื่องของแผนภูมิสำเร็จ                         |
| 401 Unauthorized | การยืนยันตัวตนล้มเหลว หรือโทเคนหาย/ไม่ถูกต้อง       |
| 404 Not Found | สมุดงาน แผ่นงาน หรือแผนภูมิที่ระบุไม่มีอยู่จริง       |
| 500 Internal Server Error | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์             |

**หมายเหตุ**: ดัชนีของแผนภูมิเริ่มต้นที่ 0; ตรวจสอบให้แน่ใจว่าแผนภูมินั้นมีอยู่จริง หากยังไม่ได้อัปโหลดสมุดงาน ให้อัปโหลดก่อนโดยใช้ API ที่เหมาะสม

**วิธีการแยกหัวเรื่องในสคริปต์ (ใช้ `jq`)**

```bash
# สมมติว่าคำตอบ JSON ถูกบันทึกไว้ในไฟล์ response.json
title=$(jq -r '.Title.Text' response.json)
echo "หัวเรื่องแผนภูมิ: $title"
```

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ตัวอย่าง C# โดยใช้ Aspose.Cells Cloud SDK
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// ตัวอย่าง Java โดยใช้ Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// ตัวอย่าง PHP โดยใช้ Aspose.Cells Cloud SDK
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# ตัวอย่าง Ruby โดยใช้ Aspose.Cells Cloud SDK
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# ตัวอย่าง Python โดยใช้ Aspose.Cells Cloud SDK
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// ตัวอย่าง Node.js โดยใช้ Aspose.Cells Cloud SDK
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt token>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// ตัวอย่าง Android (Java) โดยใช้ Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// ตัวอย่าง Swift โดยใช้ Aspose.Cells Cloud SDK
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("หัวเรื่องแผนภูมิ: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# ตัวอย่าง Perl โดยใช้ Aspose.Cells Cloud SDK
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt token>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

คุณยังสามารถดูเอกสาร SDK แต่ละตัวเพิ่มเติมสำหรับสถานการณ์ขั้นสูง เช่น การอัปเดตหรือลบหัวเรื่องของแผนภูมิ

**ดูเพิ่มเติม**: [อัปเดตหัวเรื่องของแผนภูมิ](/th/charts/title/put/), [ลบหัวเรื่องของแผนภูมิ](/th/charts/title/delete/).
---
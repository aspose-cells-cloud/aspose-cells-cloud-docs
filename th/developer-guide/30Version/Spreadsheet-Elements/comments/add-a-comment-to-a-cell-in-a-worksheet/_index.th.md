---
---
title: "เพิ่มคอมเมนต์ในชีต"
description: "เพิ่มคอมเมนต์ลงในเซลล์เฉพาะในชีต Excel โดยใช้ Aspose.Cells Cloud REST API (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})"
keywords: "Aspose.Cells, Cloud API, เพิ่มคอมเมนต์ในชีต, Excel, Spreadsheet, Cell Comment"
weight: 20
api_version: "v3.0"
---

# เพิ่มคอมเมนต์ในชีต

เพิ่มคอมเมนต์ลงในเซลล์เฉพาะในชีตของสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API

---

## ข้อกำหนดเบื้องต้น / การยืนยันตัวตน

* จำเป็นต้องมี **Bearer JWT token** สำหรับทุกคำขอ  
  *รับ token* ผ่าน endpoint **/connect/token** (ดูคู่มือ [การยืนยันตัวตน](/cells/authentication/))  
* แนบ token ลงใน header `Authorization`:

```http
Authorization: Bearer <jwt token>
```

* คำขอทั้งหมดต้องส่งผ่าน **HTTPS** เพื่อความปลอดภัยของ token และข้อมูล

---

## คำขอ HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### พารามิเตอร์ใน Path

| ชื่อพารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|------------------|--------|--------|-----------|
| `name`           | string | ✔️ | ชื่อไฟล์สมุดงาน (เช่น `test.xlsx`) |
| `sheetName`      | string | ✔️ | ชื่อชีต (เช่น `Sheet1`) |
| `cellName`       | string | ✔️ | ที่อยู่ของเซลล์เป้าหมาย (เช่น `A1`) |

### พารามิเตอร์ใน Query String

| ชื่อพารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|------------------|--------|--------|-----------|
| `folder`         | string | ไม่จำเป็น | โฟลเดอร์ที่เก็บสมุดงานไว้ |
| `storageName`    | string | ไม่จำเป็น | ชื่อของบริการจัดเก็บข้อมูลที่ไฟล์อยู่ |

### ร่างคำขอ (Request Body)

ร่างคำขอต้องมีวัตถุ **Comment** ในรูปแบบ JSON

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**ฟิลด์ของวัตถุ Comment**

| ฟิลด์                     | ประเภท  | จำเป็น | คำอธิบาย |
|---------------------------|---------|--------|-----------|
| `CellName`                | string  | ✔️ | ที่อยู่เซลล์ (ต้องตรงกับค่า `{cellName}` ใน path) |
| `Author`                  | string  | ไม่จำเป็น | ชื่อผู้เขียนคอมเมนต์ |
| `HtmlNote`                | string  | ไม่จำเป็น | ข้อความคอมเมนต์ในรูปแบบ HTML |
| `Note`                    | string  | ไม่จำเป็น | ข้อความคอมเมนต์แบบ plain text |
| `AutoSize`                | boolean | ไม่จำเป็น | ปรับขนาดกล่องคอมเมนต์อัตโนมัติ |
| `IsVisible`               | boolean | ไม่จำเป็น | แสดงคอมเมนต์ตามค่าเริ่มต้น |
| `Width` / `Height`        | number  | ไม่จำเป็น | ขนาดกล่องคอมเมนต์ (หน่วย: จุด) |
| `TextHorizontalAlignment` | string  | ไม่จำเป็น | การจัดแนวแนวนอน (`Left`, `Center`, `Right`) |
| `TextOrientationType`     | string  | ไม่จำเป็น | การหมุนข้อความ (`NoRotation`, `Rotate90`, …) |
| `TextVerticalAlignment`   | string  | ไม่จำเป็น | การจัดแนวแนวตั้ง (`Top`, `Center`, `Bottom`) |

---

## ตัวอย่าง cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## โครงสร้างคำตอบ

| ฟิลด์   | ประเภท | คำอธิบาย |
|---------|--------|-----------|
| `Comment` | object | วัตถุคอมเมนต์ที่สร้างขึ้น (ดู **ฟิลด์ของวัตถุ Comment** ข้างต้น รวมถึง metadata ของลิงก์) |
| `Code`   | integer | HTTP status code ที่ API ส่งกลับมา (เช่น `200`) |
| `Status` | string  | ข้อความแสดงสถานะ (เช่น `"OK"`) |

วัตถุ `Comment` ยังมีซับเจกต์ **link** อีกด้วย:

| ฟิลด์ย่อย | ประเภท | คำอธิบาย |
|-----------|--------|-----------|
| `Href`    | string | URL อ้างอิงตัวเองของทรัพยากรคอมเมนต์ |
| `Rel`     | string | ประเภทความสัมพันธ์ (`self`) |
| `Title`   | string | ชื่อเรื่อง (อาจเป็น `null`) |
| `Type`    | string | MIME type (อาจเป็น `null`) |

---

## ตัวอย่างคำตอบที่สำเร็จ

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## การตอบกลับเมื่อเกิดข้อผิดพลาด

| HTTP Code | คำอธิบาย | ตัวอย่าง |
|-----------|-----------|---------|
| **400**   | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหรือผิดรูปแบบ | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401**   | ไม่ได้รับอนุญาต – token ขาดหรือไม่ถูกต้อง | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**   | ไม่พบ – สมุดงาน ชีต หรือเซลล์ไม่มีอยู่จริง | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }` |
| **500**   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์ | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## ตัวอย่าง SDK

SDK ต่อไปนี้มีตัวห่อ (wrapper) สำเร็จรูปสำหรับการดำเนินการนี้ แทนค่าตัวแปรที่เป็น placeholder (`<YOUR_TOKEN>`, `<FILE_NAME>` เป็นต้น) ด้วยข้อมูลจริง

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Configure API client
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Prepare comment object
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.PutWorksheetComment: " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<your_client_id>');
$config->setAppKey('<your_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->put_worksheet_comment: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<your_client_id>';
config.clientSecret = '<your_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<your_client_id>',
    client_secret => '<your_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "Exception when calling WorksheetsApi->put_worksheet_comment: $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<your_client_id>"
    cfg.ClientSecret = "<your_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Error: %v\\n", err)
    } else {
        fmt.Printf("Response: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## ดูเพิ่มเติม

* **รับคอมเมนต์ในชีต** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **แก้ไขคอมเมนต์ในชีต** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **ลบคอมเมนต์ในชีต** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **ล้างคอมเมนต์ทั้งหมด** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## หมายเหตุเพิ่มเติม

* Path endpoint นี้มีเวอร์ชัน **v3.0** เวอร์ชันใหม่กว่า (**v3.1**) มีให้ใช้งานแล้ว ควรอัปเดต URL หลักให้สอดคล้องหากต้องการใช้ฟีเจอร์ล่าสุด  
* สำหรับ OpenAPI definition แบบเต็ม โปรดเยี่ยมชม [เอกสารอ้างอิง Aspose.Cells Cloud API](/cells/#/Worksheets/PutWorksheetComment)  
* อย่าลืมจัดการอัตราการใช้งาน (HTTP 429) และ retry ตามแนวทางของ API
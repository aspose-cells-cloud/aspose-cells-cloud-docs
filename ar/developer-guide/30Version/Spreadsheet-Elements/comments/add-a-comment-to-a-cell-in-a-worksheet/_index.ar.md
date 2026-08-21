---
title: "إضافة تعليق إلى ورقة العمل"
description: "أضف تعليقًا إلى خلية محددة في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})."
keywords: "Aspose.Cells, واجهة سحابية, إضافة تعليق إلى ورقة العمل, Excel, جدول بيانات, تعليق الخلية"
weight: 20
api_version: "v3.0"
---

# إضافة تعليق إلى ورقة العمل

أضف تعليقًا إلى خلية محددة في ورقة عمل من ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API.

---

## المتطلبات المسبقة / المصادقة

* يلزم وجود **رمز مميز JWT من نوع Bearer** لكل طلب.  
  *احصل على رمز مميز* عبر نقطة نهاية **/connect/token** (انظر [دليل المصادقة](/cells/authentication/)).  
* تضمين الرمز المميز في رأس `Authorization`:

```http
Authorization: Bearer <jwt token>
```

* يجب تنفيذ جميع الاستدعاءات عبر **HTTPS** لحماية الرمز المميز والبيانات.

---

## طلب HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### معاملات المسار (Path Parameters)

| الاسم         | النوع    | مطلوب | الوصف |
|--------------|----------|--------|---------|
| `name`       | نص (string) | ✔️ | اسم ملف المصنف (مثل `test.xlsx`). |
| `sheetName`  | نص (string) | ✔️ | اسم ورقة العمل (مثل `Sheet1`). |
| `cellName`   | نص (string) | ✔️ | عنوان الخلية المستهدفة (مثل `A1`). |

### معاملات الاستعلام (Query Parameters)

| الاسم          | النوع    | مطلوب | الوصف |
|---------------|----------|--------|---------|
| `folder`      | نص (string) | اختياري | المجلد الذي يحتوي على المصنف. |
| `storageName` | نص (string) | اختياري | اسم خدمة التخزين التي يوجد فيها الملف. |

### جسم الطلب (Request Body)

يجب أن يحتوي جسم الطلب على كائن **Comment** بصيغة JSON.

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

**حقول كائن Comment**

| الحقل                      | النوع     | مطلوب | الوصف |
|----------------------------|-----------|--------|---------|
| `CellName`                 | نص (string) | ✔️ | عنوان الخلية (يجب أن يطابق قيمة `{cellName}` في المسار). |
| `Author`                   | نص (string) | اختياري | اسم مؤلف التعليق. |
| `HtmlNote`                 | نص (string) | اختياري | نص التعليق بتنسيق HTML. |
| `Note`                     | نص (string) | اختياري | نص التعليق العادي (بدون تنسيق). |
| `AutoSize`                 | منطقي (boolean) | اختياري | ضبط حجم مربع التعليق تلقائيًا. |
| `IsVisible`                | منطقي (boolean) | اختياري | إظهار التعليق بشكل افتراضي. |
| `Width` / `Height`         | رقم (number) | اختياري | حجم مربع التعليق (بالنقاط). |
| `TextHorizontalAlignment` | نص (string) | اختياري | المحاذاة الأفقية (`Left`، `Center`، `Right`). |
| `TextOrientationType`      | نص (string) | اختياري | دوران النص (`NoRotation`، `Rotate90`، إلخ). |
| `TextVerticalAlignment`   | نص (string) | اختياري | المحاذاة العمودية (`Top`، `Center`، `Bottom`). |

---

## مثال باستخدام cURL

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

## مخطط الاستجابة

| الحقل      | النوع    | الوصف |
|------------|----------|---------|
| `Comment`  | كائن (object) | كائن التعليق المُنشأ (انظر **حقول كائن Comment** أعلاه، بالإضافة إلى بيانات رابط التعريف). |
| `Code`     | عدد صحيح (integer) | رمز حالة HTTP الذي تعيده الواجهة (مثل `200`). |
| `Status`   | نص (string) | رسالة الحالة النصية (مثل `"OK"`). |

كما يحتوي كائن `Comment` على كائن فرعي **link**:

| الحقل الفرعي | النوع    | الوصف |
|--------------|----------|---------|
| `Href`       | نص (string) | رابط مرجعي ذاتي لمورد التعليق. |
| `Rel`        | نص (string) | نوع العلاقة (`self`). |
| `Title`      | نص (string) | عنوان اختياري (قد يكون `null`). |
| `Type`       | نص (string) | نوع MIME اختياري (قد يكون `null`). |

---

## مثال على استجابة ناجحة

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

## استجابات الأخطاء

| رمز HTTP | الوصف | مثال |
|-----------|--------|-------|
| **400**   | طلب غير صالح – معلمات مفقودة أو غير صحيحة. | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401**   | غير مصرح به – رمز مميز مفقود أو غير صالح. | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**   | غير موجود – المصنف أو ورقة العمل أو الخلية غير موجودة. | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }` |
| **500**   | خطأ داخلي في الخادم – حالة غير متوقعة على الخادم. | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## أمثلة على SDKs

توفر حزم SDK التالية واجهات جاهزة لهذه العملية. استبدل القيم الوهمية (`<YOUR_TOKEN>`، `<FILE_NAME>`، إلخ) ببيانات فعلية.

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

## انظر أيضًا

* **الحصول على تعليق ورقة العمل** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **تحديث تعليق ورقة العمل** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **حذف تعليق ورقة العمل** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **مسح جميع التعليقات** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## ملاحظات إضافية

* يحتوي مسار نقطة النهاية على **v3.0**. تتوفر نسخة أحدث (**v3.1**)؛ قم بتحديث عنوان URL الأساسي وفقًا لذلك إذا احتجت إلى أحدث الميزات.  
* لرؤية تعريف OpenAPI الكامل، قم بزيارة [مرجع واجهة Aspose.Cells Cloud API](/cells/#/Worksheets/PutWorksheetComment).  
* تذكّر التعامل مع قيود المعدل (HTTP 429) وإعادة المحاولة وفقًا لإرشادات الواجهة.  

---
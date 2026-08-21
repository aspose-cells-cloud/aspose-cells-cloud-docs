---
title: "الحصول على عنوان المخطط من ورقة عمل"
type: docs
url: /ar/charts/title/get/
aliases: [  /ar/get-chart-title-from-a-worksheet/ ]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "عنوان المخطط"
  - "Excel"
  - "واجهة برمجة تطبيقات REST"
  - "الحصول على عنوان المخطط"
  - "cURL"
  - "مكتبة SDK"
  - "أتمتة مخططات Excel"
  - "GET chart title"
description: "تعلم كيفية استرجاع عنوان مخطط من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. تتضمن النهاية النهائية (Endpoint)، والمتغيرات، ومصادقة الهوية، وكود مثال باستخدام cURL ومكتبات SDK."
ArticleTitle: "الحصول على عنوان المخطط من ورقة عمل"
---

تسترد هذه الواجهة REST عنوان المخطط المخزن في ورقة عمل من ملف Excel.

**المتطلبات المسبقة**: لاستدعاء هذه النهاية النهائية، يجب أن يكون لديك رمز وصول صحيح لـ Aspose.Cells Cloud باستخدام OAuth2/JWT مع نطاق `Cells.Read`. كما يجب أن يكون ملف المصنف مرفوعًا مسبقًا إلى موقع التخزين المحدد.

## واجهة برمجة تطبيقات GetWorksheetChartTitle

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **الأمان والمصادقة**

تستخدم واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة تعتمد على رمز <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a> وتُعد آمنة.

### متغيرات الطلب

| اسم المتغير | النوع | الموقع | الوصف |
| ------------ | ------- | -------- | ---------------------------------------------- |
| name | string | path | اسم ملف المصنف |
| sheetName | string | path | اسم ورقة العمل التي تحتوي على المخطط |
| chartIndex | integer | path | المؤشر (من صفر) للمخطط |
| folder | string | query | مسار المجلد الذي يحتوي على المصنف |
| storageName | string | query | اسم خدمة التخزين |

يعرّف <a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle" rel="noopener noreferrer">مواصفة OpenAPI</a> واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

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
    "Text": "Sales Q1",
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

**حقول الاستجابة**

| الحقل | الوصف |
| ------------------- | ----------------------------------------------- |
| `Title.Text` | النص الفعلي المعروض كعنوان للمخطط |
| `Title.Font.Name` | عائلة الخط المستخدمة في العنوان (مثل _Arial_) |
| `Title.Font.Size` | حجم الخط بالنقاط |
| `Title.Font.IsBold` | يشير إلى ما إذا كان نص العنوان عريضًا (Bold) |

**رموز حالة الاستجابة**

| الكود | الوصف |
|------|-------------|
| 200 OK | تم استرجاع عنوان المخطط بنجاح |
| 401 Unauthorized | فشلت المصادقة أو أن الرمز مفقود/غير صالح |
| 404 Not Found | المصنف أو الورقة أو المخطط المحدد غير موجود |
| 500 Internal Server Error | حدث خطأ غير متوقع في الخادم |

**ملاحظات**: المؤشر للمخطط يبدأ من الصفر؛ تأكد من وجود المخطط. وإذا لم يكن المصنف مرفوعًا، فارفعه أولًا باستخدام الواجهة المناسبة.

**كيفية استخراج العنوان في سكريبت (باستخدام `jq`)**

```bash
# بافتراض أن الاستجابة بصيغة JSON محفوظة في response.json
title=$(jq -r '.Title.Text' response.json)
echo "Chart title: $title"
```

## عائلة مكتبات SDK السحابية

استخدام مكتبة SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى مكتبات SDK إدارة التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

توضح أمثلة الرمز التالية كيفية إجراء استدعاءات إلى خدمات Aspose.Cells عبر واجهة الويب باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// مثال بلغة C# باستخدام مكتبة Aspose.Cells Cloud SDK
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
// مثال بلغة Java باستخدام مكتبة Aspose.Cells Cloud SDK
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
// مثال بلغة PHP باستخدام مكتبة Aspose.Cells Cloud SDK
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
# مثال بلغة Ruby باستخدام مكتبة Aspose.Cells Cloud SDK
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
# مثال بلغة Python باستخدام مكتبة Aspose.Cells Cloud SDK
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
// مثال بلغة Node.js باستخدام مكتبة Aspose.Cells Cloud SDK
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
// مثال لـ Android (Java) باستخدام مكتبة Aspose.Cells Cloud SDK
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
// مثال بلغة Swift باستخدام مكتبة Aspose.Cells Cloud SDK
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Chart title: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# مثال بلغة Perl باستخدام مكتبة Aspose.Cells Cloud SDK
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

كما يمكنك الرجوع إلى وثائق كل مكتبة SDK على حدة لمزيد من السيناريوهات المتقدمة، مثل تحديث أو حذف عنوان المخطط.

**انظر أيضًا**: [تحديث عنوان المخطط](/charts/title/put/)، [حذف عنوان المخطط](/charts/title/delete/).
---
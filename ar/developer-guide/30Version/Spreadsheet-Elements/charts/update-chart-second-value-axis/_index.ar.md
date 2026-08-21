---
title: "تحديث المحور القيمي الثاني للرسم البياني"
ArticleTitle: "تحديث المحور القيمي الثاني للرسم البياني – Aspose.Cells Cloud REST API"
type: docs
url: /ar/charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart API, Second Value Axis, Excel, REST, Cloud SDK"
description: "تحديث المحور القيمي الثاني للرسم البياني في ورقة عمل Excel باستخدام Aspose.Cells Cloud REST API. يتضمن أمثلة على الطلبات وأكواد الاستجابة والمتطلبات الأساسية."
---

يقوم هذا الـ REST API بتحديث المحور القيمي الثاني للرسم البياني.

**المتطلبات الأساسية:**  
- رمز وصول JWT صالح (انظر [دليل المصادقة](https://docs.aspose.cloud/cells/authentication/)).  
- يجب تخزين ملف Excel المستهدف في مساحة تخزين Aspose Cloud (يُقدَّم `folder` واسم `storageName` اختياريًا).  
- تُستخدم إصدارة الـ API v3.0؛ تأكد أن عنوان URL الأساسي هو `https://api.aspose.cloud/v3.0`.

## PostChartSecondValueAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| -------------- | ------- | -------- | ------------------------------------------------- |
| name           | string  | path     | اسم ملف Excel.                           |
| sheetName      | string  | path     | اسم ورقة العمل التي يحتوي عليها الرسم البياني.       |
| chartIndex     | integer | path     | مؤشر الرسم البياني المراد تعديله (يبدأ من الصفر).          |
| axis           | object  | body     | الإعدادات الخاصة بالمحور القيمي الثاني.               |
| folder         | string  | query    | مسار المجلد داخل مساحة التخزين التي يوجد فيها الملف. |
| storageName    | string  | query    | اسم خدمة التخزين.                      |

**مثال على جسم الطلب (JSON):**

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

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) واجهة برمجة تطبيقات متاحة للعامة، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

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

**أكواد حالة HTTP**

| الكود | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (تم بنجاح)                          | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request (طلب خاطئ)                 | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized (غير مصرّح)                | رمز JWT غير صالح أو مفقود. |
| 413  | Payload Too Large (حمولة كبيرة جدًا)           | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500  | Internal Server Error (خطأ داخلي في الخادم)       | خطأ غير متوقع في الخادم. |

**انظر أيضًا:**  
- [الحصول على المحور القيمي الثاني للرسم البياني](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [تحديث المحور القيمي للرسم البياني](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. حيث يعتني SDK بالتفاصيل منخفضة المستوى ويجعلك تركز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// مثال C# لتحديث المحور القيمي الثاني
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// مثال Java لتحديث المحور القيمي الثاني
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// مثال PHP لتحديث المحور القيمي الثاني
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# مثال Ruby لتحديث المحور القيمي الثاني
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# مثال Python لتحديث المحور القيمي الثاني
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
// مثال Android (Java) – نفسه كما في مقتطف Java أعلاه
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// مثال Swift لتحديث المحور القيمي الثاني
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# مثال Perl لتحديث المحور القيمي الثاني
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// مثال Go لتحديث المحور القيمي الثاني
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}
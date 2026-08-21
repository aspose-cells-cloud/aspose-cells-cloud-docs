---
title: "إزالة التكرارات"
ArticleTitle: "إزالة التكرارات – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktitle: "إزالة التكرارات"
type: docs
url: /ar/cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells، إزالة التكرارات، واجهة برمجة تطبيقات"
description: "يزيل القيم المكرَّرة في ورقة العمل أو النطاق أو الجدول."
weight: 1000
---

## إزالة التكرارات في خدمات الويب Aspose.Cells Cloud

يزيل القيم المكرَّرة في ورقة العمل أو النطاق أو الجدول. تقوم هذه الطريقة بمسح النطاق المستهدف للبحث عن الصفوف ذات القيم المتطابقة في الأعمدة المحددة المراد التحقق منها. ولكل مجموعة من القيم المكرَّرة، تُزال جميع الحالات ما عدا الحالة الأولى. يكون المقارنة عادةً حساسة لحالة الأحرف وتتطابق مع القيمة الدقيقة للخلية.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار/سلسلة الاستعلام/جسم HTTP | الوصف |
|-------------|--------|----------------------------------|---------|
| Spreadsheet | ملف | FormData | تحميل ملف جدول البيانات. |
| worksheet | نص | استعلام | اسم ورقة العمل. (اختياري) |
| range | نص | استعلام | اسم النطاق الذي يجب إزالة التكرارات منه. (اختياري) |
| table | نص | استعلام | اسم الجدول الذي يجب إزالة التكرارات منه. (اختياري) |
| outPath | نص | استعلام | (اختياري) مسار المجلد الذي يُخزَّن فيه ملف جدول البيانات. القيمة الافتراضية هي null. |
| outStorageName | نص | استعلام | اسم مساحة التخزين للملف الناتج. |
| region | نص | استعلام | إعدادات إقليم/لغة جدول البيانات (مثل `en-US`، `fr-FR`). تؤثر على تنسيق الأرقام وتحليل التواريخ والسلوك المتعلق بالإعدادات الإقليمية. |
| password | نص | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **الاستجابة**

```json
{
  "File": "تيار ثنائي لجدول البيانات الناتج (مثل .xlsx)"
}
```

**كود حالات الاستجابة**

| الكود | المعنى | الوصف |
|------|---------|--------|
| 200 | ناجح | يتم إرجاع جدول البيانات الناتج مع إزالة التكرارات كتيار ملف. |
| 400 | طلب غير صالح | معاملات طلب غير صالحة أو عنوان URL غير منسق. |
| 401 | غير مصرح به | فشلت المصادقة أو لم تُقدَّم أي بيانات اعتماد. |
| 413 | حجم الحمولة كبير جدًا | يتجاوز حجم الملف المرفَع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | واجه جدول البيانات حالة شاذة في الحصول على البيانات أو خطأ آخر من جانب الخادم. |

## كيفية استخدام إزالة التكرارات مع واجهات برمجة التطبيقات (SDKs)

### مواصفات إزالة التكرارات

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات إزالة التكرارات</a> واجهة برمجة برمجية متاحة علنًا وتتيح لك إجراء عمليات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# استخدم HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "تيار ثنائي لجدول البيانات الناتج (مثل .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### استخدام واجهات برمجة التطبيقات (SDKs) لـ Aspose Cells Cloud

استخدام واجهة برمجة التطبيقات (SDK) هي أسرع طريقة لتسريع عملية التطوير. تُجرِّد واجهة برمجة التطبيقات (SDK) التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بواجهات برمجة التطبيقات (SDKs) لـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات الويب Aspose Cells Cloud باستخدام واجهات برمجة التطبيقات (SDKs) المختلفة:

```csharp
// مثال رمز SDK بلغة C#
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// مثال رمز SDK بلغة Java
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# مثال رمز SDK بلغة Python
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Exception when calling TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---
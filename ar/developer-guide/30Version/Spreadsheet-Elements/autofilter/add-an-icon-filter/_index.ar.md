---
title: "إضافة مرشح أيقونات إلى ورقة عمل إكسل"
second_title: "مستند"
linktype: "إضافة مرشح أيقونات"
type: docs
url: /autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: "Aspose.Cells Cloud, إكسل, مرشح الأيقونات, المرشح التلقائي, REST API"
description: "تعرّف على كيفية إضافة مرشح أيقونات إلى ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API، مع تفاصيل الطلب، ومثال باستخدام cURL، وأكواد أمثلة للـ SDK، وإدارة الأخطاء."
weight: 65
ArticleTitle: "إضافة مرشح أيقونات إلى ورقة عمل إكسل – وثائق Aspose.Cells Cloud"
---

## واجهة برمجة التطبيقات REST

تُضيف هذه الواجهة **مرشح أيقونات** إلى ورقة عمل إكسل باستخدام **واجهة Aspose.Cells Cloud REST API**.

**الخلفية:** يطبّق مرشح الأيقونات مجموعة مرئية من الأيقونات على الخلايا بناءً على قيمها، مما يسمح بتحليل بصري سريع لاتجاهات البيانات. تشمل حالات الاستخدام الشائعة تسليط الضوء على مقاييس الأداء أو مؤشرات الحالة أو تصنيف القيم باستخدام أيقونات على شكل إشارات مرورية (مثل الإشارة الضوئية) مباشرةً داخل ورقات عمل إكسل.


```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة قائمة على رمز <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a>، وهي آمنة.

### معاملات الطلب:

| اسم المعامل | النوع   | الموقع | الوصف |
|-------------|---------|--------|--------|
| name        | string  | Path   | اسم ملف العمل (workbook). |
| sheetName   | string  | Path   | اسم ورقة العمل. |
| range       | string  | Query  | النطاق الخلوي (مثل `A1:B1`) الذي سيتم تطبيق المرشح عليه. |
| fieldIndex  | integer | Query  | الفهرس الصفر-based للعمود الذي يستهدفه المرشح. |
| iconSetType | string  | Query  | مجموعة الأيقونات المراد استخدامها. القيم المسموح بها: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId      | integer | Query  | المُعرّف الخاص بالأيقونة المحددة ضمن مجموعة الأيقونات المختارة. |
| matchBlanks | boolean | Query  | يحدد ما إذا كانت الخلايا الفارغة تُشمل (`true` أو `false`). |
| refresh     | boolean | Query  | يشير إلى ما إذا كان المرشح يجب أن يُحدّث بعد التطبيق (`true` أو `false`). |
| folder      | string  | Query  | المجلد الذي يحتوي على ملف العمل الأصلي. |
| storageName | string  | Query  | اسم وحدة التخزين التي يوجد فيها ملف العمل. |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف |
|-------|-----------------------------|--------|
| 200   | OK                          | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request                 | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401   | Unauthorized                | رمز JWT غير صالح أو مفقود. |
| 413   | Payload Too Large           | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500   | Internal Server Error       | خطأ داخلي في الخادم غير متوقع. |

## كيفية استخدام PutWorksheetIconFilter API باستخدام SDKs

### مواصفات PutWorksheetIconFilter API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) واجهة برمجة تطبيقات مفتوحة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
  -X PUT \
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

رموز حالات الاستجابة الممكنة:

| الرمز | الوصف |
|-------|--------|
| 200   | تم تطبيق المرشح بنجاح. |
| 400   | طلب غير صالح – معاملات مفقودة أو غير صحيحة. |
| 401   | غير مصرّح به – رمز مصادقة غير صالح أو مفقود. |
| 404   | ملف العمل أو ورقة العمل أو النطاق المحدد غير موجود. |
| 500   | خطأ داخلي في الخادم. |
{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تتعامل الـ SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

لمزيد من إمكانات المرشح التلقائي، راجع الوثائق حول **[إضافة مرشح لون](/autofilter/add-color-filter/)**، **[إضافة مرشح تواريخ](/autofilter/add-date-filter/)**، و **[مسح المرشح التلقائي](/autofilter/clear-autofilter/)**.
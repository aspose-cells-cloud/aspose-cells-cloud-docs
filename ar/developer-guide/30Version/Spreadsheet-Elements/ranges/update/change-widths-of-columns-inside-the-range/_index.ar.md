---
title: "تغيير عرض الأعمدة داخل نطاق"
ArticleTitle: "تغيير عرض الأعمدة داخل النطاق – واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktype: "docs"
url: /ranges/update/column-width/
aliases: [/change-widths-of-columns-inside-the-range/]
keywords: "Aspose.Cells، عرض العمود، واجهة REST API، Excel، SDK، نطاق، سحابة"
description: "تعلم كيفية تغيير عرض الأعمدة داخل النطاق باستخدام واجهة Aspose.Cells Cloud REST API أو SDKs (C#، Java، Python، إلخ). يتضمن تفاصيل cURL، والاستجابة، وخطوات المصادقة."
weight: 74
---

تقوم هذه الواجهة REST بتحديد عرض العمود لنطاق معين.

## الأمان والمصادقة
واجهات Aspose.Cells Cloud API آمنة وتحتاج إلى [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**المتطلبات المسبقة** – قبل استدعاء نقطة النهاية، يجب أن تقوم بما يلي:

1. إنشاء حساب Aspose Cloud والحصول على *مُعرّف العميل* و*سر العميل*.  
2. طلب رمز JWT من خلال استدعاء نقطة النهاية OAuth (`/connect/token`)؛ يُعاد الرمز في حقل `access_token`.  
3. رفع ملف المصنف المستهدف إلى مساحة التخزين الخاصة بـ Aspose Cloud (أو التأكد من وجوده مسبقًا في المجلد المحدد).  

معطيات الطلب هي:

| اسم المعطى | النوع | الموقع | الوصف |
|------------|--------|----------|-------------|
| name | نص | المسار | اسم ملف المصنف |
| sheetName | نص | المسار | اسم ورقة العمل |
| value | رقم | الاستعلام | القيمة المطلوبة لعرض العمود |
| range | كائن | الجسم | كائن النطاق الذي يُعرّف الخلايا المستهدفة |
| folder | نص | الاستعلام | مسار المجلد الذي يُخزّن فيه المصنف |
| storageName | نص | الاستعلام | اسم خدمة التخزين |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء مكالمات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

<h3 id="request">الطلب</h3>

```bash
# استدعاء نقطة النهاية لعرض العمود لمصنف *test.xlsx*،
# ورقة العمل *Sheet1*، وضبط عرض الأعمدة المحددة على 20 نقطة.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">الاستجابة</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*ردود الأخطاء المحتملة*  

| رمز HTTP | الوصف |
|-----------|-------------------------------------------|
| 400 | طلب غير صالح – JSON أو معطيات غير صحيحة |
| 401 | غير مخوّل – نقص أو صلاحية رمز غير صحيحة |
| 404 | غير موجود – غياب المصنف أو ورقة العمل |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير؛ حيث يتعامل SDK مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## الأسئلة الشائعة

**س:** *ما نقطة النهاية التي يجب استدعاؤها لضبط عرض عمود في نطاق داخل ملف Excel؟*  
**ج:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth`، حيث يُشير `{name}` إلى اسم ملف المصنف، و`{sheetName}` إلى ورقة العمل المستهدفة.

**س:** *كيف أُصادق الطلب عند استخدام واجهة ضبط عرض الأعمدة؟*  
**ج:** تضمين رأس `Authorization: Bearer <jwt token>`؛ احصل على رمز JWT عبر تدفق OAuth لـ Aspose Cloud (`/connect/token`) باستخدام مُعرّف العميل وسر العميل.

**س:** *ما محتوى JSON الذي يجب إرساله لتغيير عرض الأعمدة من A إلى C إلى 25 نقطة؟*  
**ج:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

أضف معطى الاستعلام `value=25` إلى عنوان URL للطلب.
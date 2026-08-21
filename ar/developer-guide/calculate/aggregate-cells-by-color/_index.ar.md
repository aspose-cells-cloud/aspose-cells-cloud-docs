---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – جمع وحساب القيم حسب اللون في إكسل"
second_title: "وثيقة"
ArticleTitle: "جمع وحساب القيم (المجموع، العدد، المتوسط، القيمة الصغرى، القيمة العظمى) حسب اللون في جدول بيانات/إكسل"
LinkTitle: "جمع الخلايا حسب اللون"
type: docs
url: /ar/aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregate, color, sum, count, average, min, max"
description: "اجمع خلايا إكسل حسب لون الخلفية أو لون الخط (المجموع، العدد، المتوسط، القيمة الصغرى، القيمة العظمى) باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. تعلّم نقطة النهاية، والمتغيرات، والمصادقة، وأمثلة SDK."
weight: 100
---

## نظرة عامة

يمكن للواجهة إجراء عمليات حسابية على البيانات بناءً على **لون** الخلايا. ويمكنها حساب المجموع، والعدد، والمتوسط، بالإضافة إلى تحديد القيمة العظمى والصغرى في جدول بيانات إكسل وفقًا للون ملء الخلية أو لون الخط.

| عملية الحساب | الوصف                                                        |
| :----------- | :----------------------------------------------------------- |
| العدد        | تحديد عدد الخلايا التي تحمل نفس اللون.                       |
| المجموع      | حساب القيمة الإجمالية للخلايا التي تحمل نفس اللون.          |
| القيمة العظمى | تحديد أعلى قيمة بين الخلايا التي تحمل نفس اللون.             |
| القيمة الصغرى | تحديد أقل قيمة بين الخلايا التي تحمل نفس اللون.              |
| القيمة المتوسطة | حساب القيمة المتوسطة للخلايا التي تحمل نفس اللون.          |

## واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المتغير     | النوع   | الموقع    | الوصف                                                         |
| :-------------- | :----- | :-------- | :------------------------------------------------------------ |
| Spreadsheet     | ملف   | FormData  | ملف جدول عمل إكسل المراد معالجته.                             |
| Worksheet       | نص     | Query     | اسم ورقة العمل التي تحتوي على النطاق.                          |
| Range           | نص     | Query     | النطاق بتنسيق A‑1 (مثل `A1:B10`).                            |
| Operation       | نص     | Query     | طريقة الحساب – `Sum` أو `Count` أو `Average` أو `Min` أو `Max`. |
| ColorPosition   | نص     | Query     | تحديد اللون المراد تقييمه – `Background` أو `Font`.           |
| Region          | نص     | Query     | إعداد منطقة جدول العمل (مثل `us-east-1`).                    |
| Password        | نص     | Query     | كلمة المرور لفتح ملف جدول عمل محمي (اختياري).                 |

#### التعدادات

- **ColorPosition**

  | القيمة      | المعنى                         |
  | :--------- | :---------------------------- |
  | Background | استخدام لون ملء الخلية.        |
  | Font       | استخدام لون خط الخلية.         |

**مثال على طلب multipart/form‑data**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### الاستجابة

توضّح المخطط التالي كائن الاستجابة. يلي المخطط مثال حقيقي.

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**مثال على استجابة حقيقية (بقيم فعلية)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**رموز حالة HTTP**

| الرمز | المعنى                 | الوصف                                                      |
| ----- | ----------------------- | ---------------------------------------------------------- |
| 200   | OK                      | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request             | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).     |
| 401   | Unauthorized            | رمز JWT غير صالح أو مفقود.                                |
| 413   | Payload Too Large       | حجم الملف المرفق يتجاوز الحد المسموح.                     |
| 500   | Internal Server Error   | خطأ في الخادم غير متوقع.                                  |

## أين ينبغي استخدام واجهة برمجة تطبيقات جمع الخلايا حسب اللون؟

في جدول البيانات، غالبًا ما تُرمّز البيانات الخاصة بالفئات المختلفة بلون معيّن. وتتيح لك هذه الواجهة حساب المجموع، والعدد، والمتوسط، أو تحديد القيمة الصغرى والعظمى لكل مجموعة ألوان، ما يبسّط تحليل البيانات المعتمد على اللون.

## لماذا يجب استخدام واجهة برمجة تطبيقات جمع الخلايا حسب اللون؟

توفر الواجهة طريقة سريعة وموثوقة لأداء الحسابات المعتمدة على اللون دون الحاجة إلى كتابة منطق مخصّص لتحليل البيانات. كما تتكامل بسلاسة مع مكتبات Aspose.Cells Cloud SDK، مما يسمح للمطورين بتطبيق جمع القيم حسب اللون باستخدام بضعة أسطر من الكود فقط.

## كيفية استخدام واجهة برمجة تطبيقات جمع الخلايا حسب اللون مع مكتبات SDK

### مواصفات واجهة برمجة تطبيقات جمع الخلايا حسب اللون

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات جمع الخلايا حسب اللون</a> واجهة برمجة قابلة للوصول من خارج النظام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفّح الويب.

### استخدام مكتبات Aspose.Cells Cloud SDK

استخدام مكتبة SDK هو أسرع طريقة للتطوير، حيث تُجرّدك من التفاصيل منخفضة المستوى، وتتيح لك جمع الحسابات حسب لون الخلايا باستخدام جزء صغير من الكود فقط.  
يرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر الأمثلة التالية كيفية إجراء مكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**ملاحظات:**

- عند العمل مع ملفات جدول عمل محمية، تأكد من تضمين المتغير الاختياري `Password` في استعلام الطلب؛ وإلا فستفشل الطلب مع خطأ 401.
- الحد الأقصى لحجم طلب الملف `Spreadsheet` هو 100 ميغابايت. وإذا احتجت إلى معالجة ملفات أكبر، فكر في رفع جدول العمل إلى مستودع Aspose Cloud أولًا ثم الإشارة إليه عبر المتغير `Path` (وهو ما لا يظهر هنا).
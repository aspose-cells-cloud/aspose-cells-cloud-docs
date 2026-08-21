---
title: "الحصول على النطاقات المسماة في مصنف إكسل"
second_title: "وثيقة"
linktype: "اسم"
type: docs
url: /ar/ranges/get/name/
aliases: [  /ar/get-named-ranges-inside-the-workbook/ ]
keywords: "النطاقات المسماة، إكسل، Aspose.Cells، واجهة برمجة التطبيقات السحابية، أوراق العمل"
description: "استرجاع النطاقات المسماة من مصنف إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن تفاصيل الطلب وأوامر cURL النموذجية وأمثلة لعدة لغات برمجة."
ArticleTitle: "الحصول على النطاقات المسماة في مصنف إكسل – واجهة برمجة التطبيقات السحابية Aspose.Cells"
weight: 10
---

تُعيد هذه الواجهة البرمجية (REST API) معلومات حول النطاقات المسماة المُعرَّفة داخل أوراق العمل.

**الخلفية** – يُعد *النطاق المسماة* مُعرِّفًا يُعرِّفه المستخدم ويُشير إلى خلية محددة أو مجموعة محددة من الخلايا في ورقة عمل. وتساعد النطاقات المسماة في تبسيط إنشاء الصيغ، وتحسين قابلية القراءة، وتمكين الوصول البرمجي إلى المناطق المستخدمة بشكل متكرر في المصنف.

**المتطلبات الأساسية** – يتطلب الوصول إلى واجهة برمجة تطبيقات Aspose.Cells Cloud رمز وصول JWT صالح. احصل على الرمز المميز من خلال المصادقة باستخدام مُعرِّف العميل وسر العميل الخاصين بك على خدمة OAuth 2.0. وقم بتضمين الرمز المميز في رأس الطلب `Authorization: Bearer <jwt token>` في كل طلب.

## واجهة GetNamedRanges البرمجية

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع     | الوصف                                  |
| -------------- | ------ | ------------ | -------------------------------------------- |
| name           | string | Path         | اسم مستند إكسل.              |
| folder         | string | Query string | المجلد الذي يحتوي على المستند.       |
| storageName    | string | Query string | اسم وحدة التخزين التي يوجد فيها المستند. |

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح                          | تم تطبيق الفلتر بنجاح؛ ويتضمن الاستجابة تفاصيل العملية. |
| 400  | طلب غير صالح                 | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصادَق                 | رمز JWT غير صالح أو مفقود. |
| 413  | حجم البيانات أكبر من المسموح به           | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم       | خطأ غير متوقع في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) واجهة برمجة تطبيقات عامة قابلة للوصول تتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية استرجاع النطاقات المسماة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**نموذج الاستجابة**

| الحقل          | النوع    | الوصف                                          |
|----------------|---------|------------------------------------------------------|
| `ColumnCount`  | integer | عدد الأعمدة في النطاق.                      |
| `ColumnWidth`  | number  | عرض كل عمود (بالنقاط).                    |
| `FirstColumn`  | integer | فهرس العمود الأول (مبني على الصفر) في النطاق.   |
| `FirstRow`     | integer | فهرس الصف الأول (مبني على الصفر) في النطاق.      |
| `Name`         | string  | الاسم المُعرَّف من قِبل المستخدم للنطاق.                  |
| `RefersTo`     | string  | صيغة تُعرِّف مرجع الخلية (مثل `=Sheet1!$B$10:$H$10`). |
| `RowCount`     | integer | عدد الصفوف في النطاق.                         |
| `RowHeight`    | number  | ارتفاع كل صف (بالنقاط).                      |
| `Worksheet`    | string  | اسم ورقة العمل التي يحتوي عليها النطاق.       |

## مجموعة أدوات SDK السحابية

يُعد استخدام حزمة SDK أسرع طريقة لدمج هذه الوظيفة. وتتولى حزم SDK تفاصيل المستوى المنخفض، مما يسمح لك بالتركيز على منطق أعمالك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم SDK لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام حزم SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}
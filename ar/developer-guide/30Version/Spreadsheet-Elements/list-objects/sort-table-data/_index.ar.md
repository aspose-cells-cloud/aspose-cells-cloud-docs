---
title: "فرز بيانات كائن القائمة في ورقة عمل Excel"
second_title: "مستند"
linktitle: "فرز"
type: docs
url: /ar/list-objects/sort-data/
aliases: [  /ar/get-a-list-object-or-table-inside-the-worksheet/ , /ar/tables/sort-data/ ]
keywords: "Aspose.Cells Cloud، Excel، ListObject، فرز البيانات، واجهة برمجة التطبيقات REST، ورقة العمل"
description: "تعلم كيفية فرز بيانات كائن القائمة (الجدول) في ورقة عمل Excel باستخدام واجهة برمجة التطبيقات REST لـ Aspose.Cells Cloud (النسخة 3.0). يتضمن العنوان، المعلمات، مثال لطلب cURL، وأمثلة لواجهات برمجة التطبيقات (SDK)."
weight: 40
ArticleTitle: "فرز بيانات كائن القائمة في ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

**المتطلبات المسبقة**  
لاستدعاء هذه الواجهة، يجب أن تمتلك رمز وصول JWT ساري المفعول من Aspose Cloud، كما يجب رفع ملف المصنف إلى مساحة التخزين الخاصة بـ Aspose Cloud. تأكد من تضمين الرأس `Authorization: Bearer <jwt token>` في كل طلب.

تقوم هذه الواجهة REST بفرز بيانات الجدول داخل ورقة عمل Excel.  
لاستخدام هذه العملية، قم بتوفير اسم المصنف، واسم ورقة العمل، وفهرس كائن القائمة المستهدف، إلى جانب جسم JSON يحتوي على كائن `dataSorter` يحدد معايير الفرز.

## واجهة PostWorksheetListObjectSortTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### **معلمات الطلب**

| اسم المعلمة     | النوع   | المسار / سلسلة الاستعلام / جسم HTTP | الوصف                                                                                             |
|------------------|---------|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| name             | نص (string) | path                           | اسم ملف Excel المخزن في مساحة التخزين الخاصة بـ Aspose Cloud.                                      |
| sheetName        | نص (string) | path                           | اسم ورقة العمل التي تحتوي على كائن القائمة (ListObject).                                           |
| listObjectIndex  | عدد صحيح (integer) | path                   | الفهرس المبتدئ من الصفر لكائن القائمة (الجدول) داخل ورقة العمل.                                   |
| dataSorter       | كائن (object) | body                        | كائن JSON يحدّد خيارات الفرز (مثل `CaseSensitive`، `HasHeaders`، `KeyList`، `SortLeftToRight`). |
| folder           | نص (string) | query                         | مسار المجلد داخل التخزين حيث يقع ملف Excel.                                                        |
| storageName      | نص (string) | query                         | اسم مساحة التخزين الخاصة بـ Aspose Cloud.                                                          |

**ملاحظات**  
يجب أن يكون جسم الطلب كائن JSON صالحًا يطابق مخطط `dataSorter`. تأكد من وجود المصنف وورقة العمل وكائن القائمة قبل تنفيذ عملية الفرز.

يعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) واجهة برمجة قابلة للوصول علنًا، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
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

**رموز حالة HTTP**

| رمز الحالة | الوصف                                          |
|-------------|------------------------------------------------|
| 200         | نجاح – تم إكمال عملية الفرز بنجاح.            |
| 400         | طلب غير صالح – معلمات غير صحيحة.              |
| 401         | غير مُصرّح – فشلت عملية المصادقة.              |
| 404         | غير موجود – لم يتم العثور على المصنف أو ورقة العمل أو كائن القائمة. |
| 500         | خطأ داخلي في الخادم – مشكلة من جانب الخادم.   |

**معلمات الاستجابة**

| المعلمة | النوع   | الوصف                                      |
|---------|---------|----------------------------------------------|
| Code    | عدد صحيح | رمز حالة HTTP الذي تعيده واجهة برمجة التطبيقات. |
| Status  | نص (string) | وصف نصي لنتيجة العملية (مثل "OK").         |

{{< /tab >}}

{{< /tabs >}}

## عائلة واجهات برمجة التطبيقات (SDK) السحابية

استخدام واجهات برمجة التطبيقات (SDKs) هو أفضل طريقة لتسريع عملية التطوير، إذ تتعامل SDKs مع التفاصيل منخفضة المستوى، وتتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بواجهات برمجة التطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[عودة إلى نظرة عامة sobre ListObjects](/ar/list-objects/)
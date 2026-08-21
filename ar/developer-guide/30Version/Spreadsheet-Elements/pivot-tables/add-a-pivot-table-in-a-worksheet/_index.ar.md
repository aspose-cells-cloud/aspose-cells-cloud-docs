---
title: "إضافة جدول محوري في ورقة عمل Excel"
second_title: "مستند"
linktype: إضافة
type: docs
url: /ar/pivot-tables/add/
aliases: [  /ar/add-a-pivot-table-in-a-worksheet/ ]
keywords: "إضافة جدول محوري، ورقة عمل Excel، Aspose.Cells Cloud، REST API، SDK، جدول محوري Excel"
description: "استخدم REST API الخاص بـ Aspose.Cells Cloud لإضافة جدول محوري في ورقة عمل Excel. متاح عبر SDKs لكل من C#، Java، PHP، Python، Node.js، Android، Swift، Perl، Go."
weight: 30
ArticleTitle: "كيفية إضافة جدول محوري في ورقة عمل Excel باستخدام Aspose.Cells Cloud"
---

تضيف هذه الواجهة البرمجية (REST API) جدولًا محوريًا في ورقة عمل.

**المتطلبات المسبقة:**  
- حساب Aspose.Cells Cloud مع رمز وصول JWT صالح.  
- يجب تخزين ملف العمل المستهدف في موقع تخزين مدعوم (التخزين الافتراضي أو تخزين مُحدّد من قِبل المستخدم).  
- يجب أن توجد الورقة المحددة عبر `sheetName` في ملف العمل.  

## PutWorksheetPivotTable API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **الأمان والمصادقة**

تُطبّق واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud سياسة أمان صارمة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### **معاملات الطلب**

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| name | string | path | اسم ملف Excel. |
| sheetName | string | path | اسم ورقة العمل التي سيتم إنشاء الجدول المحوري فيها. |
| request | object | body | كائن `CreatePivotTableRequest` DTO الذي يحتوي على تعريف الجدول المحوري. |
| folder | string | query | المجلد الذي يحتوي على المستند. |
| storageName | string | query | اسم مكان التخزين الذي يوجد فيه المستند. |
| sourceData | string | query | النطاق الذي يزوّد البيانات المصدرية لذاكرة التخزين المؤقتة الجديدة للجدول المحوري (مثل `A5:E10`). |
| destCellName | string | query | عنوان الخلية العلوية اليسرى للنطاق الوجهة لتقرير الجدول المحوري. |
| tableName | string | query | الاسم المُسنَد إلى الجدول المحوري الجديد. |
| useSameSource | boolean | query | عندما تكون القيمة `true`، فإن الجدول المحوري الجديد يُعيد استخدام مصدر بيانات موجود، مما يوفّر الذاكرة إذا كان هناك جدول محوري آخر قد استخدم هذا المصدر مسبقًا. |

يمكنك الاطّلاع على [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) التي تُعرّف واجهة برمجة تطبيقات عامة قابلة للاستعمال، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

**ملاحظة أمنية:** تأكد دائمًا من استخدام `https://` عند استدعاء الواجهة البرمجية، واحتفظ بسرية رمز JWT الخاص بك؛ إذ أن إرساله عبر بروتوكول HTTP غير المشفر يعرّضه للاختطاف.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح (OK) | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُصرّح (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK التعامل مع التفاصيل من المستوى المنخفض، مما يمكّنك من التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs المختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

لمزيد من العمليات، راجع صفحات الواجهة البرمجية ذات الصلة: **[الحصول على جدول محوري](https://docs.aspose.cloud/cells/pivot-tables/get/)**، **[حذف جدول محوري](https://docs.aspose.cloud/cells/pivot-tables/delete/)**، و **[تحديث جدول محوري](https://docs.aspose.cloud/cells/pivot-tables/update/)**.
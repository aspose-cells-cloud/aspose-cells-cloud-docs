---
title: "إضافة ورقة عمل Excel"
ArticleTitle: "إضافة ورقة عمل Excel - دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "إضافة"
type: docs
url: /ar/worksheets/add/
aliases: [  /ar/add-a-new-excel-worksheet/ ]
keywords: "إضافة ورقة عمل Excel، Aspose.Cells Cloud، واجهة برمجة تطبيقات REST، إضافة ورقة عمل عبر PUT، ملف Excel، طلب واجهة برمجة التطبيقات"
description: "دليل خطوة بخطوة لإضافة ورقة عمل جديدة إلى ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST، ويتضمن تفاصيل الطلب، ومثال باستخدام cURL، وأجزاء من كود SDK لعدة لغات برمجة."
weight: 20
---

تُضيف هذه الواجهة البرمجية ورقة عمل جديدة إلى ملف عمل موجود.

**المتطلبات الأساسية**: لاستدعاء هذه النقطة النهائية، يجب أن يكون لديك رمز مصادقة صالح لـ Aspose Cloud، ويجب أن يكون ملف العمل المستهدف قد تم رفعه إلى مساحة التخزين في Aspose Cloud، ويجب أن تعرف اسم مساحة التخزين (إن كنت تستخدم مساحة تخزين مخصصة).

## واجهة برمجة التطبيقات REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **مُعطَلات الطلب**

| اسم المُعطَل | النوع    | الموقع | الوصف                                              |
|--------------|----------|--------|-----------------------------------------------------|
| name         | string   | path   | اسم ملف ملف العمل.                                 |
| sheetName    | string   | path   | اسم ورقة العمل الجديدة المراد إنشاؤها.              |
| position     | integer  | query  | الموقع الصِّفرِي المُرَتَّب الذي تُدرج فيه الورقة.  |
| sheettype    | string   | query  | نوع الورقة الجديدة (مثل **Chart**، **Dialog**).    |
| folder       | string   | query  | المجلد الذي يحتوي على ملف العمل.                   |
| storageName  | string   | query  | اسم مساحة التخزين في Aspose Cloud.                 |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet) واجهة برمجة تطبيقات قابلة للوصول العام، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء استدعاء لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
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

**رموز حالات الاستجابة الممكنة**

| رمز الحالة | الوصف                                               |
|------------|------------------------------------------------------|
| 200        | تمت إضافة ورقة العمل بنجاح.                         |
| 400        | طلب غير صالح – مُعطَلات غير صحيحة.                 |
| 401        | غير مخوّل – رمز المصادقة مفقود أو غير صالح.        |
| 404        | غير موجود – ملف العمل أو المجلد غير موجود.         |
| 500        | خطأ داخلي في الخادم – حالة غير متوقعة.             |

## عائلة SDK السحابية

استخدام SDK هو أسرع طريقة لتطوير التطبيقات. فالمكتبة (SDK) تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
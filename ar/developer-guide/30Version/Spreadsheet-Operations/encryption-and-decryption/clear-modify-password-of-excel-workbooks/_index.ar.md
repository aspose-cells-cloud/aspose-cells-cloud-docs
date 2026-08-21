---
title: "إزالة حماية الكتابة (كلمة المرور) من ملف مصنف إكسل"
second_title: "مستند"
linktitle: "مسح كلمة مرور ملفات إكسل"
type: docs
url: /clear-excel-files-password/
aliases:
  [
    /clear-modify-password-of-excel-workbooks/,
    /workbook/clear-modify-password/،/workbook/password/clear/,
  ]
keywords: "Aspose.Cells، إكسل، إزالة كلمة المرور، حماية الكتابة، واجهة برمجة تطبيقات REST، أمثلة SDK"
description: "تعلم كيفية حذف حماية الكتابة (كلمة المرور) من ملف مصنف إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يتضمن مثالًا باستخدام cURL، خطوات المصادقة، وأكواد الأمثلة من SDKs."
weight: 110
ArticleTitle: "إزالة حماية الكتابة (كلمة المرور) من ملف مصنف إكسل"
---

تقوم هذه واجهة برمجة تطبيقات REST بإزالة **حماية الكتابة (كلمة المرور)** من ملف مصنف إكسل، مما يتيح لك **إزالة حماية كلمة المرور** من ملفات إكسل برمجيًا.

**المتطلبات المسبقة:** احصل على رمز JWT صالح، وتأكد من أن المصنف مخزن في موقع دعم للتخزين، واستخدم إصدار API v3.0.

لإضافة الحماية، راجع دليل [حماية إكسل](/cells/protect/).

## DeleteDocumentUnprotectFromChanges API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **متغيرات الطلب**

| اسم المتغير | النوع | الموقع | الوصف |
| ------------ | ------ | -------- | ------------------------------------------------- |
| `name` | string | path | اسم ملف مصنف إكسل. |
| `folder` | string | query | المجلد الذي يحتوي على المصنف (اختياري). |
| `storageName` | string | query | اسم خدمة التخزين (اختياري). |

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الكود | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معطيات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو ناقص. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

## كيفية استخدام DeleteDocumentUnprotectFromChanges API باستخدام SDKs

### مواصفات DeleteDocumentUnprotectFromChanges API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) واجهة برمجة تطبيقات عامة قابلة للاستخدام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة تطبيقات REST باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
  -X DELETE \
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


### استخدام Aspose.Cells Cloud SDKs

استخدام SDKs هو أفضل طريقة لتسريع التطوير. تُدير SDKs التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}
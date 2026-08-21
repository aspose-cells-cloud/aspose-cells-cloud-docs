---
title: "إزالة جميع خصائص المستند"
second_title: "المستند"
linktype: "مسح"
type: docs
url: /document-properties/clear/
aliases: [/remove-all-document-properties/]
keywords: "Aspose.Cells, حذف خصائص المستند, مسح خصائص Excel, واجهة برمجة تطبيقات REST, حزمة تطوير برامج السحابة, جدول بيانات, مرجع واجهة برمجة التطبيقات"
description: "دليل خطوة بخطوة لإزالة جميع الخصائص المخصصة والمدمجة من ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST."
weight: 58
---

تقوم هذه الواجهة البرمجية لـ REST بحذف جميع الخصائص المخصصة للمستند ومسح الخصائص المدمجة.

## واجهة برمجة تطبيقات REST

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### معلمات الطلب

| اسم المعلمة | النوع   | الموقع | الوصف                |
| ------------ | ------ | -------- | -------------------- |
| name         | string | path     | اسم المستند.          |
| folder       | string | query    | مجلد المستند.         |
| storageName  | string | query    | اسم التخزين.          |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperties) واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
  -X DELETE \
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

{{< /tab >}}

{{< /tabs >}}

## عائلة حزم تطوير البرمجيات السحابية

استخدام حزمة تطوير البرمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير. تتعامل حزمة تطوير البرمجيات مع التفاصيل منخفضة المستوى وتركّز أنت على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام حزم تطوير برامج مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperties.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperties.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperties.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperties.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperties.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperties.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperties.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperties.go" >}}
{{< /tab >}}

{{< /tabs >}}
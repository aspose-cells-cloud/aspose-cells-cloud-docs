---
title: "نسخ المحتويات والتنسيقات من ورقة عمل أخرى."
second_title: "Document"
linktitle: "نسخ"
type: docs
url: /worksheets/copy/
aliases: [/copy-excel-worksheet/]
keywords: "واجهة برمجة تطبيقات Aspose Cells لنسخ ورقة العمل، REST API لنسخ ورقة Excel، SDK Aspose Cloud لنسخ، نسخ ورقة العمل في جداول البيانات"
description: "تعرّف على كيفية نسخ ورقة عمل وتنسيقاتها إلى ورقة جديدة باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن نقطة النهاية، المُعاملات، أمثلة cURL وSDKs لـ C#، Java، Python، والمزيد."
weight: 20
---

تقوم هذه الواجهة البرمجية REST بنسخ ورقة عمل وتنسيقاتها إلى ورقة جديدة داخل نفس ملف العمل.

## واجهة برمجة تطبيقات REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

تُسرد المُعاملات المطلوبة أدناه:

| اسم المُعامل      | النوع   | الموقع   | الوصف                                                                 |
| ---------------- | ------ | -------- | --------------------------------------------------------------------- |
| `name`           | string | path     | اسم ملف ملف العمل.                                                   |
| `sheetName`      | string | path     | اسم ورقة العمل الوجهة (الورقة الجديدة).                              |
| `sourceSheet`    | string | query    | اسم ورقة العمل المراد نسخها.                                         |
| `options`        | object | body     | كائن JSON يحتوي على خيارات النسخ (مثل عرض الأعمدة، الصيغ).           |
| `sourceWorkbook` | string | query    | اسم ملف العمل المصدري إذا اختلف عن ملف العمل الحالي.                |
| `sourceFolder`   | string | query    | مسار المجلد الذي يُخزَّن فيه ملف العمل المصدري.                      |
| `folder`         | string | query    | مسار المجلد الذي سيُحفظ فيه ملف العمل الهدف.                         |
| `storageName`    | string | query    | اسم خدمة التخزين المراد استخدامها.                                   |

### أمثلة على الطلب والاستجابة

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) واجهة برمجة قابلة للوصول بشكل عام، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
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

### معالجة الأخطاء

تُعيد الواجهة رموز الحالة القياسية لبروتوكول HTTP مع جسم خطأ بصيغة JSON. تشمل الاستجابات الشائعة ما يلي:

| رمز HTTP | الوصف                                                     | مثال على جسم الخطأ بصيغة JSON                                 |
|---------|-----------------------------------------------------------|--------------------------------------------------------------|
| 400     | طلب غير صالح – مُعاملات مفقودة أو غير صالحة.             | `{ "Code": 400, "Message": "Invalid request parameters." }`   |
| 401     | غير مصرّح – رمز مفقود أو غير صالح.                        | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404     | غير موجود – ملف العمل أو ورقة العمل أو المجلد غير موجود. | `{ "Code": 404, "Message": "Resource not found." }`           |
| 500     | خطأ داخلي في الخادم – حالة غير متوقعة.                   | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## عائلة SDK للسحابة

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. فالـ SDK يتعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}

---
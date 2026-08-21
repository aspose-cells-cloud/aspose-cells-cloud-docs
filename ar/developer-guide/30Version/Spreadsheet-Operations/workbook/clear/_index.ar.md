---
title: "مسح الكائنات في ملف Excel"
second_title: "Document"
linktitle: "مسح"
type: docs
url: /ar/clear/
aliases: [  /ar/clearobjects/ ]
keywords: "Aspose.Cells, Excel, مسح الكائنات, REST API, Cloud SDK, إزالة التعليقات, حذف المخططات"
description: "استخدم Aspose.Cells Cloud REST API لحذف التعليقات والمخططات والأشكال والكائنات الأخرى من ملف Excel. يدعم مجموعة واسعة من SDKs ويعيد الملف النظيف بصيغة Base64."
weight: 39
---

تقوم هذه الواجهة البرمجية REST بمسح الكائنات في ملف Excel.

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/clearobjects
```

### معاملات الطلب

| المعامل       | النوع   | الموقع        | الإلزام | القيمة الافتراضية | القيم المسموح بها                                                                                                                                                                                     | الوصف                                      |
| ------------- | ------- | ------------- | ------ | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| file          | ملف    | form‑data     | نعم    | —                 | —                                                                                                                                                                                                     | ملف Excel المراد تحميله                      |
| objecttype    | نص    | query         | لا      | —                 | `duplicaterows`, `blankcolumns`, `blankrows`, `formula`, `content`, `style`, `chart`, `comment`, `picture`, `shape`, `listobject`, `hyperlink`, `oleobject`, `pivottable`, `validation`, `background` | أنواع الكائنات المراد مسحها (مفصولة بفواصل) |

يعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostClearObjects) واجهة برمجة تطبيقات عامة قابلة للوصول، وتمكنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/clearobjects?objecttype=comment" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فالـ SDK يُجرّدك من التفاصيل التقنية منخفضة المستوى ويساعدك على التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهات برمجة التطبيقات باستخدام مختلف SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearObjects.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearObjects.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearObjects.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearObjects.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearObjects.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearObjects.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearObjects.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearObjects.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
title: "الحصول على جميع الصور في ورقة عمل Excel"
second_title: "مستند"
linktitle: "الحصول على الكل"
type: docs
url: /ar/pictures/get-all/
aliases: [  /ar/get-picture-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud، ورقة عمل Excel، واجهة برمجة تطبيقات الصور، الحصول على جميع الصور، واجهة برمجة التطبيقات عبر الويب، وحدات التطوير البرمجي"
description: "استرجاع جميع كائنات الصور من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud عبر الويب."
ArticleTitle: "الحصول على جميع الصور في ورقة عمل Excel - واجهة برمجة تطبيقات Aspose.Cells Cloud"
weight: 10
---

تسترجع هذه واجهة برمجة التطبيقات REST جميع معلومات الصور من ورقة عمل Excel.

**المتطلبات الأساسية**  
قبل استدعاء هذه النقطة النهائية، تأكد من وجود ما يلي:

- رمز وصول JWT صالح لـ Aspose Cloud.  
- تحميل ملف Excel المستهدف إلى مساحة التخزين المحددة.  
- اسم مساحة التخزين الصحيح (في حال استخدام مساحة تخزين مخصصة).  
- اسم ورقة العمل التي تحتوي على الصور.

## واجهة برمجة التطبيقات GetWorksheetPictures

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**ملاحظة:** استخدم بروتوكول HTTPS (TLS 1.2 أو إصدار أحدث) عند استدعاء واجهة برمجة التطبيقات، وقم بتضمين رمز JWT صالح في رأس `Authorization`.

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### **معلَمات الطلب**

| اسم المعلَمة | النوع | الموقع | الوصف |
| ------------ | ------ | -------- | ---------------------------------------------- |
| name | string | path | اسم ملف Excel. |
| sheetName | string | path | اسم ورقة العمل التي تحتوي على الصور. |
| folder | string | query | مسار المجلد الذي يخزن فيه الملف. |
| storageName | string | query | اسم خدمة مساحة التخزين. |

### استجابات الأخطاء

| رمز HTTP | الوصف |
| --------- | ------------------------------------------------------------------------------ |
| 401 | غير مصرح به – نقص أو عدم صلاحية الرمز. |
| 404 | غير موجود – الملف أو ورقة العمل أو فهرس قطع الصف المحددة غير موجودة. |
| 400 | طلب خاطئ – بنية الطلب غير صحيحة أو المعلمات غير صالحة. |
| 500 | خطأ داخلي في الخادم – واجهت الخدمة حالة غير متوقعة. |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) واجهة برمجة تطبيقات متاحة علنًا، ويتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**استجابة ناجحة** – تُعيّد المكالمة الناجحة رمز HTTP 200 مع حُملة JSON تحتوي على كائن `Pictures` يسرد رابط المورد لكل صورة.

## عائلة وحدات تطوير البرمجي السحابية

استخدام وحدات التطوير البرمجي (SDK) هو أفضل طريقة لتسريع عملية التطوير. تتعامل وحدات التطوير البرمجي مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بوحدات تطوير البرمجي الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات Aspose.Cells عبر الويب باستخدام مختلف وحدات التطوير البرمجي:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

يمكنك تنزيل وحدات التطوير البرمجي مباشرةً من مديري الحزم الخاصة بها (مثل NuGet لـ .NET، وMaven Central لـ Java، وComposer لـ PHP، وnpm لـ Node.js، وPyPI لـ Python، وCPAN لـ Perl، وGo modules لـ Go).  

*انظر أيضًا:* إضافة صورة، حذف صورة، تحديث خصائص الصورة.
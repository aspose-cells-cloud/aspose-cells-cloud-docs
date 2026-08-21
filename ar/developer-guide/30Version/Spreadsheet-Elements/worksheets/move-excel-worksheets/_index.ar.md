---
title: "نقل ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
second_title: "مستند"
linktype: "move"
type: docs
url: /ar/worksheets/move/
aliases: [  /ar/move-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud، نقل ورقة عمل، Excel، واجهة برمجة تطبيقات REST، SDK، C#، Java، Python، Node.js، PHP، Ruby، Go، Android، Swift، Perl، الإصدار 3.0"
description: "تعرّف على كيفية نقل ورقة عمل Excel إلى موقع جديد باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0). يتضمن عنوان النهاية (Endpoint)، المُعطَلات المطلوبة، مثال cURL، ورموز SDK بلغات C# وJava وPython وغيرها."
weight: 20
ArticleTitle: "كيفية نقل ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud الإصدار 3.0"
---

تقوم هذه الواجهة البرمجية لـ REST بنقل ورقة عمل داخل ملف Excel (Book).

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### مُعطَلات الطلب (Request Parameters)

| اسم المُعطَل         | النوع   | الموقع | الوصف                                                                                                      |
|----------------------|---------|--------|-------------------------------------------------------------------------------------------------------------|
| name                 | string  | path   | اسم ملف Excel.                                                                                              |
| sheetName            | string  | path   | اسم ورقة العمل المراد نقلها.                                                                                |
| moving               | object  | body   | كائن JSON يحدّد ورقة العمل الوجهة (`DestinationWorksheet`) والموقع النسبي (`Position`).                     |
| folder               | string  | query  | مسار المجلد الذي يُخزَّن فيه ملف Workbook.                                                                 |
| storageName          | string  | query  | اسم خدمة التخزين.                                                                                           |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر `cURL` لاستدعاء خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية نقل ورقة عمل باستخدام طلب واحد.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**رموز حالة HTTP**

| الرمز | المعنى                   | الوصف                                                                 |
|-------|---------------------------|------------------------------------------------------------------------|
| 200   | OK (تم بنجاح)            | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.            |
| 400   | Bad Request (طلب خاطئ)   | مُعطَلات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).                |
| 401   | Unauthorized (غير مصرّح)  | رمز JWT غير صالح أو مفقود.                                            |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح.                          |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | حدث خطأ غير متوقع في الخادم.                                   |

**نموذج حمولة خطأ**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "المُعطَل المطلوب 'moving' مفقود."
}
```

{{< /tab >}}

{{< /tabs >}}

## مجموعة أدوات SDK للحاسوب السحابي

يُعد استخدام SDK الطريقة الأفضل لتسريع عملية التطوير. فتتولى SDK التعامل مع التفاصيل منخفضة المستوى، ما يمكّنك من التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}
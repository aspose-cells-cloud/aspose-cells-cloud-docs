---
title: "نسخ نطاق في ورقة عمل مع خيارات اللصق"
second_title: "مستند"
linktitle: "نسخ"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Aspose.Cells Cloud، واجهة برمجة تطبيقات REST، Excel، نسخ نطاق، ورقة عمل، خيارات اللصق"
description: "استخدم واجهة برمجة تطبيقات Aspose.Cells Cloud REST لنسخ نطاق داخل ورقة عمل Excel مع دعم كامل لخيارات اللصق. يشمل أمثلة SDK لعدة لغات برمجة."
weight: 20
ArticleTitle: "نسخ نطاق في ورقة عمل مع خيارات اللصق – Aspose.Cells Cloud API"
---

تقوم هذه واجهة برمجة تطبيقات REST بنسخ نطاق في ورقة عمل من ملف عمل Excel. وللحصول على العمليات ذات الصلة، راجع وثائق **الحصول على النطاق** و**تحديث النطاق**.

**المتطلبات المسبقة:** لاستخدام هذه النقطة النهائية، يجب أن يكون لديك رمز OAuth 2.0 / JWT صالح، وأن تضمن توافق إصدار واجهة برمجة التطبيقات مع عنوان URL للطلب.

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **مُعاملات الطلب**

| اسم المُعامل | النوع | الموقع | الوصف |
| ------------ | ------ | -------- | ---------------------------------------------------------------------------- |
| name | string | path | اسم ملف العمل. |
| sheetName | string | path | اسم ورقة العمل. |
| rangeOperate | string | body | العملية المراد تنفيذها: `copydata`، `copystyle`، `copyto`، أو `copyvalue`. |
| folder | string | query | المجلد الذي يحتوي على ملف العمل. |
| storageName | string | query | اسم خدمة التخزين. |

**ملاحظات:** يحدد الحقل `rangeOperate` ما سيتم نسخه. استخدم `copydata` لنسخ قيم الخلايا فقط، و`copystyle` للتنسيق، و`copyto` لكل من البيانات والتنسيق، و`copyvalue` لنسخ القيم دون الصيغ. تدعم واجهة برمجة التطبيقات النطاقات التي تصل إلى مليون خلية؛ وقد تؤدي النطاقات الأكبر إلى حدوث انتهاء للمهلة الزمنية.

يعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopy) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

تعيد الاستجابة الناجحة حالة `200 OK`. وفي حالة حدوث خطأ، قد تُعيد واجهة برمجة التطبيقات أحمال مثل:

```json
{
  "Code": 400,
  "Message": "Bad Request – مُعلمات غير صالحة."
}
```

أو

```json
{
  "Code": 401,
  "Message": "Unauthorized – رمز المصادقة مفقود أو غير صالح."
}
```

تتضمن كائنات الخطأ هذه رمز حالة HTTP ورسالة وصفية تساعد في تشخيص المشكلات.

{{< /tab >}}

{{< /tabs >}}

يمكنك تنزيل ملف عمل تجريبي لاختبار عملية النسخ من [هنا](https://example.com/sample.xlsx).

## عائلة SDK السحابية

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. فتتولى حزم SDK تفاصيل المستوى المنخفض، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام حزم SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}
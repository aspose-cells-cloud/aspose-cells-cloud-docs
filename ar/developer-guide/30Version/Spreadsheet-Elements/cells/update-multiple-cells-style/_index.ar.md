---
title: "تحديث أسلوب خلايا متعددة – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
type: docs
url: /update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "تحديث أسلوب خلايا متعددة", "واجهة برمجة تطبيقات تنسيق خلية إكسل", "حزمة تطوير برمجيات السحابة", "واجهة برمجة تطبيقات REST", "مثال باستخدام cURL", "طلب JSON", "مصادقة JWT"]
description: "تعرّف على كيفية تحديث أسلوب مجموعة من الخلايا في ملف عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API الإصدار 3.0. يشمل الرابط، طريقة HTTP، المُعلَمات، أمثلة لـ cURL وحزم التطوير (SDKs)، المصادقة، معالجة الأخطاء، ومعلومات الإصدار."
ArticleTitle: "تحديث أسلوب خلايا متعددة – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
---

## واجهة برمجة تطبيقات REST

تقوم هذه واجهة برمجة تطبيقات REST بضبط **النمط** لمجموعة من الخلايا في ملف عمل إكسل.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## الأمان والمصادقة

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى [مصادقة باستخدام رمز مميز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### مُعلَمات الطلب

| اسم المُعلَمة | النوع   | الموقع | الوصف |
|----------------|--------|----------|-------------|
| **name**       | نص (string) | المسار (path) | اسم ملف العمل. |
| **sheetName**  | نص (string) | المسار (path) | اسم ورقة العمل. |
| **range**      | نص (string) | الاستعلام (query) | نطاق الخلايا (مثل `A1:A10`). |
| **style**      | كائن (object) | الجسم (body) | كائن JSON يُعرّف النمط المراد تطبيقه. |
| **folder**     | نص (string) | الاستعلام (query) | المجلد الذي يحتوي على ملف العمل. |
| **storageName**| نص (string) | الاستعلام (query) | اسم وحدة التخزين. |

#### كائن النمط (Style object)
يمثّل كائن JSON `style` تنسيق الخلايا، وقد يحتوي على أيٍّ من الخصائص الاختيارية التالية:

- **Font** – إعدادات الخط (`Name`، `Size`، `IsBold`، `IsItalic`، `Color`، إلخ).  
- **BackgroundColor** – لون الخلفية بصيغة ARGB.  
- **ForegroundColor** – لون المقدّمة بصيغة ARGB.  
- **Name**، **CultureCustom**، **Custom** – بيانات تعريف إضافية للنمط.

## **الاستجابة**

ترجع كائن `CellCloudResponse`.

- **نظرة عامة على حقول الاستجابة**

| الحقل           | النوع    | الوصف                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | نص (string)  |                    |
| `Code`           | عدد صحيح (integer) | 200، 400، 401، 500، ...                                 |

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                          | تم تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | مُعلَمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصادَق (Unauthorized)                | رمز مُتَوَسِّط JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large)           | حجم الملف المرفّع يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة برمجة تطبيقات PostUpdateWorksheetRangeStyle مع حزم تطوير البرمجيات (SDKs)

### مواصفات واجهة برمجة تطبيقات PostUpdateWorksheetRangeStyle

توفّر [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) المخطط الكامل.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells السحابية. يُظهر المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
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

{{< /tab >}}

{{< /tabs >}}


### استخدام حزم تطوير البرمجيات (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام حزمة تطوير البرمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير، إذ تقوم SDK بمعالجة التفاصيل الدقيقة منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام حزم تطوير البرمجيات المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}
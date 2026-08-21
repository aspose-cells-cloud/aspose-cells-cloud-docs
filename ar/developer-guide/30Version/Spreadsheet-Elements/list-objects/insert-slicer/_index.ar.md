---
title: "إضافة مُفلّت (Slicer) إلى كائن قائمة في Excel – واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktitle: "إضافة مُفلّت"
type: docs
keywords: "Aspose.Cells, مُفلّت Excel, كائن قائمة, واجهة REST, حزمة SDK سحابية"
description: "تعرّف على كيفية إضافة مُفلّت إلى كائن قائمة في Excel باستخدام واجهة Aspose.Cells Cloud REST API (النسخة 3.0). يشمل الطلب نقطة النهاية والمُعلَمات ومصادقة المصادقة، ومثال على طلب cURL واستجابة JSON."
weight: 20
ArticleTitle: "إضافة مُفلّت (Slicer) إلى كائن قائمة في Excel – واجهة Aspose.Cells Cloud API"
---

تُضيف هذه الواجهة البرمجية REST مُفلّت (Slicer) لكائن قائمة في ورقة عمل Excel.

## واجهة REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### مُعلَمات الطلب

| اسم المُعلَمة        | النوع    | الموقع | الوصف                                                                 |
|----------------------|----------|--------|------------------------------------------------------------------------|
| name                 | نص (String) | المسار | اسم ملف Excel.                                                        |
| sheetName            | نص (String) | المسار | اسم ورقة العمل التي تحتوي على كائن القائمة.                           |
| listObjectIndex      | عدد صحيح (Integer) | المسار | الفهرس الصفري لكائن القائمة الذي سيتم إضافة المُفلّت إليه.            |
| columnIndex          | عدد صحيح (Integer) | الاستعلام | الفهرس الصفري للعمود الذي يستند إليه المُفلّت.                         |
| destCellName         | نص (String) | الاستعلام | مرجع الخلية (مثل **A1**) حيث سيتم وضع المُفلّت.                        |
| folder               | نص (String) | الاستعلام | المجلد في التخزين الذي يحتوي على ملف Excel.                           |
| storageName          | نص (String) | الاستعلام | اسم خدمة تخزين Aspose Cloud.                                           |

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء الواجهة:

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **ملاحظة:** يتطلب الطلب رمز bearer JWT صالحًا يُحصل عليه من خدمة مصادقة Aspose Cloud. لا تتطلب هذه النقطة النهائية جسم طلب؛ أرسل كائن JSON فارغ `{}` إذا كان مكتبة العميل الخاصة بك تفرض وجود حمولة (payload).

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **رأس الاستجابة:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                                 |
|-------|-----------------------------|------------------------------------------------------------------------|
| 200   | نجاح (OK)                   | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.          |
| 400   | طلب غير صالح (Bad Request) | مُعلَمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم).                 |
| 401   | غير مصرّح به (Unauthorized) | رمز JWT غير صالح أو مفقود.                                            |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.                             |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                              |

### معالجة الأخطاء

عند حدوث خطأ، تُعيد الواجهة كائن JSON يحتوي على حقل `ErrorMessage` يصف المشكلة. راجع رمز حالة HTTP وحقل `ErrorMessage` لتحديد الإجراء التصحيحي.

## عائلة حزم SDK السحابية

يُعد استخدام حزمة SDK أفضل طريقة لتسريع التطوير. فتتولى حزمة SDK إدارة التفاصيل منخفضة المستوى وتركّز أنت على مهام مشروعك. يُرجى زيارة مستودع GitHub للحصول على قائمة كاملة بحزم SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}
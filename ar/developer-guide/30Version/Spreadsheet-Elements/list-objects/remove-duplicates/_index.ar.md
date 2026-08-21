---
title: "إزالة الصفوف المكررة من ListObject – وثائق واجهة Aspose.Cells Cloud API"
second_title: "وثيقة"
linktitle: "إزالة التكرارات"
type: docs
keywords: "إزالة التكرارات، listobject، واجهة Aspose.Cells Cloud API، إكسل، REST"
url: /ar/list-objects/remove-duplicates/
description: "تعرّف على كيفية حذف الصفوف المكررة من ListObject في ورقة عمل إكسل باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن النقطة النهائية (endpoint)، المعاملات، المصادقة، وطلبات واستجابات نموذجية."
weight: 20
---

تقوم هذه الواجهة (REST API) بإزالة الصفوف المكررة من **ListObject** في ورقة عمل إكسل.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **معاملات الطلب**

| اسم المعاملة         | النوع    | الموقع   | الوصف                                                    |
|---------------------|----------|----------|-----------------------------------------------------------|
| **name**            | نص (String) | المسار (Path) | اسم ملف إكسل.                                            |
| **sheetName**       | نص (String) | المسار (Path) | اسم ورقة العمل التي تحتوي على الكائن القائم (list object). |
| **listObjectIndex** | عدد صحيح (Integer) | المسار (Path) | الفهرس الصفري (zero-based) للكائن القائم الذي سيتم معالجته. |
| **folder**          | نص (String) | الاستعلام (Query) | (اختياري) مسار المجلد حيث يُخزَّن الملف.                  |
| **storageName**     | نص (String) | الاستعلام (Query) | (اختياري) اسم خدمة التخزين.                              |

### طلب نموذجي (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "تمت إزالة الصفوف المكررة بنجاح."
}
```

{{< /tab >}}
{{< /tabs >}}

### الاستجابة

عند النجاح، تُعيد الخدمة كائن JSON يشبه المثال أعلاه. الحقول هي:

- **Code** – رمز حالة HTTP (`200` للنجاح).
- **Status** – وصف نصي لحالة الطلب.
- **DuplicateRowsRemoved** – عدد الصفوف التي تمت إزالتها.
- **Message** – معلومات إضافية حول العملية.

**رموز حالات HTTP**

| الرمز | المعنى                      | الوصف                                                       |
|-------|-----------------------------|-------------------------------------------------------------|
| 200   | OK (نجاح)                  | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب خاطئ)     | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).      |
| 401   | Unauthorized (غير موثّق)    | رمز JWT غير صالح أو مفقود.                                  |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح.                        |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                     |

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فالـ SDK يتعامل مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى مراجعة مستودع GitHub للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}
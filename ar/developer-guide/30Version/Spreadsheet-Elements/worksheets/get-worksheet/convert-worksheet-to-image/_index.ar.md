---
title: "تحويل ورقة عمل إلى PDF و PNG و CSV وأكثر – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktitle: "تحويل ورقة العمل"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells، تحويل ورقة العمل، واجهة برمجة التطبيقات REST، cURL، SDK، PDF، PNG، CSV"
description: "تعلم كيفية تحويل ورقة عمل واحدة من ملف Excel إلى PDF و PNG و CSV وأكثر من 15 صيغة أخرى باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن مثالًا لـ cURL، وأجزاء كود SDK، ومرجع كامل للمعلمات."
weight: 130
ArticleTitle: "تحويل ورقة عمل إلى PDF و PNG و CSV وأكثر – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

**واجهة برمجة تطبيقات تحويل ورقة العمل** – نقطة النهاية `GET /cells/{name}/worksheets/{sheetName}` تحوّل ورقة عمل واحدة (ورقة داخل ملف Excel) إلى نوع ملف آخر.

> **الشرط المسبق:** يجب أن يكون لديك رمز JWT صالح وملف العمل مخزنًا في موقع مخزون Aspose Cloud المدعوم قبل استدعاء نقطة النهاية هذه.

الصيغ **المُدخَلة** المدعومة (يمكن قراءة ورقة العمل منها):

- XLS، XLSX، XLSB، CSV، TSV، XLSM، ODS، TXT

الصيغ **المُخرَجة فقط** المدعومة (يمكن حفظ ورقة العمل بها):

- PDF، OTS، XPS، DIF، PNG، JPEG، BMP، SVG، TIFF، EMF، NUMBERS، FODS

## واجهة برمجة التطبيقات REST

تُوضّح [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) الواجهة المتاحة علنًا.

### **معطيات الطلب**

| المعطى                   | النوع   | الإلزام | القيمة الافتراضية | القيم المسموح بها                                             | الوصف                                              |
| ------------------------ | ------- | ------ | ----------------- | ------------------------------------------------------------- | --------------------------------------------------- |
| **format**               | string  | نعم    | –                 | pdf، png، jpeg، bmp، svg، tiff، emf، csv، txt، … (انظر القائمة المدعومة) | صيغة الإخراج الهدف.                                 |
| **verticalResolution**   | integer | لا     | 96                | 72‑600                                                         | الدقة العمودية للإخراج الصور.                       |
| **horizontalResolution** | integer | لا     | 96                | 72‑600                                                         | الدقة الأفقية للإخراج الصور.                        |
| **password**             | string  | لا     | –                 | –                                                              | كلمة المرور لفتح ملف عمل محمي.                      |
| **folder**               | string  | لا     | –                 | –                                                              | مجلد السحابة حيث يتم تخزين ملف العمل المصدر.       |
| **storage**              | string  | لا     | –                 | –                                                              | اسم المخزن (مثلًا “Default”).                       |

### الاستجابة

| رمز الحالة | الوصف                                                                   | نوع الإرجاع                 |
| ----------- | ------------------------------------------------------------------------ | --------------------------- |
| **200**     | نجح التحويل؛ يُعاد تيار ثنائي للملف المحول.                              | `application/octet-stream`  |
| **400**     | طلب غير صالح – معطيات مفقودة أو غير صالحة.                             | كائن خطأ JSON               |
| **401**     | غير مصرّح به – رمز JWT غير صالح أو مفقود.                              | كائن خطأ JSON               |
| **404**     | غير موجود – ملف العمل أو ورقة العمل غير موجود.                         | كائن خطأ JSON               |
| **500**     | خطأ داخلي في الخادم – فشل غير متوقع.                                   | كائن خطأ JSON               |

#### مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### مثال على الاستجابة

```
الصورة المحولة (تيار ثنائي)
```

## عائلة SDK للحوسبة السحابية

استخدام SDK هو أسرع طريقة للتطوير. يُدار تفاصيل المستوى المنخفض تلقائيًا، ما يسمح لك بالتركيز على مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
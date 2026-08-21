---
title: "حساب صيغة الخلية – واجهة برمجة تطبيقات Aspose.Cells Cloud"
type: docs
url: /ar/calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud، حساب صيغة الخلية، واجهة برمجة تطبيقات Excel، واجهة برمجة تطبيقات REST، مكتبة SDK"
description: "احسب صيغة خلية في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API (الإصدار 3.0). تتضمن النقطة النهائية (endpoint)، والمعطيات، ومثال على cURL، وأكواد مقتطفات SDK."
ArticleTitle: "حساب صيغة الخلية – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

## واجهة برمجة تطبيقات REST

تحسب هذه واجهة برمجة تطبيقات REST **صيغة الخلية** في ملف Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## الأمان والمصادقة

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة مبنية على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معطيات الطلب

| اسم المعطى | النوع | موقع المعطى (path/query/body) | الوصف |
|------------|--------|--------------------------------|--------|
| name | string | path | اسم ملف Excel (مثال: `Book1.xlsx`). |
| sheetName | string | path | اسم ورقة العمل التي تحتوي على الخلية. |
| cellName | string | path | عنوان الخلية المراد حسابها (مثال: `A1`). |
| options | object | body | كائن JSON يحتوي على خيارات الحساب (انظر جدول **كائن الخيارات**). |
| folder | string | query | المجلد في التخزين حيث يوجد الملف. |
| storageName | string | query | اسم مجلد تخزين Aspose Cloud. |

#### كائن الخيارات

| الحقل | النوع | الوصف | القيمة الافتراضية |
|--------|--------|--------|------------------|
| CalcStackSize | string | الحد الأقصى لحجم كومة الحساب. | `"1"` |
| IgnoreError | boolean | إذا كانت القيمة `true`، يتم تجاهل أخطاء الحساب وتُضبط قيمة الخلية على `#N/A`. | `false` |
| Recursive | boolean | يُفعّل الحساب التكراري للخلايا التابعة. | `false` |
| Precision | string | عدد المنازل العشرية للنتائج الرقمية. | `"15"` |
| UseThreading | boolean | يُفعّل الحساب متعدد الخيوط (multi-threaded). | `false` |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | نجاح (OK) | تم تطبيق الحساب بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معطيات مفقودة أو غير صحيحة (مثال: نوع ملف غير مدعوم). |
| 401 | غير مُصادق (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حمل البيانات كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostCellCalculate API باستخدام مكتبات SDK

### مواصفات واجهة PostCellCalculate API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) واجهة برمجة تطبيقات قابلة للوصول العام وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يُظهر المثال التالي كيفية استدعاء واجهة برمجة تطبيقات Cloud باستخدام cURL. **احصل أولًا على رمز JWT** عن طريق المصادقة ضد النقطة النهائية `/connect/token` واستبدل `<jwt token>` بقيمة الرمز.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
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

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أفضل طريقة لتسريع التطوير. فالمكتبة SDK تُجيزك من تفاصيل المستوى المنخفض وتركّز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهة الويب باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}
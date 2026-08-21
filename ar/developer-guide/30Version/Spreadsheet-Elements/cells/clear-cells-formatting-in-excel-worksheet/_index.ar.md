---
title: "مسح تنسيق الخلايا في ورقة عمل Excel"
type: docs
url: /ar/clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud، Excel، مسح تنسيق الخلايا، REST API، C#، Java، PHP، Ruby، Node.js، Python، Perl، Go"
description: "استخدم واجهة Aspose.Cells Cloud REST API لمسح تنسيق الخلايا في ورقة عمل Excel. يتضمن تفاصيل الطلب، مثالًا باستخدام cURL، ومقتطفات من كود SDK بلغات برمجة متعددة."
ArticleTitle: "مسح تنسيق الخلايا في ورقة عمل Excel - واجهة Aspose.Cells Cloud API"
---

**ملاحظة:** يجب أن تتم جميع مكالمات واجهة Aspose.Cells Cloud API عبر **HTTPS**. عناوين URL الخاصة ببروتوكول HTTP غير موصى بها وقد تُحظر من قبل المتصفحات.

- **الطريقة:** POST  
- **النقطة الطرفية (Endpoint):** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

تقوم هذه الواجهة البرمجية REST بمسح تنسيق الخلايا في ملف Excel، وهي جزء من مجموعة Aspose.Cells Cloud لمسح تنسيق الخلايا في أوراق عمل Excel.

## واجهة PostClearFormats API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**مخطط الاستجابة**

| الحقل | النوع | الوصف |
|--------|---------|-----------------------------------------------|
| Code | عدد صحيح | رمز حالة HTTP الذي تعيده الواجهة (مثل 200). |
| Status | نص | نتيجة العملية (`OK` للنجاح). |

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصدق | رمز JWT غير صحيح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostClearFormats API مع مكتبات SDK

### مواصفات واجهة PostClearFormats API

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات متاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة cURL سطر الأوامر للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمة إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
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

استخدام مكتبة SDK هو أسرع طريقة للتطوير. فتقوم المكتبة بمعالجة التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا**

- [مسح محتويات الخلايا وأنماطها](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [ضبط نمط الخلية](https://docs.aspose.cloud/cells/set-cell-style)
---
---
title: "كيفية دمج الخلايا في ورقة عمل Excel – واجهة Aspose.Cells Cloud API (الإصدار 3.0)"
type: docs
url: /ar/merge-cells-in-excel-worksheet/
weight: 110
keywords: "دمج الخلايا، Aspose.Cells، واجهة Cloud API، Excel"
description: "دليل لدمج الخلايا في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API مع أمثلة لـ cURL وSDKs."
ArticleTitle: "كيفية دمج الخلايا في ورقة عمل Excel – واجهة Aspose.Cells Cloud API (الإصدار 3.0)"
---

تقوم واجهة Aspose.Cells Cloud REST API بدمج كتلة مستطيلة من الخلايا في خلية واحدة تمتد عبر الصفوف والأعمدة المحددة.

**المتطلبات المسبقة**  
- رمز JWT صالح للمصادقة.  
- يجب أن تكون المصنف موجودًا مسبقًا في مجلد التخزين المحدد.  
- يجب إعداد إعدادات التخزين (اسم المجلد واسم التخزين) في حسابك على Aspose.Cloud.

## واجهة PostWorksheetMerge

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **الأمان والمصادقة**

تُعتبر واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| الاسم            | النوع     | الموقع   | الوصف                                                |
|------------------|-----------|----------|--------------------------------------------------------|
| name             | string    | path     | اسم المصنف.                                           |
| sheetName        | string    | path     | اسم ورقة العمل.                                       |
| startRow         | integer   | query    | الفهرس الصفر-based للصف الأول (0 = الصف الأول).      |
| startColumn      | integer   | query    | الفهرس الصفر-based للعمود الأول (0 = العمود الأول).   |
| totalRows        | integer   | query    | عدد الصفوف المراد دمجها.                              |
| totalColumns     | integer   | query    | عدد الأعمدة المراد دمجها.                             |
| folder           | string    | query    | المجلد الذي يحتوي على المصنف.                        |
| storageName      | string    | query    | اسم التخزين.                                          |

*لا يُطلب أي جسم للطلب في هذه العملية.*

## **الاستجابة**

ترجع كائن CellsCloudResponse.

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                        | الوصف                                                |
|-------|-------------------------------|-------------------------------------------------------|
| 200   | OK (نجاح)                     | تمت تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب غير صالح)    | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | Unauthorized (غير مُخوّل)      | رمز JWT غير صالح أو مفقود.                           |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به.         |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                        |

## كيفية استخدام واجهة PostWorksheetMerge باستخدام SDKs

### مواصفات واجهة PostWorksheetMerge

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة **cURL** سطر الأوامر للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
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

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDK الطريقة الأفضل لتسريع عملية التطوير. فتتولى SDK إدارة التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
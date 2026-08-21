---
title: "إضافة صف فارغ إلى ورقة عمل Excel"
ArticleTitle: "إضافة صف فارغ إلى ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "الوثيقة"
linktype: "صف"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, إضافة صف فارغ, ورقة عمل, REST API, إدراج صف, جدول بيانات سحابي"
description: "استخدم واجهة برمجة تطبيقات Aspose.Cells Cloud REST لinsert صف فارغ في ورقة عمل Excel. يدعم العديد من SDKs (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) لتسريع عملية التطوير."
weight: 20
---

تقوم هذه الواجهة البرمجية REST بإضافة صف جديد إلى ورقة عمل Excel. وهي تُدرج صفًا فارغًا عند الفهرس المحدد الذي يبدأ من الصفر.

**المتطلبات المسبقة:**  
- يجب تضمين رمز وصول Aspose Cloud صالح (Bearer JWT) في رأس `Authorization`.  
- يجب رفع ملف المصنف المستهدف إلى مساحة التخزين الخاصة بك في Aspose Cloud، ويجب أن تشير المعاملات `folder` و`storageName` إلى موقعه.

**ملاحظات:**  
- يكون الفهرس `rowIndex` ابتدائيًا من الصفر؛ وإدراج صف عند الفهرس 0 يضيف صفًا في أعلى ورقة العمل.  
- تحتوي ورقات عمل Excel على 1,048,576 صفًّا كحد أقصى؛ ومحاولة الإدراج خارج هذا الحد ستؤدي إلى

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا وتستخدم <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معاملات الطلب**

| اسم المعامل | النوع | الموقع | الوصف |
|------------|------|--------|--------|
| name | string | path | اسم ملف المصنف. |
| sheetName | string | path | اسم ورقة العمل. |
| rowIndex | integer | path | الفهرس الذي يبدأ من الصفر حيث سيتم إدراج الصف الجديد. |
| folder | string | query | مسار المجلد في التخزين الذي يحتوي على المصنف. |
| storageName | string | query | اسم مساحة التخزين في Aspose Cloud التي سيتم استخدامها. |

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات متاحة للعامة، ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى الواجهة البرمجية السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **ملاحظة:** جميع مسارات Aspose.Cells Cloud تتطلب HTTPS. استخدم المخطط الآمن `https://` عند إجراء المكالمات في بيئة الإنتاج.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**رموز حالة HTTP**

| الكود | المعنى | الوصف |
|-------|---------|--------|
| 200 | OK | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | Internal Server Error | خطأ داخلي غير متوقع في الخادم. |

*مثال على استجابة خطأ (مثلًا عندما يتجاوز الفهرس الحد المسموح به لعدد الصفوف):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "فهرس الصف خارج النطاق المسموح. الحد الأقصى لعدد الصفوف المسموح به: 1048576."
}
```

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يُجرّد SDK التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}
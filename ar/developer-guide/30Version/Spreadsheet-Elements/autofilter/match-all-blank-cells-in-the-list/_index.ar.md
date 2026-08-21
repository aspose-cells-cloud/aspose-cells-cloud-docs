---
title: "تطابق جميع الخلايا الفارغة في ورقة عمل Excel"
ArticleTitle: "تطابق جميع الخلايا الفارغة في ورقة عمل Excel – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "docs"
url: /ar/autofilter/match-all-blank/
aliases: [  /ar/match-all-blank-cells-in-the-list/ ]
keywords: "Aspose.Cells، الخلايا الفارغة، AutoFilter، واجهة برمجة التطبيقات REST، Excel"
description: "تعرّف على كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST لفلترة وتطابق جميع الخلايا الفارغة في ورقة عمل Excel. يتضمن عنوان النهاية (endpoint)، المعاملات، خطوات المصادقة، مثال cURL، ومقتطفات كود SDK لغات C# وJava وPython وغيرها."
weight: 100
---

تقوم هذه الواجهة البرمجية REST بتطابق **جميع الخلايا الفارغة** في قائمة التصفية على ورقة عمل Excel.

**المتطلبات المسبقة:** قبل استدعاء هذه النهاية البرمجية، تأكد من امتلاك رمز وصول JWT صالح، ورفع المصنف إلى مستودع Aspose Cloud، ومعرفة مسار المجلد في المستودع (إن وُجد). قدم المعاملين `folder` و`storageName` إذا لم يكن الملف موجودًا في الجذر الافتراضي.

## واجهة PostWorksheetMatchBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| name | string | path | اسم ملف المصنف. |
| sheetName | string | path | اسم ورقة العمل التي تحتوي على التصفية. |
| fieldIndex | integer | query | المؤشر المبتدئ من الصفر للعمود الذي تُطبّق عليه التصفية. |
| folder | string | query | مسار المجلد في المستودع حيث يقع المصنف. |
| storageName | string | query | اسم مستودع Aspose Cloud. |

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
| 200 | OK | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostWorksheetMatchBlanks API باستخدام SDKs

### مواصفات واجهة PostWorksheetMatchBlanks API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) واجهة برمجة تطبيقات متاحة للعامة، وتتيح إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
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

يُعد استخدام SDKs أفضل طريقة لتسريع عملية التطوير. فتُجرّدك SDKs من التفاصيل منخفضة المستوى وتتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهات SDK متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}
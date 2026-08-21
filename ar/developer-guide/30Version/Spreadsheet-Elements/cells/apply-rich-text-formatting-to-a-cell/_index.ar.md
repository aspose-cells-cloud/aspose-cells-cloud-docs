---
title: "تطبيق تنسيق نص غني على خلية"
type: docs
url: /apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, نص غني, تنسيق الخلايا, واجهة برمجة تطبيقات REST, Aspose.Cells Cloud"
description: "تعلم كيفية تطبيق تنسيق نص غني على خلية محددة في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن بناء جملة الطلب، تفاصيل المُعَامِلات، مثال cURL، وأجزاء من كود SDK."
ArticleTitle: "تطبيق تنسيق نص غني على خلية باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة REST بتطبيق **تنسيق النص الغني** على خلية في ملف Excel.

**المتطلبات المسبقة:** يجب أن يكون لديك رمز JWT صالح، ويجب أن يكون ملف Excel المستهدف موجودًا مسبقًا في مجلد التخزين المُحدَّد قبل تنفيذ هذه العملية.

**الخلفية:** يسمح تنسيق النص الغني بتطبيق أنماط خطوط متعددة داخل خلية واحدة، مما يمكّن من عرض البيانات في أوراق عمل Excel بشكل أكثر تعبيرًا.

## واجهة PostCellCharacters API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| name | string | path | اسم ملف Excel (مثل `Book1.xlsx`). |
| sheetName | string | path | ورقة العمل التي تحتوي على الخلية المستهدفة. |
| cellName | string | path | عنوان الخلية المراد تنسيقها (مثل `A1`). |
| options | object | body | كائن JSON يُعرّف إعدادات تنسيق النص الغني للخلية. |
| folder | string | query | المجلد في التخزين حيث يقع ملف Excel. |
| storageName | string | query | اسم خدمة التخزين (إذا تم استخدام تخزين مخصص). |

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
| 200 | OK | تم تطبيق التنسيق بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostCellCharacters API مع SDKs

###仕様 واجهة PostCellCharacters API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) واجهة برمجة تطبيقات عامة قابلة للاستدعاء، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
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

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تتعامل الـ SDK مع التفاصيل الدقيقة من المستوى المنخفض وتسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تعرض أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*مثال لـ SDK بلغة C\**  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*مثال لـ SDK بلغة Java*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*مثال لـ SDK بلغة PHP*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*مثال لـ SDK بلغة Ruby*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*مثال لـ SDK بلغة Node.js*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*مثال لـ SDK بلغة Python*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*مثال لـ SDK بلغة Perl*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*مثال لـ SDK بلغة Go*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}
---
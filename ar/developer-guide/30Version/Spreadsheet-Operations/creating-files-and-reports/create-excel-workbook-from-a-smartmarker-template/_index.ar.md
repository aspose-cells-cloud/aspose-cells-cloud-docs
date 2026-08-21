---
title: "بناء تقارير إكسل باستخدام قوالب العلامات الذكية"
second_title: "وثيقة"
linktype: "العلامات الذكية"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "إكسل، العلامات الذكية، Aspose.Cells Cloud، REST API، ملف عمل، مكتبة برمجيات (SDK)، واجهة برمجة تطبيقات، توليد التقارير"
description: "تعرّف على كيفية إنشاء ملفات عمل إكسل من قوالب العلامات الذكية باستخدام واجهة Aspose.Cells Cloud REST API. يشمل تفاصيل الطلب والاستجابة، مثال cURL، المتطلبات المسبقة، الملاحظات، وأكواد أمثلة SDK."
weight: 40
ArticleTitle: "بناء تقارير إكسل باستخدام قوالب العلامات الذكية – دليل واجهة Aspose.Cells Cloud API"
---

تُنشئ هذه الواجهة البرمجية (REST API) ملف عمل باستخدام قالب علامة ذكية.

## واجهة برمجة تطبيقات العلامات الذكية لملف العمل

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud آمنة وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة القائمة على رمز JWT</a>.

### **ما هي العلامة الذكية؟**

العلامة الذكية هي بنية موضعية تُستخدم لربط حقول البيانات في ملف XML (أو JSON) بخلايا في قالب إكسل. وفي وقت التشغيل، تستبدل مكتبة Aspose.Cells هذه العلامات بالبيانات المقابلة، مما يسمح لك بإنشاء تقارير مُعبّأة بالكامل برمجيًا.

### **متغيرات الاستعلام (Query Parameters)**

| اسم المتغير | النوع | الوصف |
| ------------ | ------ | ------------------------------------------------------------ |
| outPath | string | المسار الوجهة حيث سيُحفظ ملف العمل الذي تم إنشاؤه. |
| folder | string | المجلد الذي يحتوي على ملف العمل الأصلي. |
| storageName | string | اسم خدمة التخزين المراد استخدامها. |

### **متغير جسم الطلب**

| اسم المتغير | النوع | الوصف |
| ------------ | ---- | ----------------------------------------------------- |
| xmlFile | file | ملف بيانات العلامات الذكية XML المرفوع مع الطلب. |

### **الاستجابة**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**ملاحظات / قيود:**  
- تدعم الواجهة البرمجية ملفات إكسل بحجم يصل إلى **50 ميغابايت**.  
- التنسيقات المقبولة هي **.xlsx** و**.xlsm** و**.xlsb** فقط.  
- تُطبّق قيودًا على معدل الطلبات بمقدار **20 طلبًا في الثانية** لكل حساب.

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | ناجح (OK) | تمت تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُعتمد (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة برمجة تطبيقات العلامات الذكية لملف العمل

### مواصفات واجهة برمجة تطبيقات العلامات الذكية لملف العمل

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) واجهة برمجة برمجية عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

### استخدام مكتبات Aspose.Cells Cloud SDK

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء مكالمات لواجهة Cloud API باستخدام cURL.

**مثال سريع مكوّن من سطر واحد**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **معالجة الأخطاء**

| حالة HTTP | الوصف | السبب الشائع |
| ----------- | --------------------- | ------------------------------------------------------- |
| 400 | طلب غير صالح (Bad Request) | ملف القالب مفقود أو ملف XML معطوب أو معلمات غير صحيحة. |
| 401 | غير مُعتمد (Unauthorized) | رمز مصادقة غير صالح أو مفقود. |
| 404 | غير موجود (Not Found) | ملف العمل أو موقع التخزين المحدد غير موجود. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | فشل غير متوقع من جانب الخادم. |

**مثال على استجابة خطأ (400)**

```json
{
  "Code": 400,
  "Message": "ملف بيانات XML مفقود أو معطوب."
}
```

## عائلة مكتبات SDK السحابية

يُعد استخدام مكتبة SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى المكتبة معالجة التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهات برمجة التطبيقات باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}
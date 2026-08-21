---
title: "واجهة بحث نصوص Aspose.Cells Cloud لملفات Excel – البحث عن نصوص في نطاقات جداول البيانات البعيدة"
second title: "وثيقة"
ArticleTitle: "البحث عن نصوص في جداول بيانات Excel البعيدة – اكتشف البيانات في نطاقات محددة"
linktitle: "البحث في محتوى النطاق البعيد"
type: docs
url: /ar/search-content-in-remote-range/
keywords: "Aspose.Cells, واجهة برمجة تطبيقات Excel, البحث عن نصوص, النطاق البعيد, جدول بيانات سحابي, واجهة برمجة تطبيقات REST, اكتشاف البيانات"
description: "ابحث عن نصوص أو أرقام أو صيغ داخل نطاق محدد من ملفات جداول بيانات Excel المحفوظة في خدمة Aspose Cloud."
weight: 100
---

## **البحث عن المحتوى داخل النطاق البعيد**

ابحث برمجيًا عن نصوص محددة ضمن أي نطاق من جداول بيانات Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. اعثر على نصوص أو أرقام أو صيغ داخل ملفات مخزنة في التخزين السحابي. واجهة برمجة تطبيقات RESTية لعمليات اكتشاف البيانات الآلية وتحليل المحتوى وتنفيذ سير عمل مراجعة جداول البيانات.

### **واجهة برمجة التطبيقات عبر الويب**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


**مثال باستخدام cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### معاملات الطلب

| اسم المعامل | النوع | المسار/الاستعلام/النص/جسم الطلب | الوصف |
| :---------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name | String | المسار | **إجباري**. اسم ملف جدول بيانات Excel الذي سيتم البحث فيه (مع امتداد الملف)، مثال: `customer_data.xlsx`. |
| worksheet | String | المسار | **إجباري**. الاسم الدقيق لورقة العمل داخل جدول البيانات الذي سيتم البحث فيه، مثال: `Orders_2024`. |
| cellArea | String | المسار | **إجباري**. النطاق المستهدف للبحث، ويُحدّد باستخدام الترميز A1 (مثال: `B2:H100`). يقتصر البحث على هذه المنطقة فقط. |
| searchText | String | الاستعلام | **إجباري**. النص أو الرقم أو المحتوى الجزئي المطلوب العثور عليه داخل النطاق المحدد. |
| ignoreCase | Boolean | الاستعلام | **اختياري**. عند تعيين القيمة إلى `true`، يتجاهل البحث الفروق في حالة الأحرف (مثلاً: "Report" يطابق "report"). القيمة الافتراضية هي `false` (حساس لحالة الأحرف). |
| folder | String | الاستعلام | **اختياري**. مسار الدليل في التخزين السحابي الخاص بك حيث يقع ملف جدول البيانات. إذا تم تجاهله، يُستخدم الدليل الجذري افتراضيًا. |
| storageName | String | الاستعلام | **اختياري**. المُعرّف الخاص بتكوين تخزين سحابي مخصص. إذا لم يُحدّد، يُستخدم التخزين الافتراضي للمستخدم. |
| region | String | الاستعلام | **اختياري**. إعداد الثقافة/المنطقة (مثال: `en‑AU`) الذي قد يؤثر على تفسير الأحرف أو التنسيقات الخاصة بالمنطقة أثناء البحث. |
| password | String | الاستعلام | **اختياري**. كلمة المرور لفك تشفير ملف جدول البيانات المحمي بكلمة مرور وفتحه. تُتجاهل هذه القيمة إذا لم يكن الملف مشفرًا. |

### الاستجابة

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

### أكواد الأخطاء

- **400 Bad Request** – رابط واجهة برمجة تطبيقات Aspose.Cells Cloud غير صالح.  
- **401 Unauthorized** – رمز الوصول أو مُعرّف العميل أو سر العميل غير صالح.  
- **404 Not Found** – ملف جدول البيانات غير قابل للوصول.  
- **500 Server Error** – ظرف غير متوقع منع الخادم من استكمال الطلب.

## أين يجب استخدام ميزة البحث عن المحتوى داخل نطاق جدول البيانات؟

- **التحقق من جودة البيانات على نطاق واسع** – أثناء مرحلة القبول في عملية ETL لمستودع البيانات، ابحث عن أوصاف حقول مفقودة أو اختصارات غير مُعرّفة أو نصوص بديلة (مثل `"TBD"` أو `"NULL"`) في جدول تعيين البيانات (`DataDictionary!B2:F1000`) لاكتشاف تعريفات البيانات غير الكاملة.  
- **توليد التقارير الديناميكية واستخراج المحتوى** – في أنظمة إنشاء التقارير الآلية، ابحث بذكاء واستخرج كتل البيانات الخاصة بالفترة الجارية المُعلَّمة بمُعرّفات محددة (مثل `"[KPI]"`) من أوراق العمل القالبية التي تحتوي على بيانات مختلطة (`Monthly_Metrics!C10:G50`) لتكوين التقرير النهائي.  
- **تحليل العقود والمستندات القانونية** – عند مراجعة ملاحق جداول البيانات التي تحتوي على العديد من البنود، احدد بفعالية المصطلحات القانونية المحددة (مثل `"liability limit"`)، أو أسماء الأطراف، أو التواريخ داخل نطاق مُحدّد (`Contract_Terms!A:A`) لتسريع عملية المراجعة.

## لماذا يجب استخدام ميزة البحث عن المحتوى داخل نطاق جدول البيانات؟

- **سهل الاستخدام للمطورين** – توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يُسهّل التطوير السريع ويُقدّم وثائق شاملة، ويقلل بشكل كبير من جهد التطوير مقارنةً بإنشاء حلول مخصصة.  
- **تقليل تكاليف العمالة** – يلغي الحاجة إلى تعيين أفراد متخصصين في دمج الوثائق.  
- **الدفع حسب الاستخدام** – لا توجد استثمارات أولية؛ تدفع فقط مقابل مكالمات الواجهة التي تستخدمها فعليًا.  
- **لا توجد تكاليف صيانة** – لا حاجة لصيانة خوادم، ولا تحديثات برمجية، ولا قلق بشأن التوافق.

## كيفية استخدام ميزة البحث عن المحتوى داخل نطاق جدول البيانات باستخدام مكتبات SDK

### مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange) واجهة برمجة تطبيقات متاحة للعامة وتسمح لك بإجراء تفاعلات REST مباشرة من خلال متصفح الويب.

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أفضل طريقة لتسريع التطوير. فالمكتبة تُدير التفاصيل الأساسية تلقائيًا، مما يتيح لك تنفيذ البحث عن محتوى داخل نطاقات جداول البيانات برمجيًا بأقل قدر ممكن من الكود. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية إجراء مكالمات لخدمات ويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---
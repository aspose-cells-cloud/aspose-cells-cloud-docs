---
title: "Aspose.Cells Cloud – API اكتشاف الروابط التالفة في Excel – مسح وتحقق من روابط جداول البيانات عن بُعد"
second_title: "مستند"
ArticleTitle: "العثور على الروابط التالفة وإصلاحها في ملفات Excel عن بُعد – أداة التحقق من الروابط في جداول البيانات السحابية"
linktitle: "البحث عن الروابط التالفة في جداول البيانات عن بُعد"
type: docs
url: /search-broken-links-in-remote-spreadsheet/
keywords: "Excel، الروابط التالفة، API، سحابة، جدول بيانات، التحقق، Aspose.Cells"
description: "استخدم API Aspose.Cells Cloud لمسح ملفات Excel المخزنة عن بُعد بحثًا عن روابط خارجية تالفة، وصيغ غير صالحة، ومصادر بيانات مفقودة."
weight: 100
---

## **البحث عن الروابط التالفة في جدول بيانات عن بُعد عبر API**

اكتشف الروابط التالفة تلقائيًا في ملفات Excel المخزنة في التخزين السحابي. تقوم واجهة برمجة التطبيقات هذه بمسح النطاقات المحددة للعثور على المراجع الخارجية التالفة، والصيغ غير الصالحة، ومصادر البيانات المفقودة. وتدعم مراجعة جداول البيانات عن بُعد، والفحوصات الآلية للجودة، والتكامل مع موفري التخزين السحابي. استخدم واجهة برمجة التطبيقات القائمة على REST لتشغيل سير عمل على مستوى المؤسسات تلقائيًا.

### **واجهة برمجة التطبيقات الويبية**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **معلمات الطلب:**

| اسم المعلمة | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
| :------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name | String | Path | **إلزامي.** اسم ملف مصنف Excel الذي سيتم مسحه للعثور على الروابط التالفة (مثل `Quarterly_Report.xlsx`). |
| worksheet | String | Query | **إلزامي.** اسم ورقة العمل التي سيتم تنفيذ عملية البحث فيها. حدد اسم الورقة بدقة كما يظهر في المصنف. |
| cellArea | String | Query | **إلزامي.** نطاق الخلايا المراد تحليله للعثور على الروابط التالفة، ويُعبّر عنه بتقنية التدوين A1 (مثل `C5:J50`). تبحث واجهة برمجة التطبيقات داخل هذا النطاق فقط. |
| folder | String | Query | **اختياري.** مسار الدليل الذي يحتوي على المصنف في التخزين السحابي الخاص بك. وإذا تُرك فارغًا، يُفترض أنه الدليل الجذري. |
| storageName | String | Query | **اختياري.** اسم تكوين التخزين السحابي المخصص الخاص بك. وإذا تُرك فارغًا، يستخدم النظام التخزين الافتراضي. |
| region | String | Query | **اختياري.** إعداد التهيئة الإقليمية التي تُطبَّق أثناء المعالجة (مثل `en-US`). قد يؤثر على تفسير بنية الصيغ أو المراجع الخاصة بالمنطقة. |
| password | String | Query | **اختياري.** كلمة المرور المطلوبة لفتح جدول بيانات مشفر. اتركه فارغًا إذا لم يكن الملف محميًا بكلمة مرور. |

**مثال على طلب cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **الاستجابة**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**مثال على استجابة JSON**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "File not found"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "External reference not supported in cloud mode"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### أكواد الأخطاء

- **400 Bad Request** – رابط واجهة برمجة تطبيقات Aspose.Cells Cloud غير صالح.  
- **401 Unauthorized** – رمز الوصول أو مُعرّف العميل أو سر العميل غير صالح.  
- **404 Not Found** – ملف جدول البيانات غير قابل للوصول.  
- **500 Server Error** – حدث خطأ أثناء جلب بيانات الحساب.

## أين يجب استخدام خدمة البحث عن الروابط التالفة داخل جدول البيانات عبر API؟

- **مراجعة منتظمة لنماذج مالية كبيرة** – قبل إصدار التقارير الشهرية أو الفصلية، امسح تلقائيًا المناطق الحسابية الرئيسية (مثل `Dashboard!B5:K50`) التي تحتوي على مراجع كثيرة لبيانات خارجية لضمان أن جميع الروابط تشير إلى ملفات مصدر صالحة.  
- **دمج البيانات في عمليات الاندماج والاستحواذ** – عند دمج جداول بيانات متعددة تمثل وحدات أعمال، امسح ورقة العمل "نظرة عامة" بعد الدمج للعثور على الروابط التي أصبحت غير صالحة بسبب تغيّر مسارات الملفات أو مشاكل الأذونات.  
- **إعداد حزم بيانات المستثمرين** – قبل إنهاء مواد العرض التقديمي التي تحتوي على رسوم بيانية وجداول مرتبطة بقواعد بيانات خارجية أو مصادر بيانات السوق، تحقق من صحة جميع الروابط.

## لماذا يجب استخدام خدمة البحث عن الروابط التالفة داخل جدول البيانات عبر API؟

- **سهل الاستخدام للمطورين** – توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يتيح تطويرًا سريعًا مع توثيق شامل. ومقارنةً ببناء حل مخصص، يقلل هذا بشكل كبير من جهود التطوير.  
- **خفض تكاليف العمالة** – أتمتة التحقق من الروابط، مما يلغي الحاجة إلى موظفين مخصصين لدمج المستندات يدويًا.  
- **الدفع حسب الاستخدام** – لا توجد استثمارات أولية؛ تدفع فقط مقابل استدعاءات API التي تستخدمها فعليًا.  
- **لا تكاليف صيانة** – لا خوادم يجب صيانتها، ولا تحديثات برمجيات، ولا مخاوف تتعلق بالتوافق.

## كيفية استخدام خدمة البحث عن الروابط التالفة داخل جدول البيانات عبر API باستخدام SDKs

### مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) واجهة برمجة تطبيقات قابلة للوصول بشكل عام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام SDKs لـ Aspose.Cells Cloud

يُعد استخدام SDK الطريقة الأكثر كفاءة لتسريع التطوير. فهي تُجرّدك من تفاصيل HTTP الأساسية، مما يسمح لك بتنفيذ كشف الروابط التالفة بكتابة كود معدود. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية التفاعل مع خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}
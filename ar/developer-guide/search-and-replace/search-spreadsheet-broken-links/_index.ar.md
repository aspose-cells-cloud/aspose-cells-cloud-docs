---
title: "البحث عن الروابط التالفة في جداول البيانات – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
ArticleTitle: "العثور على الروابط التالفة وإصلاحها في Excel – أداة فحص الروابط في جداول البيانات السحابية"
linktype: "البحث عن الروابط التالفة في جداول البيانات"
type: docs
url: /ar/search-spreadsheet-broken-links/
keywords: "Aspose Cells, روابط تالفة, مراجعة جداول البيانات, واجهة برمجة تطبيقات Excel, جدول بيانات سحابي, أداة فحص الروابط"
description: "اكتشاف الروابط التالفة وإصلاحها في ملفات Excel عبر واجهة برمجة تطبيقات Aspose.Cells Cloud. مسح النطاقات المحددة، والحصول على نتائج مفصّلة بصيغة JSON، والتكامل مع أي حزمة تطوير برمجيات (SDK) بلغة برمجة."
weight: 100
---

## **واجهة برمجة التطبيقات للبحث عن الروابط التالفة في جداول البيانات**

اكتشف الروابط التالفة تلقائيًا في ملفات Excel. تقوم واجهة برمجة التطبيقات هذه بمسح النطاقات المحددة بحثًا عن مراجع خارجية تالفة، أو صيغ غير صالحة، أو مصادر بيانات مفقودة. تدعم مراجعة جداول البيانات عن بُعد، وتشغيل فحوصات الجودة تلقائيًا، والتكامل مع موفّري التخزين السحابي. واجهة RESTful لتشغيل أتمتة سير العمل المؤسسي.

**الملخص:** استخدم هذه الواجهة لتحديد الروابط غير الصالحة وإصلاحها بسرعة في الملفات، مما يضمن سلامة البيانات في النماذج المالية، ومجموعات بيانات عمليات الدمج والاستحواذ، وحزم البيانات المُعدّة للمستثمرين.

### **واجهة ويب API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **مُعلمات الطلب**

| اسم المعلمة | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| Spreadsheet | ملف | FormData (multipart) | **مطلوبة.** ملف جدول بيانات Excel (`.xlsx`, `.xls`، إلخ) المراد تحليله. |
| worksheet | نص | استعلام | **اختياري.** اسم ورقة العمل المراد تحليلها. إذا تُركت فارغة، تُستخدم الورقة الأولى. |
| cellArea | نص | استعلام | **اختياري.** نطاق الخلايا المستهدف بصيغة A1 (مثل `B2:D10`). إذا لم يُحدّد، يُحلل النطاق المستخدم كاملاً. |
| region | نص | استعلام | **اختياري.** إعداد الترجمة (مثل `en‑GB`) الذي قد يؤثّر على تفسير التواريخ أو الأرقام أو العملات. |
| password | نص | استعلام | **اختياري.** كلمة المرور لملفات الجداول المحمية. اتركها فارغة إذا لم تكن الملف محميًا. |

### **الاستجابة**

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "الملف غير موجود",
      "Status": "Broken"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 غير موجود",
      "Status": "Broken"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### **أكواد الأخطاء**

| الكود | الوصف |
|------|--------|
| **400 Bad Request** | عنوان URI لواجهة Aspose.Cells Cloud API غير صالح. |
| **401 Unauthorized** | رمز الوصول أو معرّف العميل أو سر العميل غير صالح. |
| **404 Not Found** | ملف جدول البيانات غير قابل للوصول. |
| **429 Too Many Requests** | تجاوز الحد المسموح من الطلبات (60 طلبًا في الدقيقة). |
| **500 Server Error** | واجه جدول البيانات مشكلة أثناء جلب بيانات الحسابات. |

## **متى نستخدم واجهة البحث عن الروابط التالفة داخل جداول البيانات؟**

- **المراجعة الدورية للنماذج المالية الكبيرة**: قبل إصدار التقارير الشهرية أو الفصلية، امسح تلقائيًا المناطق الحسابية الرئيسية (مثل `Dashboard!B5:K50`) التي تحتوي على العديد من المراجع الخارجية لضمان أن جميع الروابط تشير إلى ملفات مصادر صالحة.  
- **دمج البيانات في عمليات الدمج والاستحواذ**: عند دمج ملفات جداول بيانات متعددة تمثّل وحدات أعمال مختلفة، امسح ورقة العمل "النظرة العامة" بعد الدمج لتحديد الروابط التي أصبحت غير صالحة بسبب تغيّر مسارات الملفات أو مشاكل في الأذونات.  
- **إعداد حزم بيانات المستثمرين**: قبل إعداد المواد التقديمية التي تحتوي على مخططات وجداول مرتبطة بقواعد بيانات خارجية أو مصادر بيانات سوق، تحقق من صلاحية جميع الروابط.

## **لماذا يجب استخدام واجهة البحث عن الروابط التالفة داخل جداول البيانات؟**

- **مُيسّرة للمطورين** – توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، ما يُسهّل التطوير السريع ويوفّر وثائق شاملة. وبالمقارنة مع بناء حلول مخصصة، تقلّل هذه الميزة بشكل كبير من جهد التطوير.  
- **تقليل تكاليف العمالة** – تُلغي الحاجة إلى موظفين مخصّصين لفحص الروابط في المستندات يدويًا.  
- **الدفع حسب الاستخدام** – لا يوجد استثمار مبدئي؛ تدفع فقط مقابل طلبات API التي تستخدمها فعليًا.  
- **لا تكاليف صيانة** – لا خوادم لصيانتها، ولا تحديثات برمجية، ولا مشاكل ت compatibility.  
- **الحفاظ على تنسيق Excel المعقد** – تُعاد النتائج بصيغة JSON سهلة الوصول عالميًا مع الحفاظ على هيكل ملف العمل الأصلي.

## **كيفية استخدام البحث عن الروابط التالفة داخل واجهة جداول البيانات باستخدام SDKs**

### **مواصفات OpenAPI**

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} واجهة برمجة تطبيقات متاحة علنًا، ما يسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

### **استخدام SDKs لـ Aspose.Cells Cloud**

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تتعامل SDK مع التفاصيل الدقيقة من الخلفية، ما يسمح لك بتنفيذ وظيفة البحث عن الروابط التالفة بحد أدنى من الكود. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}
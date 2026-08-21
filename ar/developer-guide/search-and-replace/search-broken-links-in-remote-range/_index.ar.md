---
title: "Aspose.Cells Cloud – اكتشاف الروابط التالفة في نطاق Excel (واجهة برمجة تطبيقات)"
secondtitle: "وثيقة"
articletitle: "العثور على الروابط التالفة وإصلاحها في نطاق Excel عن بُعد – مدقق روابط جداول البيانات السحابية"
linktitle: "البحث عن الروابط التالفة في النطاق عن بُعد"
type: docs
url: /ar/search-broken-links-in-remote-range/
keywords: "Aspose, Cells, روابط تالفة, واجهة برمجة تطبيقات, نطاق Excel, التحقق, سحابة, جدول بيانات, مرجع خارجي, مدقق"
description: "استخدم واجهة برمجة تطبيقات Aspose.Cells Cloud لمسح نطاق Excel محدد بحثًا عن روابط خارجية تالفة أو صيغ غير صالحة أو مصادر بيانات مفقودة. خدمة آمنة وسريعة وتعمل عبر السحابة."
weight: 100
---

## **البحث عن الروابط التالفة في النطاق عن بُعد عبر واجهة برمجة التطبيقات**

اكتشف تلقائيًا الروابط التالفة في بيانات النطاق لملفات Excel المخزّنة في التخزين السحابي. تقوم واجهة برمجة التطبيقات هذه بمسح النطاقات المحددة بحثًا عن مراجع خارجية تالفة أو صيغ غير صالحة أو مصادر بيانات مفقودة. وتدعم مراجعة جداول البيانات عن بُعد، والتحقق الآلي من الجودة، والتكامل مع موفّري التخزين السحابي. واجهة برمجة تطبيقات RESTful لأتمتة سير العمل المؤسسي.

### **واجهة برمجة التطبيقات عبر الويب**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **متغيرات الطلب**

| اسم المتغير | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| name | String | Path | **إجباري.** اسم ملف مصنف Excel (مثل `financial_report.xlsx`) المخزّن في التخزين السحابي والمطلوب مسحه بحثًا عن الروابط التالفة. |
| worksheet | String | Path | **إجباري.** اسم ورقة العمل المحددة (مثل `Sheet1` أو `Q4_Data`) داخل المصنف الذي يجب إجراء البحث عن الروابط التالفة فيه. |
| cellArea | String | Path | **إجباري.** عنوان نطاق الخلايا المستهدف (مثل `A1:F100`) داخل ورقة العمل المحددة الذي سيتم مسحه بحثًا عن مراجع خارجية تالفة أو صيغ أو روابط. |
| folder | String | Query | **اختياري.** المسار التشعبي للدليل في التخزين السحابي الخاص بك حيث يقع المصنف المستهدف. في حال حذف هذه القيمة، يُفترض أن الدليل الجذري هو المكان الافتراضي. |
| storageName | String | Query | **اختياري.** اسم خدمة التخزين السحابي المُعدّة لديك (مثل `DropboxBusiness` أو `S3Bucket`). في حال عدم تحديده، تستخدم واجهة برمجة التطبيقات مساحة التخزين الافتراضية الخاصة بالحساب. |
| region | String | Query | **اختياري.** إعداد الترجمة المحلي (مثل `en-GB` أو `de-DE`) ليُطبّق أثناء المسح لتفسير البيانات حسب الإعدادات الإقليمية. |
| password | String | Query | **اختياري.** كلمة المرور المطلوبة لفك تشفير مصنف محمي بكلمة مرور. اتركه فارغًا إذا لم يكن الملف مشفرًا. |

**مثال لجسم الطلب**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
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

تحتوي مجموعة `BrokenLinks` على كائنات من النوع **BrokenLink**. يوفّر كل كائن الخصائص التالية:

- **CellName** – عنوان الخلية التي تحتوي على المرجع التالف (مثل `B12`).
- **LinkType** – نوع الرابط التالف (مثل `ExternalReference` أو `Formula`).
- **ErrorMessage** – وصفٌ لسبب اعتبار الرابط تالفًا.

**ملاحظة:** تخضع واجهة برمجة التطبيقات لقيود معدل الطلبات. راجع صفحة [التسعير وقيود المعدل](https://www.aspose.cloud/pricing) للحصول على التفاصيل.

### **أكواد الأخطاء**

- **400 Bad Request** – رابط واجهة برمجة تطبيقات Aspose.Cells Cloud غير صالح.
- **401 Unauthorized** – رمز الوصول أو مُعرّف العميل أو سر العميل غير صالح.
- **404 Not Found** – ملف جدول البيانات غير قابل للوصول.
- **500 Server Error** – واجه جدول البيانات خطأً أثناء جلب بيانات الحساب.

## أين نستخدم البحث عن الروابط التالفة في نطاق جدول البيانات عبر واجهة برمجة التطبيقات؟

- **مراجعة منتظمة لنماذج التمويل الكبيرة** – قبل نشر التقارير الشهرية أو الفصلية، امسح مناطق الحسابات الأساسية (مثل `Dashboard!B5:K50`) تلقائيًا بحثًا عن الروابط التي تحتوي على مراجع بيانات خارجية كثيرة للتأكد من أن جميع الروابط تشير إلى ملفات مصادر صالحة.
- **دمج البيانات في عمليات الاستحواذ والاندماج** – عند دمج ملفات جداول بيانات متعددة تمثّل وحدات أعمال، امسح ورقة العمل "النظرة العامة" بعد الدمج لتحديد الروابط التي أصبحت غير صالحة بسبب تغيّر مسارات الملفات أو مشكلات الصلاحيات.
- **تحضير حزم بيانات المستثمرين** – قبل إنهاء مواد العرض التقديمي التي تحتوي على مخططات وجداول مرتبطة بقواعد بيانات خارجية أو مصادر بيانات السوق، تحقّق من صلاحية جميع الروابط.

## لماذا يجب استخدام البحث عن الروابط التالفة في نطاق جدول البيانات عبر واجهة برمجة التطبيقات؟

- **سهل الاستخدام للمطورين** – توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يمكّن من تطوير سريع مع توثيق شامل. ومقارنةً ببناء حل مخصص، فإن هذا يقلّل بشكل كبير من جهود التطوير.
- **تقليل تكاليف العمالة** – يلغي الحاجة إلى موظفين مخصصين لدمج المستندات يدويًا.
- **دفع مقابل الاستخدام فقط** – لا استثمار أولي؛ تدفع فقط مقابل مكالمات واجهة برمجة التطبيقات التي تقوم بها فعليًا.
- **لا تكاليف صيانة** – لا خوادم لصيانتها، ولا تحديثات برمجيات، ولا مخاوف تتعلق بالتوافق.
- **الحفاظ على تنسيق Excel المعقد** – يمكن تصدير النتائج إلى تنسيق PDF شاملاً ومتاح عالميًا دون فقدان التنسيق.

## كيف تستخدم البحث عن الروابط التالفة في نطاق جدول البيانات عبر واجهة برمجة التطبيقات باستخدام مكتبات SDK؟

### **مواصفات OpenAPI**

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) واجهة برمجة تطبيقات متاحة علنًا وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

### **استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud**

يُعد استخدام SDK أفضل طريقة لتسريع التطوير. فتتولى مكتبة SDK إدارة التفاصيل الأساسية، مما يتيح لك تنفيذ "البحث عن الروابط التالفة في نطاق" بأقل قدر ممكن من الكود. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---
title: "البحث في محتوى جداول البيانات – واجهة برمجة تطبيقات Aspose.Cells Cloud (العثور على نص في Excel)"
second_title: "مستند"
ArticleTitle: "البحث عن نص في جداول بيانات Excel المحلية – العثور على بيانات محددة"
linktype: "docs"
url: /ar/search-spreadsheet-content/
keywords: "Aspose.Cells، واجهة برمجة تطبيقات البحث في Excel، البحث في محتوى جداول البيانات، واجهة برمجة تطبيقات جداول البيانات السحابية، البحث عن النص"
description: "استخدم واجهة برمجة تطبيقات Aspose.Cells Cloud للبحث عن نصوص أو أرقام أو صيغ في ملفات Excel المحلية. تدعم الاستعلامات غير الحساسة لحالة الأحرف، وتحديد نطاق البحث داخل ورقة عمل محددة، ومصادقة آمنة."
weight: 100
---

## **واجهة برمجة تطبيقات البحث في محتوى جداول البيانات**

ابحث برمجيًا عن نصوص محددة داخل أي جدول بيانات Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. يمكن للواجهة تحديد النصوص أو الأرقام أو الصيغ في الملفات المحلية المخزنة في السحابة، مما يمكّن من أتمتة عمليات اكتشاف البيانات وتحليل المحتوى وتدقيق جداول البيانات.

### **واجهة برمجة التطبيقات على الويب**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

إذا كنت تفضل استخدام HTTP الخام، يوضح مثال cURL التالي نفس الطلب:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **معاملات الطلب**

| المعامل      | النوع    | الموقع     | الوصف                                                                 |
|-------------|---------|------------|---------------------------------------------------------------------|
| spreadsheet | ملف     | FormData   | ملف Excel الذي سيتم البحث فيه.                                          |
| searchText  | نص (String) | Query     | النص (أو القيمة العددية) الذي سيتم العثور عليه داخل المصنف.                         |
| ignoringCase | منطقي (Boolean) | Query | ضع القيمة `true` لإجراء بحث غير حساس لحالة الأحرف.                             |
| worksheet   | نص (String) | Query     | اسم ورقة العمل التي سيتم تقييد البحث فيها. إذا حُذف هذا المعامل، فسيتم مسح جميع أوراق العمل. |
| cellArea    | نص (String) | Query     | نطاق بنمط A‑1 (مثل `A1:C10`) يحدّ من منطقة البحث.                             |
| region      | نص (String) | Query     | المنطقة الجغرافية للخدمة (مثل `us-east-1`).                                 |
| password    | نص (String) | Query     | كلمة المرور المطلوبة لفتح مصنف محمي.                                        |

### **الاستجابة**

تعيد الواجهة كائن `SearchResult` يحتوي على مصفوفة من الخلايا المطابقة. ويُزوَّد كل عنصر باسم ورقة العمل وعنوان الخلية والنص المطابق.

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "المجموع",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "المجموع",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### أكواد الأخطاء

- **400 طلب غير صالح (Bad Request)** – URI أو معاملات الطلب غير صالحة.
- **401 غير مصرح به (Unauthorized)** – رمز وصول مفقود أو غير صالح أو بيانات اعتماد عميل خاطئة.
- **404 غير موجود (Not Found)** – لا يمكن الوصول إلى جدول البيانات المحدد.
- **500 خطأ داخلي في الخادم (Internal Server Error)** – حدث خطأ غير متوقع في الخادم أثناء معالجة المصنف.

## أين نستخدم واجهة برمجة التطبيقات للبحث في محتوى جدول البيانات؟

- **تدقيق شامل للامتثال داخل المصنف** – امسح المصنف كاملاً لاكتشاف المصطلحات الحساسة (مثل "بند السرية"، "بيانات داخلية") للاختبارات الأمنية والامتثالية للبيانات.
- **استعلام الارتباطات عبر الأوراق** – ابحث عن رقم مشروع أو اسم عميل يظهر في أوراق عمل متعددة، مما يُسهّل التكامل السريع عبر الأوراق.
- **التحقق من محتوى القوالب دفعة واحدة** – بعد إنشاء التقارير، تحقق من استبدال جميع العناصر النائبة (مثل `{{Date}}`) بشكل صحيح عبر دفعة من ملفات Excel.
- **أرشفة البيانات التاريخية واستخراجها** – ابحث في ملفات Excel القديمة عن رموز أحداث محددة أو مصطلحات تجارية لتسريع عمليات التنقيب وتحليل البيانات.

## لماذا يجب استخدام واجهة برمجة التطبيقات للبحث في محتوى جدول البيانات؟

- **سهلة الاستخدام للمطورين** – توفر SDKs للعديد من لغات البرمجة، مما يقلل جهود التطوير مقارنة ببناء حل مخصص.
- **تقليل تكاليف العمالة** – يُؤتمت المهام التي تتطلب عادة فحصًا يدويًا لجداول البيانات.
- **الدفع حسب الاستخدام** – تدفع فقط مقابل استدعاءات الواجهة التي تُجريها فعليًا.
- **بدون صيانة** – لا خوادم لإدارتها، ولا تحديثات برمجيات، ولا مخاوف تتعلق بالتوافق.
- **الحفاظ على التنسيقات المعقدة** – يمكن تصدير النتائج إلى PDF مع الحفاظ على تخطيط Excel الأصلي.

## كيفية استخدام البحث عن الروابط التالفة داخل جدول البيانات باستخدام SDKs

### مواصفات OpenAPI

تعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة لدمج وظيفة البحث. وتُجرّد SDKs من طبقة HTTP، ما يسمح باستدعاء الواجهة بحد أدنى من الكود. راجع القائمة الكاملة لـ SDKs في [مستودع GitHub](https://github.com/aspose-cells-cloud).

تُظهر أمثلة الكود التالية كيفية استدعاء عملية البحث في محتوى جدول البيانات باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
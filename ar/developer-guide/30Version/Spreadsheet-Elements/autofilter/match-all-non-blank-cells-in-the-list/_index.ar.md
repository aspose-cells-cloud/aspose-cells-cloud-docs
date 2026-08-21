---
title: "مطابقة جميع الخلايا غير الفارغة في ورقة عمل Excel"
second_title: "مستند"
linktype: "مطابقة جميع الخلايا غير الفارغة"
type: docs
url: /ar/autofilter/match-all-non-blank/
aliases: [  /ar/match-all-non-blank-cells-in-the-list/ ]
keywords: "Aspose.Cells Cloud، مطابقة الخلايا غير الفارغة، AutoFilter، واجهة برمجة تطبيقات Excel"
description: "تعرّف على كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API لمطابقة جميع الخلايا غير الفارغة في قائمة AutoFilter في ورقة عمل Excel. يشمل ذلك عنوان_endpoint_، المَعلمات، المصادقة، مخطط الاستجابة، رموز الأخطاء، وأمثلة SDK."
ArticleTitle: "مطابقة جميع الخلايا غير الفارغة في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
weight: 100
---

**نظرة عامة**  
يعمل إجراء *مطابقة جميع الخلايا غير الفارغة* على تطبيق فلتر تلقائي (AutoFilter) على ورقة عمل ويعيد فقط الصفوف التي تحتوي على بيانات في العمود المحدّد، مع تجاهل الخلايا الفارغة. ويُعد هذا الإجراء مفيدًا في تنظيف مجموعات البيانات، وإنشاء التقارير، أو إعداد البيانات للتحليل اللاحق.

**المتطلبات المسبقة**  
- رمز JWT صالح للمصادقة مع خدمة Aspose.Cells Cloud.  
- يجب رفع ملف المصنف (workbook) إلى مساحة التخزين في Aspose Cloud.  
- تحتاج إلى اسم الملف، واسم ورقة العمل، وفهرس العمود (بصيغة صفرية-البداية `fieldIndex`) الذي ترغب في تطبيق الفلتر عليه.

تقوم واجهة برمجة التطبيقات هذه (REST API) بمطابقة جميع الخلايا غير الفارغة في قائمة AutoFilter في ورقة عمل Excel.

## واجهة PostWorksheetMatchNonBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### مَعلمات الطلب

| اسم المعلمة | النوع | الموقع | الوصف |
| ------------ | ------- | -------- | -------------------------------------------------------------- |
| name | string | path | اسم ملف Excel. |
| sheetName | string | path | اسم ورقة العمل التي تحتوي على AutoFilter. |
| fieldIndex | integer | query | الفهرس بصيغة صفرية-البداية للعمود الذي يُطبّق عليه الفلتر. |
| folder | string | query | _(اختياري)_ مسار المجلد الذي يُخزّن فيه الملف. |
| storageName | string | query | _(اختياري)_ اسم خدمة التخزين المراد استخدامها. |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK | تمت عملية تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | مَعلمات غير مكتملة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | Internal Server Error | خطأ داخلي غير متوقع في الخادم. |

*مثال على استجابة خطأ (400)*  

```json
{
  "Code": 400,
  "Message": "معلمة غير صالحة: يجب أن يكون fieldIndex عددًا صحيحًا غير سالب."
}
```

## كيفية استخدام واجهة PostWorksheetMatchNonBlanks API باستخدام حزم التطوير (SDKs)

### مواصفات واجهة PostWorksheetMatchNonBlanks API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) واجهة برمجة تطبيقات قابلة للوصول من خارج النظام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
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

### استخدام حزم تطوير Aspose.Cells Cloud (SDKs)

استخدام حزمة التطوير (SDK) هو أفضل طريقة لتسريع عملية التطوير. فتتولى حزمة التطوير معالجة التفاصيل منخفضة المستوى، وتتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام حزم تطوير مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}
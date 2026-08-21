---
title: "واجهة Aspose.Cells Cloud الويبية - تحويل بيانات النطاق المحلي لملف Excel إلى ملف JSON - أداة مجانية عبر الإنترنت"
second_title: "مستند"
ArticleTitle: "كيف تحول بيانات النطاق في ملف جدول بيانات محلي إلى ملف JSON: دليل خطوة بخطوة"
linktype: "تحويل النطاق إلى JSON"
type: docs
url: /ar/convert-range-to-json/
keywords: "تحويل النطاق إلى JSON، Aspose.Cells Cloud، Excel إلى JSON، تحويل جداول البيانات، API"
description: "حوّل نطاقًا مُحدّدًا من ملف Excel المحلي إلى JSON باستخدام واجهة Aspose.Cells Cloud API."
weight: 100
---

صدِّر بيانات النطاق من ملف Excel محلي إلى ملف JSON باستخدام واجهة Cloud API.

## **واجهة تحويل النطاق إلى JSON**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **الأمان والمصادقة**

تُعدّ واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### **معلمات الطلب:**

| اسم المعلمة | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|-------|--------------------------------------|-------|
| Spreadsheet | ملف | FormData | رفع ملف جدول البيانات. |
| worksheet | نص | استعلام | اسم ورقة العمل داخل جدول البيانات. |
| range | نص | استعلام | منطقة الخلايا المراد تحويلها، مثل A1:C10. |
| outPath | نص | استعلام | (اختياري) مسار المجلد حيث يُخزَّن ملف العمل؛ القيمة الافتراضية هي null. |
| outStorageName | نص | استعلام | اسم مخزن ملفات الإخراج. |
| fontsLocation | نص | استعلام | موقع تخزين الخطوط المخصّصة للاستخدام الشخصي. |
| region | نص | استعلام | إعداد منطقة جدول البيانات. |
| password | نص | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### **الاستجابة**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُصادَق | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## **أين يجب استخدام واجهة تحويل النطاق إلى JSON؟**

- لوحات التحكم في الوقت الفعلي: حوّل بيانات Excel الحية إلى JSON لاستخدامها مع مكتبات الرسم البياني مثل Chart.js أو D3.js.
- جداول البيانات كخدمة (Spreadsheet-as-a-Service): قدّم نطاقات Excel كنقاط نهاية JSON لخدمات أخرى.
- حمولات Webhook: حوّل بيانات جداول البيانات إلى JSON لإرسال إشعارات Webhook.
- نماذج أولية سريعة للبيانات: حوّل بيانات Excel النظيفة بسرعة إلى JSON لتحليلها باستخدام Python أو R.
- سير عمل التعلّم الآلي: أجرِ معالجة أولية لبيانات التدريب من جداول البيانات المُدارة من قِبل الأعمال.
- عمليات التجارة الإلكترونية: زامن كتالوجات المنتجات أو أوراق أسعارها مع المواقع الإلكترونية عبر JSON.
- أتمتة التقارير: أنشئ تدفقات بيانات JSON من نماذج مالية لأغراض إنشاء تقارير تلقائية.
- تكوين التطبيقات: أدر علامات الميزات والإعدادات أو معلمات اختبارات A/B في Excel → JSON.
- الدعم متعدد اللغات: حوّل جداول البيانات الخاصة بالتعريب إلى JSON لاستخدامها مع مكتبات i18n.
- القوائم/التنقل الديناميكي: اخزن هياكل التنقل في الموقع الإلكتروني في Excel ونفّذها كـ JSON.

_لعرض خيارات التحويل الأخرى، راجع دليل [تحويل النطاق إلى CSV](/convert-range-to-csv/)._

## لماذا يجب استخدام واجهة تحويل النطاق إلى JSON؟

- **دعم SDK**: توفر Aspose.Cells Cloud مكتبات بلغات برمجة متعددة، مما يقلل من الحاجة إلى كتابة كود مخصص.
- **خفض تكاليف التخزين**: يمكن تحويل النطاق دون رفع ملف العمل بالكامل أولاً، مما يوفر مساحة تخزين.
- **التوافق مع تطبيقات الويب والجوّال**: JSON هو تنسيق البيانات الأصلي لإطارات عمل JavaScript الحديثة مثل React وVue وAngular.
- **دعم واسع للغات البرمجة**: يمكن لمعظم لغات البرمجة وقواعد البيانات قراءة JSON.
- **الحفاظ على هيكلية البيانات**
  - **الكشف الذكي عن الهيكل**: تحويل تلقائي لبيانات الجداول إلى مصفوفات أو كائنات JSON صحيحة.
  - **ربط الرؤوس**: استخدام الصف الأول كمفاتيح JSON لبناء كائنات واضحة.
  - **الحفاظ على أنواع البيانات**: الاحتفاظ بأنواع البيانات (أرقام، تواريخ، قيم منطقية) بدلاً من نصوص بسيطة.

## كيف تستخدم واجهة تحويل النطاق إلى JSON باستخدام SDKs؟

### معيار واجهة تحويل النطاق إلى JSON

يُعرّف [معيار واجهة تحويل النطاق إلى JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) واجهة برمجة تطبيقات متاحة للعامة وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDK الطريقة الأسرع للتطوير، إذ تُجرّدك من التفاصيل المنخفضة المستوى، مما يسمح لك بتحويل نطاق من البيانات إلى ملف JSON بكود موجز.  
يرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام SDKs مختلفة:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}
---
title: "قبول جميع التحديثات في جدول بيانات بعيد"
ArticleTitle: "قبول جميع التحديثات في جدول بيانات بعيد – Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "قبول جميع التحديثات في جدول بيانات بعيد"
type: docs
url: /ar/cells/accept-all-revisions
aliases: [  /ar/cells/accept-all-revisions ]
keywords: "Aspose.Cells، AcceptAllRevisions، جدول بيانات بعيد"
description: "قبول جميع التحديثات (المراجعات) في جدول بيانات بعيد وإعادة ملف المصنف المُحدّث."
weight: 1000
---

## قبول جميع التحديثات في جدول بيانات بعيد عبر خدمات Aspose.Cells Cloud واجهة الويب

تقبل هذه العملية جميع التغييرات المُتتبعة (المراجعات) في المصنف المُحدد المخزَّن في التخزين البعيد. ويمكن لهذه العملية اختياريًا حفظ المصنف الناتج في موقع أو تخزين مختلف، ثم تُعيد الملف المحدّث كتيار ثنائي.

### نقطة نهاية واجهة واجهة برمجة تطبيقات الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|----------------|------|-----------------------------|-------------|
| name | string | Path | اسم ملف المصنف المخزَّن في التخزين البعيد. |
| folder | string | Query | (اختياري) المجلد الموجود فيه المصنف ضمن التخزين. |
| storageName | string | Query | (اختياري) اسم التخزين عند استخدام تخزين سحابي مخصص. ويُستخدم التخزين الافتراضي إن حُذِف هذا المعامل. |
| outPath | string | Query | (اختياري) مسار المجلد الذي يجب حفظ المصنف المحدّث فيه. القيمة الافتراضية هي null. |
| outStorageName | string | Query | (اختياري) اسم تخزين ملف الإخراج. |
| fontsLocation | string | Query | (اختياري) مسار موقع الخطوط المخصصة. |
| region | string | Query | (اختياري) إعدادات المنطقة/اللغة لجدول البيانات (مثل `en-US` أو `fr-FR`). تؤثر هذه القيمة على تنسيق الأرقام، وتحليل التواريخ، والسلوك المتعلق باللغة المحلية. |
| password | string | Query | (اختياري) كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| *None* | *None* | لا تتطلب هذه العملية وجود جسم طلب. |

### **الاستجابة**

```json
{
  "File": "تيار ثنائي لملف المصنف المحدّث (مثل .xlsx)، يُعاد كجسم للاستجابة."
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|---------|-------------|
| 200 | OK | يُعاد المصنف الذي تم قبول جميع مراجعاته كتيار ملف ثنائي. |
| 400 | Bad Request | معاملات مطلوبة مفقودة أو تنسيق طلب غير صالح. |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | تجاوز الطلب الحدود القصوى المسموح بها للحجم. |
| 500 | Internal Server Error | حدث خطأ غير متوقع في الخادم. |

## كيفية استخدام قبول جميع التحديثات في جدول بيانات بعيد باستخدام وحدات التطوير البرمجي (SDKs)

### معيار قبول جميع التحديثات في جدول بيانات بعيد

يُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات قبول جميع التحديثات في جدول بيانات بعيد</a> واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells Cloud بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
# استخدام HTTPS لإنشاء اتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "تيار ثنائي لملف المصنف المحدّث (مثل .xlsx)."
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام وحدات التطوير البرمجي Aspose Cells Cloud

استخدام وحدة التطوير البرمجي (SDK) هو أسرع طريقة لتسريع عملية التطوير. وتُجرِّدك وحدة التطوير البرمجي من تفاصيل التنفيذ منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بوحدات تطوير البرمجي لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose Cells Cloud باستخدام مكتبات تطوير برمجية مختلفة:
 `[TBD]`
---
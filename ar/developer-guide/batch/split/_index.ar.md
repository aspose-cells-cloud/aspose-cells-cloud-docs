---
title: دفعة سبلي
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/batch/split
keywords: Batch split Excel file
description: Aspose.Cells كلاود API يدعم ملف تقسيم الدُفعات. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 100
---
يشير REST API إلى `batch split` من الملف المؤهل.
 
## رسيت API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody|وصف|
|:- |:- |:- |:- |
| BatchSplitRequest|| جسم||

**خصائص BatchSplitRequest**
 
الاسم | اكتب | الوصف | ملحوظات
------------ | ------------- | ------------- | -------------
 مجلد المصدر | سلسلة | | [اختياري] تخزين المصدر | سلسلة | | [اختياري] حالة المطابقة | طلب مطابقة الشرط | | [اختياري] التنسيق | سلسلة | | [اختياري] من الفهرس | عدد صحيح | | [اختياري] للفهرسة | عدد صحيح | | [اختياري]المجلد الخارجي | سلسلة | | [اختياري] خيارات الحفظ | خيارات الحفظ | | [خياري]**خصائص MatchConditionRequest**
 
الاسم | اكتب | الوصف | ملحوظات
------------ | ------------- | ------------- | -------------
 النمط العادي | سلسلة | | [اختياري]شروط المباراة الكاملة | سلسلة[]| | [اختياري] ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchsplit) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## عائلة Cloud SDK
 
يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على المهام المقسمة. يرجى الاطلاع على[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:
 
 
  
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< tab tabNum="10" >}}


{{< /tab >}}

{{< /tabs >}}


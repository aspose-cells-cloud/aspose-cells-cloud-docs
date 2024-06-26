﻿---
title: دفعة لوك
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/batch/lock
keywords: Batch lock of multiple Excel files
description: Aspose.Cells كلاود API يدعم القفل الدفعي لملفات اكسل المتعددة. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 100
kwords: Excel، Office كلاود، ريست API، جدول البيانات، PDF، CSV، Json، Markdwon، Batch Lock
---
يشير REST API إلى `batch lock` من الملفات المؤهلة.
 
## رسيت API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/lock
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody|وصف|
|:- |:- |:- |:- |
| BatchLockRequest|| جسم||

**خصائص BatchLockRequest**
 
الاسم | اكتب | الوصف | ملحوظات
------------ | ------------- | ------------- | -------------
 مجلد المصدر | سلسلة | | [اختياري] حالة المطابقة | طلب مطابقة الشرط | | [اختياري] كلمة المرور | سلسلة | | [اختياري]المجلد الخارجي | سلسلة | | [خياري]**خصائص MatchConditionRequest**
 
الاسم | اكتب | الوصف | ملحوظات
------------ | ------------- | ------------- | -------------
 النمط العادي | سلسلة | | [اختياري]شروط المباراة الكاملة | سلسلة[]| | [اختياري] ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}" 
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
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام القفل. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
 
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


---
title: تقسيم الدفعة
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/batch/split
keywords: Batch split Excel file
description: يدعم Cloud Aspose.Cells تقسيم الملفات دفعةً واحدة. تدعم SDK أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، تقسيم الدفعة
---
يشير هذا REST API إلى الملف المؤهل `batch split`.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طلب تقسيم الدفعة|| جسم||

**خصائص BatchSplitRequest**

الاسم | النوع | الوصف | الملاحظات
------------ | ------------- | ------------- | -------------
 مجلد المصدر | سلسلة نصية | | [اختياري]تخزين المصدر | سلسلة نصية | | [اختياري]شرط المطابقة | طلب شرط المطابقة | | [اختياري]التنسيق | سلسلة نصية | | [اختياري]من الفهرس | عدد صحيح | | [اختياري]إلى الفهرس | عدد صحيح | | [اختياري]مجلد الصادر | سلسلة نصية | | [اختياري]خيارات الحفظ | خيارات الحفظ | | [اختياري]**خصائص MatchConditionRequest**

الاسم | النوع | الوصف | الملاحظات
------------ | ------------- | ------------- | -------------
 نمط التعبير العادي | سلسلة | | [اختياري]شروط المطابقة الكاملة | سلسلة[]| | [اختياري][مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

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

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهامك المُقسّمة. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

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

{{< /tabs >}}

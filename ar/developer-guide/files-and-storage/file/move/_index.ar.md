---
title: نقل فيل
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/file/move/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: تعرف على كيفية تنزيل الملف باستخدام Aspose Cells Cloud REST API SDK الذي يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 100
---
يشير هذا REST API إلى `move file`
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| srcPath| خيط| طريق| مسار الملف المصدر على سبيل المثال '/src.ext'|
| ديسباث| خيط| استفسار| مسار ملف الوجهة على سبيل المثال "/dest.ext"|
| srcStorageName| خيط| استفسار| اسم تخزين المصدر|
| destStorageName| خيط| استفسار| اسم تخزين الوجهة|
| الإصدار| خيط| استفسار| معرف إصدار الملف المراد نقله|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## عائلة Cloud SDK
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:
 
 
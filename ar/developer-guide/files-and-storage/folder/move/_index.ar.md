﻿---
title: نقل المجلد
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/folder/move/
keywords: Learn how to move folder with Aspose Cells Cloud REST API
description: تعرف على كيفية نقل المجلد باستخدام Aspose Cells Cloud REST API SDK الذي يدعم أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 100
kwords: Excel، Office كلاود، ريست API، جدول البيانات، PDF، CSV، Json، Markdwon، نقل المجلد
---
يشير REST API إلى `move folder`
 
## رسيت API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody|وصف|
|:- |:- |:- |:- |
| srcPath| خيط| طريق| مسار المجلد المراد نقله، على سبيل المثال "/مجلد"|
| com.destPath| خيط| استفسار| مسار المجلد الوجهة للانتقال إليه، على سبيل المثال "/dst"|
| srcStorageName| خيط| استفسار| اسم تخزين المصدر|
| destStorageName| خيط| استفسار| اسم تخزين الوجهة|

 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
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
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:
 
 

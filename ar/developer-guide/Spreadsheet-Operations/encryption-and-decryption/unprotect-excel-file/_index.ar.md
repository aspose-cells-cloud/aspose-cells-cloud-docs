---
title: إلغاء حماية دفتر العمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: إلغاء حماية الملف Excel
type: docs
url: /ar/excel-file-unprotect/
aliases: [/unprotect-excel-workbooks/, /workbook/unprotect/]
keywords: REST API, spreadsheets, excel, merg
description: "Cells.Cloud API لتشغيل Excel: حماية مصنف Excel"
weight: 60
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، إلغاء حماية مصنف Excel
---
هذا REST API يقوم بإلغاء حماية Excel `workbook`.

**معلمة الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|مجلد|خيط|مجلد المصنف الأصلي.|
|اسم التخزين|خيط|اسم التخزين.|

**معلمة نص الطلب**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|حماية|طلب حماية المصنف||

**طلب حماية المصنف**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|نوع الحماية|خيط|الكل/المحتويات/لا شيء/الكائنات/السيناريوهات/الهيكل/النوافذ|
|كلمة المرور|خيط||

## الباقي API

|**API**|**يكتب**|**وصف**|**رابط سواجر**|
|:- |:- |:- |:- |
|/الخلايا/{الاسم}/الحماية|يمسح|إلغاء حماية المستند|[حذف مصنف غير محمي](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectWorkbook)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectWorkbook) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL** أداة سطر أوامر للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection" -H "accept: application/json"  -H "Content-Type: application/json" -d "{ \"ProtectionType\": \"all\", \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

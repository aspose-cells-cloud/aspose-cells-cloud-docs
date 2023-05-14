---
title: قم بفك تشفير Excel workboo
second_title: Aspose.Cells Cloud Documen
linktitle: فك
type: docs
url: /ar/workbook/decrypt/
aliases: [/decrypt-excel-workbooks/]
keywords: REST API, spreadsheets, excel, decryp
description: "Cells.Cloud API لـ Excel تعمل: فك تشفير مصنف Excel"
weight: 50
---
هذا REST API يفك تشفير Excel `workbook`.

**معامِل الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|مجلد|خيط|مجلد المصنف الأصلي.|
|اسم التخزين|خيط|اسم التخزين.|

**طلب معلمة الجسم**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|التشفير|المصنفطلب التشفير||

**المصنفطلب التشفير**
|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|نوع التشفير|خيط|XOR / Compatible / EnhancedCryptographicProviderV1 / StrongCryptographicProvider|
|طول المفتاح|عدد صحيح||
|كلمة المرور|خيط||


## REST API


|**API**|**يكتب**|**وصف**|**رابط التباهي**|
|:- |:- |:- |:- |
|/ الخلايا / {name} / التشفير|DELTE|فك تشفير وثيقة|[DeleteDecryptDocument](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptDocument)|


 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptDocument) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.

 يمكنك استخدام**cURL** أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"EncryptionType\": \"XOR\", \"KeyLength\": 1280, \"Password\": \"aspose\"}"

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

## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:


{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookDeleteDecryptDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-DecryptWorkbook-decrypt-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-DeleteDecryptDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-decrypt_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DecryptExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-DecryptWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-DecryptWorkbook-decrypt-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-DecryptWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7e303f6cbff92b225230ca3df7dd3df8" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "8982baf625e5894b2eb99f2e0f9e957e" >}}

{{< /tab >}}

{{< /tabs >}}

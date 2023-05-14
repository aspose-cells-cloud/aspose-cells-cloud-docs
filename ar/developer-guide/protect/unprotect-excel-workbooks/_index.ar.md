---
title: قم بإلغاء حماية Excel Workboo
second_title: Aspose.Cells Cloud Documen
linktitle: أونبروتيك
type: docs
url: /ar/workbook/unprotect/
aliases: [/unprotect-excel-workbooks/]
keywords: REST API, spreadsheets, excel, merg
description: "Cells.Cloud API لـ Excel تعمل: حماية مصنف Excel"
weight: 60
---
هذا REST API un- حماية Excel `workbook`.

**معامِل الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|مجلد|خيط|مجلد المصنف الأصلي.|
|اسم التخزين|خيط|اسم التخزين.|

**طلب معلمة الجسم**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|حماية|WorkbookProtectionRequest||

**WorkbookProtectionRequest**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|نوع الحماية|خيط|كل / المحتويات / لا شيء / الكائنات / السيناريوهات / الهيكل / النوافذ|
|كلمة المرور|خيط||


## REST API

|**API**|**يكتب**|**وصف**|**رابط التباهي**|
|:- |:- |:- |:- |
|/ الخلايا / {name} / الحماية|يمسح|قم بإلغاء حماية مستند|[DeleteUnProtectDocument](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectDocument)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectDocument) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.

 يمكنك استخدام**cURL** أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.

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

## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Java" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookDeleteUnProtectDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-DeleteUnProtectDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-unprotect_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-UnprotectWorkbook-unprotect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnProtectExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-UnprotectWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-UnprotectWorkbook-unprotect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-UnprotectWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e70e326db37cfb9a80aadf9d795687c5" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "a856eb7506ccc320def87e055b177ca5" >}}

{{< /tab >}}

{{< /tabs >}}

---
title: Aspose.Cells Cloud SDK لـ Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells تدعم السحابة Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 30
kwords: Excel، Office كلاود، ريست API، جدول بيانات، PDF، CSV، Json، Markdwon، Net
---
 SDK مفتوح المصدر ومرخص بموجب ترخيص MIT. يمكنك الوصول إلى الكود المصدري لمكتبة Net لـ Aspose.Cells Cloud[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).


# **كيفية استخدام مكتبة نت السحابية Aspose.Cells**

Aspose.Cells Cloud SDK for Net هي مكتبة قوية تسمح للمطورين بمعالجة ومعالجة ملفات Microsoft Excel باستخدام لغة برمجة Net. باستخدام SDK هذا، يمكنك إنشاء وتحرير وتحويل Excel مستندًا في السحابة، دون تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK for Net لتنفيذ بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## ابدء

 قبل أن تتمكن من البدء في استخدام Aspose.Cells Cloud SDK for Go، تحتاج إلى إعداد بيئة التطوير الخاصة بك وتثبيت التبعيات اللازمة. تشير إلى[المقالة](https://docs.aspose.cloud/cells/quickstart/) على الموقع الإلكتروني Aspose للحصول على معرف العميل وسر العميل.

## كيفية تثبيت باقة النت على Aspose.Cells كلاود

يمكنك تثبيت Aspose.Cells Cloud SDK for Net باستخدام nuget. فيما يلي خطوات nuget:

```nuget

Install-Package Aspose.Cells-Cloud

```

يمكنك تثبيت Aspose.Cells Cloud SDK for Net باستخدام الدوت نت أيضًا. فيما يلي خطوات الدوت نت:

```powershell

dotnet add package Aspose.Cells-Cloud 

```

## كيفية استخدام Net package لتحويل XLsx إلى PDF

- استيراد Aspose.Cells المكتبة السحابية
 ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud DotNet SDK إلى مشروعك.
- قم بتكوين API عميل ببيانات الاعتماد
 قم بتوثيق عميلك API بمعرف العميل الفريد وسر العميل.
- إعداد معلمات التحويل
 حدد المعلمات لمهمة التحويل، بما في ذلك اسم الملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام أسلوب PostConvertWorkbook والتعامل مع الاستجابة.

### **عينة من الرموز**

```CSharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Request;
using System;
using System.IO;
using System.Collections.Generic;

CellsApi cellsApi = new CellsApi("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx");
string remoteFolder = "TestData/In";

string localName = "Book1.xlsx";
string remoteName = "Book1.xlsx";

this.UploadFile( localName, remoteFolder + "/" + remoteName, "");

IDictionary<string, Stream> mapFiles =new Dictionary<string,Stream>(); 
AddFileParameter(localName,mapFiles);       
var request = new PutConvertWorkbookRequest(
    file: mapFiles,
    format: format
);
this.CellsApi.PutConvertWorkbook(request);
```

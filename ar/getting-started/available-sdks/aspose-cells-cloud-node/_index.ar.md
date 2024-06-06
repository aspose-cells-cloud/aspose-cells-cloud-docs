---
title: Aspose.Cells Cloud SDK للإيماءة
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells تدعم السحابة Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 30
kwords: Excel، Office كلاود، ريست API، جدول بيانات، PDF، CSV، Json، Markdwon، Node
---
 SDK مفتوح المصدر ومرخص بموجب ترخيص MIT. يمكنك الوصول إلى الكود المصدري لمكتبة Node لـ Aspose.Cells Cloud[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).


# **كيفية استخدام مكتبة العقدة Aspose.Cells السحابية**

Aspose.Cells Cloud SDK for Node هي مكتبة قوية تسمح للمطورين بمعالجة ومعالجة ملفات Microsoft Excel باستخدام لغة برمجة Node. باستخدام SDK هذا، يمكنك إنشاء وتحرير وتحويل Excel مستندًا في السحابة، دون تثبيت برامج أو تبعيات إضافية على جهازك المحلي.


في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK for Node لتنفيذ بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## ابدء

 قبل أن تتمكن من البدء في استخدام Aspose.Cells Cloud SDK for Go، تحتاج إلى إعداد بيئة التطوير الخاصة بك وتثبيت التبعيات اللازمة. تشير إلى[المقالة](https://docs.aspose.cloud/cells/quickstart/) على الموقع الإلكتروني Aspose للحصول على معرف العميل وسر العميل.

## كيفية تثبيت حزمة العقدة لسحابة Aspose.Cells

يمكنك تثبيت Aspose.Cells Cloud SDK للعقدة باستخدام npm. فيما يلي خطوات npm:


```Powershell

npm install asposecellscloud

```

## كيفية إضافة التبعيات في تكوين الحزمة لـ Aspose.Cells Cloud

ملف تكوين العقدة: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## كيفية استخدام حزمة Node لتحويل Xlsx إلى PDF

- استيراد Aspose.Cells المكتبة السحابية
 ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud NodeJS SDK إلى مشروعك.
- قم بتكوين API عميل ببيانات الاعتماد
 قم بتوثيق عميلك API بمعرف العميل الفريد وسر العميل.
- إعداد معلمات التحويل
 حدد المعلمات لمهمة التحويل، بما في ذلك اسم الملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام أسلوب PostConvertWorkbook والتعامل مع الاستجابة.

```javascript
var fs = require('fs');
var path = require('path');
const _ = require('asposecellscloud');

const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret,"v3.0",process.env.CellsCloudApiBaseUrl);

var remoteFolder = "TestData/In"
  
var localName = "Book1.xlsx"
var remoteName = "Book1.xlsx"

var localNameRequest = new  model.UploadFileRequest();
localNameRequest.uploadFiles ={localName:fs.createReadStream(localPath  + localName)};
localNameRequest.path = remoteFolder + "/" + remoteName ;
localNameRequest.storageName ="";
cellsApi.uploadFile(localNameRequest );
 
var format = "csv"

var mapFiles = {};           

 mapFiles[localName]= fs.createReadStream(localPath  +localName) ;

var request = new model.PutConvertWorkbookRequest();
request.file =  mapFiles;
request.format =  format;
return cellsApi.putConvertWorkbook(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});
```

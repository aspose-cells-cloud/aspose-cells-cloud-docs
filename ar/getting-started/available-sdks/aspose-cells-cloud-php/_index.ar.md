---
title: Aspose.Cells Cloud SDK لـ PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells تدعم السحابة Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 30
kwords: Excel، Office كلاود، ريست API، جدول بيانات، PDF، CSV، Json، ماركدوون، PHP
---
 SDK مفتوح المصدر ومرخص بموجب ترخيص MIT. يمكنك الوصول إلى الكود المصدري للمكتبة PHP لسحابة Aspose.Cells[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **كيفية استخدام Aspose.Cells Cloud SDK لـ PHP**

Aspose.Cells Cloud SDK لـ PHP هي مكتبة قوية تسمح للمطورين بمعالجة ومعالجة ملفات Microsoft Excel باستخدام لغة البرمجة Go. باستخدام SDK هذا، يمكنك إنشاء وتحرير وتحويل Excel مستندًا في السحابة، دون تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK لـ PHP لتنفيذ بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## ابدء

 قبل أن تتمكن من البدء في استخدام Aspose.Cells Cloud SDK for Go، تحتاج إلى إعداد بيئة التطوير الخاصة بك وتثبيت التبعيات اللازمة. تشير إلى[المقالة](https://docs.aspose.cloud/cells/quickstart/) على الموقع الإلكتروني Aspose للحصول على معرف العميل وسر العميل.

## كيفية تثبيت حزمة PHP لسحابة Aspose.Cells

يمكنك تثبيت Aspose.Cells Cloud SDK لـ PHP. فيما يلي الخطوات:

- أضف Aspose.Cells Cloud باعتبارها تبعية لملف `composer.json` الخاص بك:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- قم بتشغيل تحديث Composer لتثبيت SDK:

   ```bash

   composer install

   ```

- قم بتضمين أداة التحميل التلقائي للملحن في كود PHP الخاص بك:

   ```php

   require 'vendor/autoload.php';

   ```

## كيفية استخدام حزمة PHP لتحويل Xlsx إلى PDF

- استيراد Aspose.Cells المكتبة السحابية
 ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud PHP SDK إلى مشروعك.
- قم بتكوين API عميل ببيانات الاعتماد
 قم بتوثيق عميلك API بمعرف العميل الفريد وسر العميل.
- إعداد معلمات التحويل
 حدد المعلمات لمهمة التحويل، بما في ذلك اسم الملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام أسلوب PostConvertWorkbook والتعامل مع الاستجابة.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```

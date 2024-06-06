---
title: Aspose.Cells Cloud SDK لكل
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-perl/
description: Aspose.Cells تدعم السحابة Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 30
kwords: Excel، Office كلاود، ريست API، جدول بيانات، PDF، CSV، Json، ماركدوون، Perl
---
 SDK مفتوح المصدر ومرخص بموجب ترخيص MIT. يمكنك الوصول إلى الكود المصدري للمكتبة Perl لسحابة Aspose.Cells[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).


# **كيفية استخدام مكتبة Perl للسحابة Aspose.Cells**

Aspose.Cells Cloud SDK لـ Perl هي مكتبة قوية تسمح للمطورين بمعالجة ومعالجة ملفات Microsoft Excel باستخدام لغة البرمجة Perl. باستخدام SDK هذا، يمكنك إنشاء وتحرير وتحويل Excel مستندًا في السحابة، دون تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK لـ Perl لتنفيذ بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## ابدء

 قبل أن تتمكن من البدء في استخدام Aspose.Cells Cloud SDK for Go، تحتاج إلى إعداد بيئة التطوير الخاصة بك وتثبيت التبعيات اللازمة. تشير إلى[المقالة](https://docs.aspose.cloud/cells/quickstart/) على الموقع الإلكتروني Aspose للحصول على معرف العميل وسر العميل.

## كيفية تثبيت حزمة Perl لسحابة Aspose.Cells

يمكنك تثبيت Aspose.Cells Cloud SDK لـ Perl عن طريق الأمر أدناه:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## كيفية استخدام حزمة Perl لتحويل Xlsx إلى PDF

- استيراد Aspose.Cells المكتبة السحابية
 ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud Perl SDK إلى مشروعك.
- قم بتكوين API عميل ببيانات الاعتماد
 قم بتوثيق عميلك API بمعرف العميل الفريد وسر العميل.
- إعداد معلمات التحويل
 حدد المعلمات لمهمة التحويل، بما في ذلك اسم الملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام أسلوب PostConvertWorkbook والتعامل مع الاستجابة.

```Perl
use lib 'lib';
use strict;
use warnings;
use File::Slurp;
use MIME::Base64;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new( client_id => $ENV{'CellsCloudClientId'}, client_secret => $ENV{'CellsCloudClientSecret'});
my $instance = AsposeCellsCloud::CellsApi->new(AsposeCellsCloud::ApiClient->new( $config));

my $remoteFolder = 'TestData/In';
  
my $localName = 'Book1.xlsx';
my $remoteName = 'Book1.xlsx';

my $upload_file_request = AsposeCellsCloud::Request::UploadFileRequest->new( 'UploadFiles'=>{ $localName => $localName  }  ,'path'=>$remoteFolder . '/' . $remoteName );
 
my $format = 'csv';

my $mapFiles = {};           

 $mapFiles->{$localName}= "TestData/".$localName ;

my $request = AsposeCellsCloud::Request::PutConvertWorkbookRequest->new();
$request->{file} =  $mapFiles;
$request->{format} =  $format;
$instance->put_convert_workbook(request=> $request);
```

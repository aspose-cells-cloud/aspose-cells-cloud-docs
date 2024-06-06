---
title: Aspose.Cells Cloud SDK لـ Rub
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-ruby/
description: Aspose.Cells تدعم السحابة Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 30
kwords: Excel، Office كلاود، ريست API، جدول بيانات، PDF، CSV، Json، Markdwon، Ruby
---
 SDK مفتوح المصدر ومرخص بموجب ترخيص MIT. يمكنك الوصول إلى الكود المصدري لمكتبة روبي لـ Aspose.Cells Cloud[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby).

# **كيفية استخدام Aspose.Cells Cloud SDK لروبي**

Aspose.Cells Cloud SDK for Ruby هي مكتبة قوية تسمح للمطورين بمعالجة ومعالجة ملفات Microsoft Excel باستخدام لغة برمجة Ruby. باستخدام SDK هذا، يمكنك إنشاء وتحرير وتحويل Excel مستندًا في السحابة، دون تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK لـ Ruby لتنفيذ بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## ابدء

 قبل أن تتمكن من البدء في استخدام Aspose.Cells Cloud SDK for Go، تحتاج إلى إعداد بيئة التطوير الخاصة بك وتثبيت التبعيات اللازمة. تشير إلى[المقالة](https://docs.aspose.cloud/cells/quickstart/) على الموقع الإلكتروني Aspose للحصول على معرف العميل وسر العميل.

## كيفية تثبيت حزمة روبي لسحابة Aspose.Cells

يمكنك تثبيت Aspose.Cells Cloud SDK لـ Ruby من خلال الأمر أدناه:

```bash

    gem install aspose_cells_cloud
  
 ```

## كيفية استخدام حزمة روبي لتحويل XLSX إلى PDF

- استيراد Aspose.Cells المكتبة السحابية
 ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud Python SDK إلى مشروعك.
- قم بتكوين API عميل ببيانات الاعتماد
 قم بتوثيق عميلك API بمعرف العميل الفريد وسر العميل.
- إعداد معلمات التحويل
 حدد المعلمات لمهمة التحويل، بما في ذلك اسم الملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام أسلوب PostConvertWorkbook والتعامل مع الاستجابة.

```Ruby
require 'openssl'
require 'bundler'
require 'aspose_cells_cloud'

@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'],'v3.0',ENV['CellsCloudApiBaseUrl'])

remote_folder = 'TestData/In'

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'

format = "csv"

    
mapFiles = { }   
mapFiles = { }               
mapFiles[local_name] = ::File.open(File.expand_path("TestData/"+local_name),"r")  
 
uploadrequest = AsposeCellsCloud::UploadFileRequest.new( { :UploadFiles=>mapFiles,:path=>remote_folder })
@instance.upload_file(uploadrequest)
mapFiles[local_name]= ::File.open(File.expand_path("TestData/"+local_name),"r")
request =   AsposeCellsCloud::PutConvertWorkbookRequest.new(:File=>mapFiles,:format=>format);
@instance.put_convert_workbook(request);


```

---
title: استيراد البيانات إلى ملفات Excel وتصدير البيانات من ملفات Excel
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد وتصدير البيانات
type: docs
url: /ar/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: إنشاء مستندات أو تقارير جديدة يمكن أن تتضمن مخططات وجداول وعناصر تصور البيانات الأخرى
weight: 25
kwords: Excel استيراد البيانات مقابل الوصول المباشر إلى قاعدة البيانات؛ استيراد البيانات دفعة واحدة مقابل كتابة البيانات صفًا تلو الآخر؛ تصدير البيانات تلقائيًا مقابل استخراج البيانات يدويًا.
---
يدعم Aspose.Cells Cloud API استيراد البيانات من مجموعة متنوعة من مصادر البيانات، ويمكنه تصدير البيانات من Excel والرسوم البيانية إلى تنسيقات مختلفة، بما في ذلك Excel وCSV وPDF وHTML وPNG وما إلى ذلك. وهذا يجعل إدارة البيانات ومشاركتها بسيطة وفعالة.

## كيفية استيراد البيانات من مصادر بيانات مختلفة

استيراد البيانات إلى ملف Excel عملية معقدة. تساهم عوامل عديدة في تعقيدها، لذا يجب أخذها في الاعتبار أثناء عملية التصدير. تُعد إمكانية استيراد مختلف التنسيقات وأنواع البيانات إلى الملف بجودة احترافية ودقيقة من أهم ميزات Aspose.Cells Cloud.

### معلومات حول واجهات برمجة تطبيقات استيراد البيانات

يتم توفير واجهات برمجة التطبيقات التالية لاستيراد البيانات إلى ملف Excel أو ملفات Excel متعددة:

|API|وصف|
|:- |:- |
|[POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|استيراد البيانات إلى الملفات Excel دون استخدام مساحة التخزين.|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|استيراد البيانات إلى الملف Excel باستخدام التخزين.|

### معلمات الطلب

#### بدون استخدام التخزين

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| ملف| ملف| نموذج البيانات| الملف للتحميل|
| خيار الاستيراد| خيارات الاستيراد| نص HTTP| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

#### مع استخدام التخزين

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق||
| مجلد| خيط| استفسار||
| اسم التخزين| خيط| استفسار| اسم التخزين.|
| استيراد البيانات|| جسم||

#### معلمة خيار استيراد البيانات

**يتم وصف المعلمات المهمة في الجدول التالي**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>بيانات الدفعة</td><td>قائمة<CellValue></td> <td>بيانات الدفعة</td> </tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>هل تم إدراجه</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>مصفوفة بيانات الدفعة ذات البعدين</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>تحويل البيانات الرقمية</td><td>خيط</td> <td>صواب/خطأ.</td> </tr>
    <tr> <td>الصف الأول</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>سلسلة فاصلة</td><td> خيط</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>المحللات المخصصة</td><td>قائمة<CustomParserConfig></td><td></td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>بيانات CSV</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>الصف الأول</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>عمودي</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>بيانات</td><td> خيط[]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>هل تم إدراجه</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>صورة</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>الصف الأول</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>بيانات</td><td> عدد صحيح[،]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>هل تم إدراجه</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>مصفوفة ثنائية الأبعاد</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>الصف الأول</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>بيانات</td><td> مزدوج[،]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>هل تم إدراجه</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>مصفوفة مزدوجة الأبعاد</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>الصف الأول</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>بيانات</td><td> خيط[،]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>هل تم إدراجه</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>مصفوفة سلسلة ثنائية الأبعاد</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>الصف الأول</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>عمودي</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>بيانات</td><td> عدد صحيح[]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>هل تم إدراجه</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>مجموعة الأعداد الصحيحة</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>الصف الأول</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>عمودي</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>بيانات</td><td> مزدوج[]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>هل تم إدراجه</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>مصفوفة مزدوجة</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>الصف العلوي الأيسر</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود العلوي الأيسر</td><td>عدد صحيح</td><td></td></tr>
    <tr> <td>الصف السفلي الأيمن</td><td>عدد صحيح</td> <td></td> </tr>
    <tr> <td>العمود الأيمن السفلي</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>اسم الملف</td><td>خيط</td><td></td></tr>
    <tr><td>بيانات</td><td> خيط</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة عمل الوجهة.</td></tr>
    <tr><td>هل تم إدراجه</td><td>خيط</td><td>صواب/خطأ.</td></tr>
    <tr><td>نوع بيانات الاستيراد</td><td> خيط</td><td>مصفوفة السلاسل</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr><td>فهرس الصف</td><td>عدد صحيح</td> <td></td> </tr>
    <tr><td>فهرس العمود</td><td>عدد صحيح</td><td></td></tr>
    <tr><td>يكتب</td><td>خيط</td><td>نوع البيانات</td></tr>
    <tr><td>قيمة</td><td> خيط</td> <td></td></tr>
    <tr><td>أسلوب</td><td> النمط (الكائن)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">المعلمة</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr><td>نوع مصدر الملف</td><td>خيط</td> <td>ملفات في الذاكرة/نظام ملفات السحابة/ملفات الطلب</td> </tr>
    <tr><td>مسار الملف</td><td>خيط</td><td> موضع الملف</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## كيفية تصدير كائنات Excel إلى تنسيقات ملفات مختلفة

 إذا قمت في الأصل بإنشاء ملف Excel بتنسيق معين، مثل[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [إكس إل إس بي](https://docs.fileformat.com/spreadsheet/xlsb/) ، و[ملف CSV](https://docs.fileformat.com/spreadsheet/csv/)قد تجد أحيانًا أنه من المفيد تحويل ملف إكسل إلى صيغة أخرى للاستفادة من الميزات الخاصة التي يوفرها. على سبيل المثال، قد ترغب في تصدير ملف إكسل إلى[PDF](https://docs.fileformat.com/pdf/)لحماية محتوياتك من أي تعديلات غير مصرح بها وتسهيل قراءتها ومشاركتها في وقت واحد.

تصدير كائن Excel عملية معقدة. تساهم عوامل عديدة في تعقيدها، لذا يجب أخذها في الاعتبار أثناء عملية التصدير. تُعد إمكانية تصدير كائن Excel إلى ملف بتنسيق واحد بجودة احترافية ودقيقة من أهم ميزات Aspose.Cells Cloud.

 يعمل بشكل مثالي مع مصنفات العمل والمخططات والأشكال والصور المُصدَّرة من ملفات إكسل. يمكنك تصدير التنسيقات التالية:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [إكس إل إس بي](https://docs.fileformat.com/spreadsheet/xlsb/), [ملف CSV](https://docs.fileformat.com/spreadsheet/csv/), [تي إس في](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [المواد المستنفدة للأوزون](https://docs.fileformat.com/spreadsheet/ods/), [رسالة قصيرة](https://docs.fileformat.com/word-processing/txt/) . تنسيقات التصدير فقط:[PDF](https://docs.fileformat.com/pdf/), [أو تي إس](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [ديف](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [أرقام](https://docs.fileformat.com/spreadsheet/numbers/), [فودز](https://docs.fileformat.com/spreadsheet/fods/).

الطلب عبارة عن طلب HTTP يحتوي على محتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)يحتوي الجزء الأول من المحتوى المتعدد الأجزاء على ملف البيانات، ويحتوي الجزء الثاني على خيارات الحفظ.

مصنف REST API `export` والكائنات الداخلية لملف بتنسيق مختلف.

### معلومات التصدير API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| ملف| ملف| نموذج البيانات| الملف للتحميل|
| نوع الكائن| خيط| استفسار| نوع الكائن (مصنف/ورقة عمل/مخطط/شكل/صورة/قائمة/كائن زيتي)|
| شكل| خيط| استفسار|[تنسيق الملف](/cells/ar/supported-file-formats/)  |

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```

{{< /tab >}}

{{< /tabs >}}

## كيفية استدعاء واجهات برمجة التطبيقات للاستيراد والتصدير

تشرح المقالات التالية كل API كيفية الاتصال بالتفصيل وتحتوي على cURL وأمثلة SDK لكل API:

- [كيفية استيراد البيانات إلى الملفات Excel دون استخدام التخزين.](/cells/ar/import/without-using-storage)
- [كيفية استيراد البيانات إلى الملفات Excel باستخدام التخزين.](/cells/ar/import/with-using-storage)
- [كيفية استيراد بيانات الدفعة إلى ورقة العمل Excel](/cells/ar/import-batch-data-into-excel-worksheet/)
- [كيفية استيراد بيانات CSV إلى ورقة العمل Excel](/cells/ar/import-csv-data-into-excel-worksheet/)
- [كيفية استيراد الصورة إلى ورقة العمل Excel](/cells/ar/import-picture-into-excel-worksheet/)
- [كيفية استيراد مصفوفة الأعداد الصحيحة إلى ورقة العمل Excel](/cells/ar/import-integer-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة مزدوجة إلى ورقة العمل Excel](/cells/ar/import-double-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة نصية إلى ورقة العمل Excel](/cells/ar/import-string-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة أعداد صحيحة ثنائية الأبعاد إلى ورقة العمل Excel](/cells/ar/import-a-2D-integer-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة ثنائية الأبعاد إلى ورقة العمل Excel](/cells/ar/import-a-2D-double-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة سلسلة ثنائية الأبعاد إلى ورقة العمل Excel](/cells/ar/import-a-2D-string-array-into-excel-worksheet/)
- [تصدير الرسم البياني Excel إلى تنسيق ملف مختلف](/cells/ar/export-excel-chart-to-different-formats/)
- [تصدير كائن القائمة Excel إلى تنسيق ملف مختلف](/cells/ar/export-excel-listobject-to-different-formats/)
- [تصدير كائن ole Excel إلى تنسيق ملف مختلف](/cells/ar/export-excel-ole-object/)
- [تصدير الصورة Excel إلى تنسيق ملف مختلف](/cells/ar/export-excel-picture-to-different-formats/)
- [تصدير الشكل Excel إلى تنسيق ملف مختلف](/cells/ar/export-excel-shape-to-different-formats/)
- [تصدير مصنف Excel إلى تنسيق ملف مختلف](/cells/ar/export-excel-to-different-formats/)
- [تصدير ورقة العمل Excel إلى تنسيق ملف مختلف](/cells/ar/export-excel-worksheet-to-different-formats//)

---
title: ضمور
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API يدعم استيراد البيانات إلى ملفات Excel. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 31
---
يعد استيراد البيانات إلى ملف Excel عملية معقدة. تساهم العديد من العوامل في التعقيد ، وبالتالي ، يجب أخذها في الاعتبار أثناء عملية التصدير. تعد القدرة على استيراد أنواع التنسيقات وأنواع البيانات إلى الملف بجودة احترافية دقيقة من أهم ميزات Aspose.Cells Cloud.

## واجهات برمجة تطبيقات RSET

يتم توفير واجهات برمجة التطبيقات التالية لاستيراد البيانات إلى ملف Excel أو عدة ملفات Excel:

|API|وصف|
|:- |:- |
|[POST / خلايا / دعم](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|استيراد البيانات إلى ملفات Excel دون استخدام التخزين.|
|[نشر / خلايا / {name} / impportdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|قم باستيراد البيانات إلى ملف Excel باستخدام التخزين.|

## طلب معلمات
 
### بدون استخدام التخزين

| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| ملف| ملف| بيانات النموذج| ملف للتحميل|
| استيراد| خيارات الاستيراد| HTTPBody| IntArray / DoubleArray / StringArray / TwoDimensionIntArray / TwoDimensionDoubleArray / TwoDimensionStringArray / BatchData / CSVData / صورة|

### مع استخدام التخزين

| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق||
| مجلد| خيط| استفسار||
| اسم التخزين| خيط| استفسار| اسم التخزين.|
| بيانات الاستيراد|| جسم||


### معلمة خيار استيراد البيانات

**يتم وصف المعلمات الهامة في الجدول التالي**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>البيانات الدفعية</td><td>قائمة<CellValue></td> <td>بيانات الدُفعات</td> </tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>هو إدراج</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>ConvertNumericData</td><td>خيط</td> <td>خطأ صحيح.</td> </tr>
    <tr> <td>السطر الاول</td><td>int</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>int</td><td></td></tr>
    <tr><td>سلسلة فاصل</td><td> خيط</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>CustomParsers</td><td>قائمة<CustomParserConfig></td><td></td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>CSVData</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>السطر الاول</td><td>int</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>int</td><td></td></tr>
    <tr><td>عمودي</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>بيانات</td><td> خيط[]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>هو إدراج</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>صورة</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>السطر الاول</td><td>int</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>int</td><td></td></tr>
    <tr><td>بيانات</td><td> عدد صحيح[،]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>هو إدراج</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>السطر الاول</td><td>int</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>int</td><td></td></tr>
    <tr><td>بيانات</td><td> مزدوج[،]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>هو إدراج</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>السطر الاول</td><td>int</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>int</td><td></td></tr>
    <tr><td>بيانات</td><td> خيط[،]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>هو إدراج</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>TwoDimensionStringArray</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>السطر الاول</td><td>int</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>int</td><td></td></tr>
    <tr><td>عمودي</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>بيانات</td><td> عدد صحيح[]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>هو إدراج</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>عدد صحيح</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>السطر الاول</td><td>int</td> <td></td> </tr>
    <tr> <td>العمود الأول</td><td>int</td><td></td></tr>
    <tr><td>عمودي</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>بيانات</td><td> مزدوج[]</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>هو إدراج</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>صفيف مزدوج</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr> <td>UpperLeftRow</td><td>int</td> <td></td> </tr>
    <tr> <td>UpperLeftColumn</td><td>int</td><td></td></tr>
    <tr> <td>LowerRightRow</td><td>int</td> <td></td> </tr>
    <tr> <td>LowerRightColumn</td><td>int</td><td></td></tr>
    <tr><td>اسم الملف</td><td>خيط</td><td></td></tr>
    <tr><td>بيانات</td><td> خيط</td> <td></td></tr>
    <tr> <td>ورقة عمل الوجهة</td><td> خيط</td><td> اسم ورقة العمل الوجهة.</td></tr>
    <tr><td>هو إدراج</td><td>خيط</td><td>خطأ صحيح.</td></tr>
    <tr><td>إيمبورداتاتايب</td><td> خيط</td><td>StringArray</td></tr>
    <tr> <td>مصدر</td><td> مصدر الملف</td><td>يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr><td>RowIndex</td><td>int</td> <td></td> </tr>
    <tr><td>العمود فهرس</td><td>int</td><td></td></tr>
    <tr><td>يكتب</td><td>خيط</td><td>نوع البيانات</td></tr>
    <tr><td>قيمة</td><td> خيط</td> <td></td></tr>
    <tr><td>أسلوب</td><td> النمط (كائن)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">معامل</th><th scope="col">يكتب</th> <th scope="col">وصف</th></tr>
  </thead>
  <tbody>
    <tr><td>نوع مصدر الملف</td><td>خيط</td> <td>InMemoryFiles / CloudFileSystem / RequestFiles</td> </tr>
    <tr><td>مسار الملف</td><td>خيط</td><td> موضع الملف</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## كيفية استدعاء واجهات برمجة تطبيقات RSET

تشرح المقالات التالية كل API كيفية الاتصال بالتفصيل وتحتوي على cURL وأمثلة SDK لكل API:

- [كيفية استيراد البيانات إلى ملفات Excel دون استخدام التخزين.](/cells/ar/import/without-using-storage)
- [كيفية استيراد البيانات إلى ملفات Excel باستخدام التخزين.](/cells/ar/import/with-using-storage)
- [كيفية استيراد الدُفعات إلى ورقة عمل Excel](/cells/ar/import/batch-data/)
- [كيفية استيراد بيانات CSV إلى ورقة عمل Excel](/cells/ar/import/csv-data/)
- [كيفية استيراد الصورة إلى ورقة عمل Excel](/cells/ar/import/picture/)
- [كيفية استيراد مصفوفة عدد صحيح إلى ورقة عمل Excel](/cells/ar/import/integer-array/)
- [كيفية استيراد صفيف مزدوج إلى ورقة عمل Excel](/cells/ar/import/double-array/)
- [كيفية استيراد صفيف السلسلة إلى ورقة عمل Excel](/cells/ar/import/string-array/)
- [كيفية استيراد 2 Dimension Integer Array في Excel ورقة عمل](/cells/ar/import/2dimension-integer-array/)
- [كيفية استيراد صفيف مزدوج ثنائي الأبعاد في ورقة عمل Excel](/cells/ar/import/2dimension-double-array/)
- [كيفية iImport 2 Dimension String Array في ورقة عمل Excel](/cells/ar/import/2dimension-string-array/)

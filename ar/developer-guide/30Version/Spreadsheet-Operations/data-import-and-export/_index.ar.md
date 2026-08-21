---
title: "استيراد البيانات إلى ملفات Excel وتصدير البيانات من ملفات Excel"
second_title: "Document"
linktitle: "استيراد وتصدير البيانات"
type: docs
url: /data-import-and-export/
keywords: "Aspose.Cells Cloud, استيراد البيانات, تصدير Excel, API, CSV, JSON, صورة, مصفوفة"
description: "تعرّف على كيفية استيراد البيانات من ملفات CSV وJSON والمصفوفات والصور إلى ملفات Excel، وتصدير كتب العمل والرسوم البيانية والأشكال إلى PDF وPNG وغير ذلك باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud (النسخة 3.0)."
weight: 25
---

تدعم واجهة برمجة تطبيقات Aspose.Cells Cloud استيراد البيانات من مصادر متنوعة، كما يمكنها تصدير كتب عمل Excel والرسوم البيانية والكائنات الأخرى إلى صيغ مختلفة، تشمل **XLSX** و**CSV** و**PDF** و**HTML** و**PNG** والمزيد. ويجعل هذا إدارة البيانات ومشاركتها بسيطة وفعّالة.

**إصدار واجهة برمجة التطبيقات:** **v3.0** – آخر تحديث: **2024‑03‑15**

### دليل البدء السريع

1. **تجهيز حمولة الطلب** – بناء هيكل JSON يصف خيارات الاستيراد أو التصدير (مثل `ImportCSVDataOption` و`ExportOptions`).
2. **إرسال الطلب** – استخدام `curl` أو Postman أو SDK لاستدعاء نقطة النهاية المناسبة (`POST /cells/import` أو `POST /cells/export`).
3. **معالجة الاستجابة** – عند النجاح، تُستلم الملف المعالج (ثنائي أو مشفر بـ Base64). وفي حالة حدوث خطأ، تُفحَص كود حالة HTTP والرسالة الخطأ المُعادة في هيكل JSON.

#### المتطلبات الأساسية

- حساب نشط على Aspose Cloud ومفتاح JWT صالح.
- يجب أن يكون كتاب العمل الهدف موجودًا في موقع التخزين المحدّد (لواجهات برمجة التطبيقات المعتمدة على التخزين).
- رؤوس `Content-Type` الصحيحة (`multipart/form-data` لتحميل الملفات، `application/json` للأجسام JSON).

## كيفية استيراد البيانات من مصادر بيانات متنوعة

يتضمّن استيراد البيانات إلى ملف Excel عدة اعتبارات يجب أخذها بعين الاعتبار أثناء العملية. إن إمكانية استيراد تنسيقات وأنواع بيانات متعددة بدقة احترافية تُعدّ من الميزات الرئيسية في Aspose.Cells Cloud.

### معلومات واجهات برمجة التطبيقات لاستيراد البيانات

توفّر واجهات برمجة التطبيقات التالية إمكانية استيراد البيانات إلى ملف Excel واحد أو أكثر:

| واجهة برمجة التطبيقات                                                                              | الوصف                                               |
| :-------------------------------------------------------------------------------------------------- | :-------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | استيراد البيانات إلى ملفات Excel دون استخدام التخزين. |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | استيراد البيانات إلى ملف Excel المخزّن في السحابة. |

### معاملات الطلب

#### دون استخدام التخزين

| اسم المعامل | النوع          | الموقع     | الوصف                                                                                                    |
| :---------- | :------------- | :--------- | :------------------------------------------------------------------------------------------------------- |
| file        | ملف            | formData   | الملف المراد رفعه                                                                                         |
| ImportOption | ImportOptions | body       | يحدّد تنسيق الاستيراد (IntArray، DoubleArray، StringArray، TwoDimensionIntArray، TwoDimensionDoubleArray، TwoDimensionStringArray، BatchData، csvData، Picture) |

#### باستخدام التخزين

| اسم المعامل | النوع          | الموقع     | الوصف                 |
| :---------- | :------------- | :--------- | :--------------------- |
| name        | string         | path       | اسم ملف Excel          |
| folder      | string         | query      | مسار المجلد في التخزين |
| storageName | string         | query      | اسم التخزين            |
| importData  | ImportOptions  | body       | حمولة استيراد البيانات |

#### معاملات خيار استيراد البيانات

**تُوصَف المعاملات المهمّة في الجداول التالية:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>بيانات الدفعة المراد استيرادها</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ما إذا كان سيتم إدراج البيانات (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>ما إذا كان سيتم تحويل البيانات الرقمية (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>فهرس الصف الأول</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>فهرس العمود الأول</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>فاصل الأعمدة</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>إعدادات محللات مخصصة</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>فهرس الصف الأول</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>فهرس العمود الأول</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>ما إذا كانت الصورة موضّعة رأسيًا (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>بيانات الصورة (سلاسل مشفرة بـ Base64)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ما إذا كان سيتم إدراج البيانات (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>فهرس الصف الأول</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>فهرس العمود الأول</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>مصفوفة عددية صحيحة ثنائية الأبعاد</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ما إذا كان سيتم إدراج البيانات (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>فهرس الصف الأول</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>فهرس العمود الأول</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>مصفوفة ذات أبعاد مزدوجة من نوع double</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ما إذا كان سيتم إدراج البيانات (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>فهرس الصف الأول</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>فهرس العمود الأول</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>مصفوفة سلاسل نصية ثنائية الأبعاد</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ما إذا كان سيتم إدراج البيانات (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>فهرس الصف الأول</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>فهرس العمود الأول</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>ما إذا كانت المصفوفة رأسية (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>مصفوفة عددية صحيحة أحادية البعد</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ما إذا كان سيتم إدراج البيانات (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>فهرس الصف الأول</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>فهرس العمود الأول</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>ما إذا كانت المصفوفة رأسية (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>مصفوفة من نوع double أحادية البعد</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ما إذا كان سيتم إدراج البيانات (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>فهرس الصف العلوي الأيسر</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>فهرس العمود العلوي الأيسر</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>فهرس الصف السفلي الأيمن</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>فهرس العمود السفلي الأيمن</td></tr>
    <tr><td>Filename</td><td>string</td><td>اسم الملف المصدر</td></tr>
    <tr><td>Data</td><td>string</td><td>البيانات النصية المراد استيرادها</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>اسم ورقة العمل الوجهة</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>ما إذا كان سيتم إدراج البيانات (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>مكان ملف البيانات عند وجود BatchData كـ null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>فهرس الصف للخلية</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>فهرس العمود للخلية</td></tr>
    <tr><td>type</td><td>string</td><td>نوع بيانات قيمة الخلية</td></tr>
    <tr><td>value</td><td>string</td><td>قيمة الخلية</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>تعريف نمط الخلية</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>المعامل</th><th>النوع</th><th>الوصف</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles أو CloudFileSystem أو RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>مسار الملف المصدر</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## كيفية تصدير كائنات Excel إلى صيغ ملفات متنوعة

إذا أنشأتم ملف Excel في البداية بصيغة مثل **XLS** أو **XLSX** أو **XLSB** أو **CSV**، فقد ترغبون في تحويله إلى صيغة أخرى للاستفادة من ميزات محددة. على سبيل المثال، يحمي تصدير الملف بصيغة **PDF** المحتوى من التعديلات غير المصرح بها، مع جعله سهل القراءة والمشاركة.

يتضمّن تصدير كائنات Excel عدة اعتبارات. وتوفّر Aspose.Cells Cloud تصديرًا عالي الجودة لكتب العمل والرسوم البيانية والأشكال والصور إلى مجموعة واسعة من الصيغ:

_صيغ التصدير فقط_: PDF وOTS وXPS وDIF وPNG وJPEG وBMP وSVG وTIFF وEMF وNUMBERS وFODS.  
_صيغ تدعم الاستيراد والتصدير معًا_: XLS وXLSX وXLSB وCSV وTSV وXLSM وODS وTXT.

يستخدم الطلب محتوى متعدد الأجزاء كما هو مُعرّف في [RFC 2046] و[RFC 1341]. يحتوي الجزء الأول على ملف البيانات؛ ويحتوي الجزء الثاني على خيارات الحفظ.

### معلومات واجهة برمجة التطبيقات للتصدير

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### معاملات الطلب

| اسم المعامل | النوع   | الموقع     | الوصف                                                                                      |
| :---------- | :------ | :--------- | :------------------------------------------------------------------------------------------ |
| file        | ملف     | formData   | الملف المراد رفعه                                                                           |
| objectType  | string  | query      | نوع الكائن (`workbook` أو `worksheet` أو `chart` أو `shape` أو `picture` أو `listobject` أو `oleobject`) |
| format      | string  | query      | صيغة ملف الإخراج المطلوبة (انظر [صيغ الملفات المدعومة](/cells/supported-file-formats/))     |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) واجهة برمجة تطبيقات عامة قابلة للوصول تتيح تنفيذ تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء واجهة برمجة التطبيقات. يوضّح المثال التالي طلبًا واستجابته بصيغة JSON.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### كودات حالة HTTP الشائعة

| الحالة | المعنى                                                        | الإجراء الموصى به                           |
| ------ | -------------------------------------------------------------- | -------------------------------------------- |
| 200    | نجاح – تم تصدير الملف                                         | معالجة الملف (الملفات) المُعادة             |
| 400    | طلب غير صالح – معاملات مفقودة أو غير صالحة                  | التحقق من حمولة الطلب وسلاسل الاستعلام       |
| 401    | غير مصرّح – مفتاح JWT غير صالح أو منتهي الصلاحية             | تحديث المفتاح وإعادة المحاولة                |
| 404    | غير موجود – كتاب العمل أو ورقة العمل المحدّدة غير موجودة     | التحقق من اسم الملف ومسار التخزين            |
| 500    | خطأ داخلي في الخادم – حالة غير متوقّعة على الخادم           | الاتصال بدعم Aspose مع معرّف الطلب           |

## كيفية استدعاء واجهات برمجة التطبيقات للاستيراد والتصدير

تشرح المقالات التالية كل واجهة برمجة تطبيقات بالتفصيل، وتحتوي على أمثلة باستخدام cURL وSDKs:

- [كيفية استيراد البيانات إلى ملفات Excel دون استخدام التخزين.](/cells/import/without-using-storage)
- [كيفية استيراد البيانات إلى ملفات Excel باستخدام التخزين.](/cells/import/with-using-storage)
- [كيفية استيراد بيانات دُفعات إلى ورقة عمل Excel](/cells/import-batch-data-into-excel-worksheet/)
- [كيفية استيراد بيانات CSV إلى ورقة عمل Excel](/cells/import-CSV-data-into-excel-worksheet/)
- [كيفية استيراد صورة إلى ورقة عمل Excel](/cells/import-picture-into-excel-worksheet/)
- [كيفية استيراد مصفوفة عددية صحيحة إلى ورقة عمل Excel](/cells/import-integer-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة double إلى ورقة عمل Excel](/cells/import-double-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة سلاسل نصية إلى ورقة عمل Excel](/cells/import-string-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة عددية صحيحة ثنائية الأبعاد إلى ورقة عمل Excel](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة double ثنائية الأبعاد إلى ورقة عمل Excel](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [كيفية استيراد مصفوفة سلاسل نصية ثنائية الأبعاد إلى ورقة عمل Excel](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [تصدير الرسم البياني لملف Excel إلى صيغة ملف مختلفة](/cells/export-excel-chart-to-different-formats/)
- [تصدير كائن قائمة Excel إلى صيغة ملف مختلفة](/cells/export-excel-listobject-to-different-formats/)
- [تصدير كائن OLE Object في Excel إلى صيغة ملف مختلفة](/cells/export-excel-ole-object/)
- [تصدير صورة Excel إلى صيغة ملف مختلفة](/cells/export-excel-picture-to-different-formats/)
- [تصدير شكل Excel إلى صيغة ملف مختلفة](/cells/export-excel-shape-to-different-formats/)
- [تصدير كتاب عمل Excel إلى صيغة ملف مختلفة](/cells/export-excel-to-different-formats/)
- [تصدير ورقة عمل Excel إلى صيغة ملف مختلفة](/cells/export-excel-worksheet-to-different-formats/)

---
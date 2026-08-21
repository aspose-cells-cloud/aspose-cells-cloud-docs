---
title: "دليل المطورين لـ Aspose.Cells Cloud الإصدار 3.0"
ArticleTitle: "دليل المطورين لواجهة Aspose.Cells Cloud REST API الإصدار 3.0 – إنشاء ملفات جداول البيانات وإعدادها وتحويلها"
second_title: "الوثيقة"
type: docs
url: /developer-guide-3.0/
aliases: [/developer-guide/v3.0/, /developer-guide-v3.0/]
keywords: "Aspose.Cells Cloud, واجهة REST لجداول البيانات Excel, تحويل ملفات العمل, واجهة رسومات البيانات, استيراد البيانات, تصديرها, PDF, CSV, JSON, دليل المطورين"
description: "تعلم كيفية استخدام واجهات Aspose.Cells Cloud REST API الإصدار 3.0 لإنشاء ملفات جداول البيانات Excel وتحويلها وتنسيقها وإضافة الرسوم البيانية والجداول وغيرها. يتضمن أمثلة على الأكواد ونصائح مُستوحاة من أفضل الممارسات."
weight: 150
---

## العمل مع واجهات Aspose.Cells Cloud REST API

يوفِّر **دليل المطورين لـ Aspose.Cells Cloud الإصدار 3.0** نظرة موجزة وقابلة للبحث عن أكثر عمليات واجهة REST API استخدامًا لملفات جداول البيانات Excel وأوراق العمل. وهو موجّه للمطورين الذين يحتاجون إلى إنشاء وتعديل وتحويل ملفات Excel برمجيًا. استخدم الأقسام التالية لتحديد العملية المطلوبة؛ كل رابط يُوجِّهك إلى صفحة مفصّلة تحتوي على بنية الطلب والمعطيات والأمثلة. تُركِّز هذه الصفحة المحورية على مرجع **واجهة Aspose.Cells Cloud REST API**، مما يُسهّل العثور على نقاط النهاية المرتبطة بملفات العمل، وإدارة الرسوم البيانية، واستيراد البيانات وتصديرها.

**المتطلبات المسبقة:** قبل استخدام الواجهات، تأكّد من امتلاكك حسابًا فعّالًا على Aspose Cloud ومفتاح وسرّ API، وتثبيت حزم SDK المناسبة لبيئة التطوير الخاصة بك.

### جدول المحتويات

- [عمليات الملفات](#file-operations)
- [الصفحة الرئيسية (تنسيق الخلايا وإدارة الصفوف والأعمدة)](#home-cell-formatting--rowcolumn-management)
- [إدراج (رسوم بيانية وجداول وكائنات OLE)](#insert-charts-tables--ole-objects)
- [تخطيط الصفحة (فواصل الصفحات والإعدادات)](#page-layout-page-breaks--setup)
- [الصيغ (الحساب والأسماء)](#formulas-calculate--names)
- [البيانات (المخطط التفصيلي والترشيح والاستيراد)](#data-outline-filter--import)
- [المراجعة (التعليقات والحماية)](#review-comments--protection)
- [العرض (نافذة وتحكم في التكبير)](#view-window--zoom-controls)

### ملخص سريع للواجهة

| مجموعة الواجهات      | نقطة نهاية معيّنة                                      | الإجراء الأساسي                                              |
| -------------------- | ------------------------------------------------------ | ------------------------------------------------------------ |
| **إنشاء ملف عمل**    | `POST /cells/workbook`                                 | إنشاء ملف عمل Excel فارغ جديد                                |
| **تحويل ملف العمل**  | `PUT /cells/workbook/convert`                          | تحويل ملف Excel إلى PDF أو CSV أو JSON وما إلى ذلك           |
| **إضافة رسم بياني**  | `POST /cells/worksheets/{sheetName}/charts`            | إدراج رسم بياني جديد في ورقة عمل                             |
| **إدارة الجداول**    | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | تحديث أو حذف كائن قائمة (جدول)                               |
| **استيراد البيانات** | `POST /cells/worksheets/{sheetName}/import`            | استيراد ملفات CSV أو JSON أو الصور أو المصفوفات إلى ورقة عمل |
| **حساب الصيغ**       | `POST /cells/workbook/calculate`                       | إعادة حساب جميع الصيغ في ملف العمل                           |
| **تطبيق المرشّحات**  | `POST /cells/worksheets/{sheetName}/filters`           | إضافة أو حذف معايير الترشيح التلقائي                         |
| **حماية ملف العمل**  | `POST /cells/workbook/protect`                         | تطبيق الحماية بكلمة مرور على ملف العمل                       |

تغطي هذه العمليات ذات التردد العالي التغطية الأساسية لوظائف **واجهة Aspose.Cells Cloud REST API لجداول البيانات Excel**، وتربط مباشرةً بصفحات التوثيق التفصيلية.

يمكنك تنزيل نسخة PDF من جدول الملخص السريع للاستخدام دون اتصال بالإنترنت.

{{< tabs tabTotal="8" tabID="1" tabName1="الملف" tabName2="الصفحة الرئيسية" tabName3="إدراج" tabName4="تخطيط الصفحة" tabName5="الصيغ" tabName6="البيانات" tabName7="المراجعة" tabName8="العرض" >}}
{{< tab tabNum="1" >}}

<div class="row">
    <div class="col-md-6">
        <p>ملف العمل: إنشاء جديد، تحويل، حفظ باسم</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="Create an empty Excel workbook via API" rel="noopener">إنشاء ملف عمل Excel فارغ.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="Create a workbook from a template file" rel="noopener">إنشاء ملف عمل Excel من ملف قالب.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="Create a workbook from a SmartMarker template" rel="noopener">إنشاء ملف عمل Excel من قالب SmartMarker.</a></li>
            <li><a href="/cells/convert/" title="Convert an Excel workbook to another format" rel="noopener">تحويل ملف عمل Excel إلى تنسيقات ملفات مختلفة.</a></li>
            <li><a href="/cells/saveas-other-formats/" title="Save an Excel workbook as another format" rel="noopener">حفظ ملف عمل Excel بصيغ ملفات مختلفة.</a></li>
        </ul>
        <p>بحث واستبدال</p>
        <ul>
            <li><a href="/cells/search/" title="Search text in Excel files" rel="noopener">البحث عن نص داخل ملفات Excel.</a></li>
            <li><a href="/cells/replace/" title="Replace values in Excel files" rel="noopener">استبدال القيم القديمة بقيم جديدة داخل ملفات Excel.</a></li>
        </ul>
        <p>ضغط</p>
        <ul>
            <li><a href="/cells/compress/" title="Compress Excel files" rel="noopener">ضغط ملفات Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>ملف العمل: دمج، تقسيم</p>
        <ul>
            <li><a href="/cells/merge/" title="Merge multiple Excel workbooks" rel="noopener">دمج ملفات عمل Excel.</a></li>
            <li><a href="/cells/split/" title="Split an Excel workbook into separate files" rel="noopener">تقسيم ملفات عمل Excel.</a></li>
        </ul>
        <p>الشعارات المائية</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="Add a background image to a workbook" rel="noopener">إضافة خلفية إلى ملف عمل.</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="Delete a workbook background image" rel="noopener">حذف صورة الخلفية من ملف عمل.</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="Set a background or watermark on a worksheet" rel="noopener">تعيين خلفية أو شعار مائي لورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="Delete a worksheet background or watermark" rel="noopener">حذف الخلفية أو الشعار المائي من ورقة عمل Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>خطوط الخلايا وأنماطها وتنسيقها الشرطي والقيم</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="Retrieve a cell style from a worksheet" rel="noopener">استرجاع نمط خلية من ورقة عمل Excel.</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="Update styles of multiple cells" rel="noopener">تحديث أنماط خلايا متعددة في ورقة عمل Excel.</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="Change a single cell's style" rel="noopener">تحديث نمط خلية واحدة في ورقة عمل Excel.</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title="Apply rich‑text formatting to a cell" rel="noopener">تطبيق تنسيق نص غني لخلية في ورقة عمل Excel.</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="Clear cell contents and styles" rel="noopener">مسح محتويات وأنماط الخلايا في ورقة عمل Excel.</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="Manage conditional formatting rules" rel="noopener">إضافة وحذف وتحديث التنسيق الشرطي في ورقة عمل Excel.</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="Set the value of a cell" rel="noopener">تعيين قيمة خلية في ورقة عمل Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>الصف/العمود: إدراج، حذف، نسخ، إخفاء، والضبط التلقائي</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="Insert an empty row into a worksheet" rel="noopener">إضافة صف فارغ في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="Delete a row from a worksheet" rel="noopener">حذف صف من ورقة عمل Excel.</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="Copy rows within a worksheet" rel="noopener">نسخ صفوف داخل ورقة عمل Excel.</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="Hide rows in a worksheet" rel="noopener">إخفاء صفوف في ورقة عمل Excel.</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="Auto‑fit rows in a workbook" rel="noopener">ضبط صفوف تلقائيًا في ملف عمل Excel.</a></li>
            <li><a href="/cells/columns/add/" title="Insert an empty column into a worksheet" rel="noopener">إضافة عمود فارغ في ورقة عمل Excel.</a></li>
            <li><a href="/cells/columns/delete/" title="Delete a column from a worksheet" rel="noopener">حذف عمود من ورقة عمل Excel.</a></li>
            <li><a href="/cells/columns/copy/" title="Copy columns within a worksheet" rel="noopener">نسخ أعمدة داخل ورقة عمل Excel.</a></li>
            <li><a href="/cells/columns/hide/" title="Hide columns in a worksheet" rel="noopener">إخفاء أعمدة في ورقة عمل Excel.</a></li>
            <li><a href="/cells/columns/autofit/" title="Auto‑fit columns in a workbook" rel="noopener">ضبط أعمدة تلقائيًا في ملف عمل Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>الرسم البياني</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="Add a chart to a worksheet" rel="noopener">إضافة رسم بياني في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="Delete a chart from a worksheet" rel="noopener">حذف رسم بياني من ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="Delete all charts from a worksheet" rel="noopener">حذف جميع الرسوم البيانية من ورقة عمل Excel.</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="Convert a chart to an image file" rel="noopener">تحويل رسم بياني إلى صورة.</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="Hide a chart legend" rel="noopener">إخفاء أسطورة الرسم البياني في ورقة عمل Excel.</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="Update a chart title" rel="noopener">تحديث عنوان الرسم البياني في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="Delete a chart title" rel="noopener">حذف عنوان الرسم البياني في ورقة عمل Excel.</a></li>
        </ul>
        <p>الجدول</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="Add a table (list object) to a worksheet" rel="noopener">إضافة كائن قائمة في ورقة عمل Excel.</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="Update a table in a worksheet" rel="noopener">تحديث كائن قائمة في ورقة عمل Excel.</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="Convert a table to a range" rel="noopener">تحويل كائن قائمة إلى نطاق.</a></li>
            <li><a href="/cells/sort-table-data/" title="Sort data within a table" rel="noopener">فرز بيانات الجدول.</a></li>
        </ul>
        <p>كائن OLE</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="Add an OLE object to a worksheet" rel="noopener">إضافة كائن OLE في ورقة عمل Excel.</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="Update a specific OLE object" rel="noopener">تحديث كائن OLE معيّن في ورقة عمل Excel.</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="Convert an OLE object to an image" rel="noopener">تحويل كائن OLE إلى صورة.</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="Delete all OLE objects from a worksheet" rel="noopener">حذف جميع كائنات OLE من ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="Delete a specific OLE object" rel="noopener">حذف كائن OLE معيّن في ورقة عمل Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>الشكل</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="Add a shape to a worksheet" rel="noopener">إضافة شكل في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="Delete all shapes from a worksheet" rel="noopener">حذف جميع الأشكال من ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="Delete a shape by its index" rel="noopener">حذف شكل حسب فهرسه في ورقة عمل Excel.</a></li>
        </ul>
        <p>جدول محوري</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="Add a pivot table to a worksheet" rel="noopener">إضافة جدول محوري في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="Delete all pivot tables from a worksheet" rel="noopener">حذف جميع الجداول المحورية من ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="Delete a pivot table by its index" rel="noopener">حذف جدول محوري حسب فهرسه في ورقة عمل Excel.</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="Update cell style in a pivot table" rel="noopener">تحديث نمط خلية في جدول محوري في ورقة عمل Excel.</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="Update the overall style of a pivot table" rel="noopener">تحديث نمط الجدول المحوري في ورقة عمل Excel.</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="Work with pivot table filters" rel="noopener">العمل مع مرشّحات الجدول المحوري في ورقة عمل Excel.</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="Hide a pivot field item" rel="noopener">إخفاء عناصر حقل الجدول المحوري في ورقة عمل Excel.</a></li>
            <li><a href="/cells/move-pivot-table/" title="Move a pivot table within a worksheet" rel="noopener">نقل الجدول المحوري داخل ورقة عمل Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>فاصل الصفحات</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="Insert a horizontal page break" rel="noopener">إدراج فاصل صفحي أفقي في ورقة عمل Excel.</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="Insert a vertical page break" rel="noopener">إدراج فاصل صفحي عمودي في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="Delete a horizontal page break" rel="noopener">حذف فاصل صفحي أفقي في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="Delete a vertical page break" rel="noopener">حذف فاصل صفحي عمودي في ورقة عمل Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>إعدادات الصفحة</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>حساب</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="Calculate all formulas in a workbook" rel="noopener">حساب جميع الصيغ في ملف عمل Excel.</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="Calculate a specific cell's formula" rel="noopener">حساب صيغ خلايا محددة في ملف عمل Excel.</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="Calculate a formula in a worksheet" rel="noopener">حساب صيغة محددة في ورقة عمل Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>الاسم</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>المخطط التفصيلي</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="Group rows in a worksheet" rel="noopener">تجميع صفوف في ورقة عمل Excel.</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="Ungroup rows in a worksheet" rel="noopener">إلغاء تجميع صفوف في ورقة عمل Excel.</a></li>
        </ul>
        <p>الترشيح</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="Add a filter to a column" rel="noopener">إضافة مرشّح لعمود في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="Delete a column filter" rel="noopener">حذف مرشّح لعمود في ورقة عمل Excel.</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="Remove a date filter" rel="noopener">إزالة مرشّح تاريخ في ورقة عمل Excel.</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="Add an icon filter" rel="noopener">إضافة مرشّح أيقونات في ورقة عمل Excel.</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="Add a date filter" rel="noopener">إضافة مرشّح تاريخ في ورقة عمل Excel.</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="Filter data using AutoFilter" rel="noopener">ترشيح البيانات باستخدام الترشيح التلقائي في ورقة عمل Excel.</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="Filter the top 10 items" rel="noopener">ترشيح أفضل 10 عناصر في القائمة في ورقة عمل Excel.</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="Match all blank cells" rel="noopener">تحديد جميع الخلايا الفارغة في القائمة في ورقة عمل Excel.</a></li>
        </ul>
        <p>الفرز</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="Sort worksheet data" rel="noopener">فرز بيانات ورقة العمل في ورقة عمل Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>استيراد البيانات</p>
        <ul>
            <li><a href="/cells/import/" title="Import data into Excel files" rel="noopener">استيراد بيانات إلى ملفات Excel.</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="Import CSV data into a worksheet" rel="noopener">استيراد بيانات CSV إلى ورقة عمل Excel.</a></li>
            <li><a href="/cells/import/picture/" title="Import a picture into a worksheet" rel="noopener">استيراد صورة إلى ورقة عمل Excel.</a></li>
            <li><a href="/cells/import/double-array/" title="Import a double array into a worksheet" rel="noopener">استيراد مصفوفة من نوع double إلى ورقة عمل Excel.</a></li>
            <li><a href="/cells/import/integer-array/" title="Import an integer array into a worksheet" rel="noopener">استيراد مصفوفة أعداد صحيحة إلى ورقة عمل Excel.</a></li>
            <li><a href="/cells/import/string-array/" title="Import a string array into a worksheet" rel="noopener">استيراد مصفوفة سلاسل نصية إلى ورقة عمل Excel.</a></li>
            <li><a href="/cells/import/with-using-storage/" title="Import data using storage" rel="noopener">استيراد بيانات إلى ورقة عمل Excel باستخدام التخزين.</a></li>
            <li><a href="/cells/import/without-using-storage/" title="Import data without using storage" rel="noopener">استيراد بيانات إلى ورقة عمل Excel دون استخدام التخزين.</a></li>
        </ul>
        <p>التصنيف</p>
        <ul>
            <li><a href="/cells/assembly/" title="Assemble data in Excel files" rel="noopener">تجميع البيانات داخل ملفات Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>التعليقات</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="Add a comment to a cell" rel="noopener">إضافة تعليق إلى خلية في ورقة عمل Excel.</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="Update a cell comment" rel="noopener">تحديث تعليق خلية في ورقة عمل Excel.</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="Delete all comments in a worksheet" rel="noopener">حذف جميع التعليقات في ورقة عمل Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>التغييرات</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="Protect an Excel workbook" rel="noopener">حماية ملف عمل Excel.</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="Unprotect an Excel workbook" rel="noopener">إلغاء حماية ملف عمل Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>النوافذ</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="Freeze panes in a worksheet" rel="noopener">تجميد لوحات في ورقة عمل Excel.</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="Unfreeze panes in a worksheet" rel="noopener">إلغاء تجميد لوحات في ورقة عمل Excel.</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="Hide a worksheet" rel="noopener">إخفاء ورقة عمل Excel.</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="Unhide a worksheet" rel="noopener">إظهار ورقة عمل Excel مخفية.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>التكبير</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="Set worksheet zoom level" rel="noopener">ضبط مستوى التكبير في ورقة عمل Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

## {{< /tabs >}}

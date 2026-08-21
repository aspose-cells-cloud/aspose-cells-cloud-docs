---
title: "استيراد بيانات CSV إلى ورقة عمل Excel"
second_title: "Document"
linktitle: "استيراد بيانات CSV"
type: docs
url: /ar/import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "استيراد بيانات CSV، Excel، Aspose.Cells Cloud، REST API، جدول بيانات، استيراد CSV"
description: "تتيح واجهة Aspose.Cells Cloud REST API استيراد بيانات CSV إلى أوراق عمل Excel. تشمل SDKs المدعومة: Android، .NET، Go، Java، Node.js، Perl، PHP، Python، Ruby، وSwift."
weight: 19
---

تُستخدم هذه الواجهة REST API **لاستيراد بيانات CSV** إلى ورقة عمل Excel.

الطلب عبارة عن طلب HTTP يحتوي على محتوى متعدد الأجزاء (انظر [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). الجزء الأول من المحتوى المتعدد الأجزاء يحتوي على بيانات `ImportCSVDataOption`، بينما يحتوي الجزء الثاني على ملف CSV.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

تُوضّح الجداول التالية المعلمات المهمة.

### ImportCSVDataOption

| اسم المعلمة         | النوع                      | الوصف                                                                 |
|---------------------|----------------------------|-----------------------------------------------------------------------|
| SeparatorString     | string                     | الحرف المستخدم لفصل الحقول في ملف CSV (مثل `،` أو `؛`).              |
| ConvertNumericData  | string (`true`/`false`)    | يُشير إلى ما إذا كان يجب تحويل السلاسل الرقمية إلى قيم عددية.        |
| FirstRow            | int                        | المؤشر المبني على 1 لصف أول سطر سيتم وضع البيانات فيه.              |
| FirstColumn         | int                        | المؤشر المبني على 1 لعمود أول عمود سيتم وضع البيانات فيه.           |
| SourceFile          | string                     | اسم ملف CSV المصدر المراد استيراده.                                  |
| CustomParsers       | List\<CustomParserConfig\> | مجموعة إعدادات محللات مخصصة لحقول محددة.                            |

### CustomParserConfig

| اسم المعلمة   | النوع  | الوصف                                                           |
|---------------|--------|-----------------------------------------------------------------|
| ColumnIndex   | int    | المؤشر المبني على الصفر للفهرس العمودي الذي يطبّق عليه المحلل المخصص. |
| ParseMethod   | string | طريقة التحليل للعمود (مثل `ToString`، `ToDate`، `ToNumber`).     |
| CustomStyle   | string | النمط المخصص (مثل تنسيق الأرقام) المطبّق على الخلايا المُحلّلة.   |

**مثال**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                            |
|-------|-----------------------------|------------------------------------------------------------------|
| 200   | OK                          | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.     |
| 400   | Bad Request                 | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).            |
| 401   | Unauthorized                | رمز JWT غير صالح أو مفقود.                                      |
| 413   | Payload Too Large           | حجم الملف المرفوع يتجاوز الحد المسموح به.                       |
| 500   | Internal Server Error       | خطأ داخلي غير متوقع في الخادم.                                  |

## كيفية استخدام واجهة PostImportData API باستخدام SDKs

### مواصفات واجهة PostImportData API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) واجهة برمجة تطبيقات عامة قابلة للوصول، تسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتقوم SDK بتجريد التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على منطق تطبيقك التجاري. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

يوضح مثال الكود التالي كيفية استدعاء خدمة Aspose.Cells عبر الويب باستخدام SDK الخاص بـ PHP:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}
---
title: "استيراد بيانات دُفعات إلى ورقة عمل Excel"
second_title: "مستند"
linktype: "استيراد بيانات دُفعات"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, API سحابية, استيراد بيانات دُفعات, Excel, CSV, JSON, XML, مصفوفات"
description: "تعرّف على كيفية استيراد بيانات دُفعات (CSV و JSON و XML والمصفوفات) إلى ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يشمل المصادقة وأمثلة على الطلبات والاستجابات وأجزاء من كود SDK والتعامل مع الأخطاء."
weight: 19
ArticleTitle: "استيراد بيانات دُفعات إلى ورقة عمل Excel – وثائق Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية **استيراد بيانات دُفعات** إلى ورقة عمل Excel. وتتلقى طلبًا متعدد الأجزاء (multipart)، حيث يحتوي الجزء الأول على كائن **ImportBatchDataOption**، ويحتوي الجزء الثاني على ملف البيانات الفعلي (CSV أو JSON أو XML أو غيرها).

وتستخدم العملية طلب HTTP بمحتوى متعدد الأجزاء (انظر [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## واجهة PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### ImportBatchDataOption

| اسم المعلِمة          | النوع              | الوصف                                                                                                                                                                                                 |
| --------------------- | ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**         | `List<CellValue>`  | مجموعة قيم الخلايا التي ستُكتب مباشرة.                                                                                                                                                                |
| **DestinationWorksheet** | `string`         | اسم ورقة العمل التي ستُستورد إليها البيانات.                                                                                                                                                        |
| **IsInsert**          | `bool`             | عندما تكون القيمة `true`، تُدرج البيانات وتُزاحَم الخلايا الموجودة؛ وعندما تكون القيمة `false`، تُستبدل البيانات الخلايا الموجودة.                                                                   |
| **ImportDataType**    | `string`           | تنسيق البيانات المراد استيرادها. القيم المسموح بها: `IntArray`، `DoubleArray`، `StringArray`، `TwoDimensionIntArray`، `TwoDimensionDoubleArray`، `TwoDimensionStringArray`، `BatchData`، `csvData`. |
| **Source**            | `FileSource`       | يحدد موقع ملف البيانات عندما تكون القيمة **BatchData** `null`.                                                                                                                                       |

### CellValue

| اسم المعلِمة    | النوع    | الوصف                                                         |
| --------------- | -------- | ------------------------------------------------------------- |
| **rowIndex**    | `int`    | فهرس الصف (المرجعي من الصفر) للخلية المستهدفة.               |
| **columnIndex** | `int`    | فهرس العمود (المرجعي من الصفر) للخلية المستهدفة.             |
| **type**        | `string` | نوع البيانات للقيمة (مثل `int` أو `double` أو `string`).     |
| **value**       | `string` | القيمة الفعلية التي ستُكتب في الخلية.                         |
| **style**       | `Style`  | معلومات تنسيق اختيارية للخلية.                                |

### FileSource

| اسم المعلِمة       | النوع    | الوصف                                                                      |
| ------------------ | -------- | -------------------------------------------------------------------------- |
| **FileSourceType** | `string` | مصدر الملف: `InMemoryFiles` أو `CloudFileSystem` أو `RequestFiles`.       |
| **FilePath**       | `string` | مسار الملف أو مُعرِّفه داخل المصدر المختار.                                |

### مثال (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                                                 |
|------|----------------------------|----------------------------------------------------------------------|
| 200  | نجاح                       | تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.            |
| 400  | طلب غير صالح              | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).                 |
| 401  | غير مصرّح به               | رمز JWT غير صالح أو مفقود.                                           |
| 413  | حمل البيانات كبير جدًا      | حجم الملف المرفوع يتجاوز الحد المسموح.                               |
| 500  | خطأ داخلي في الخادم        | خطأ غير متوقع في الخادم.                                             |

## كيفية استخدام واجهة PostImportData مع حزم تطوير البرمجيات (SDKs)

### مواصفات واجهة PostImportData

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) واجهة برمجية عامة يمكن استخدامها لإجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام حزم تطوير البرمجيات (SDKs) لـ Aspose.Cells Cloud

استخدام حزمة تطوير البرمجيات (SDK) هو أسرع طريقة لدمج هذه الوظيفة. فحزم SDK تتعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق عملك. يمكنك الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم Aspose.Cells Cloud SDK.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام حزم SDK مختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
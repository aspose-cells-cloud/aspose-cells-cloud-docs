---
title: "استيراد مصفوفة سلاسل نصية إلى ورقة عمل إكسل – Aspose.Cells Cloud"
second_title: "المستند"
linktitle: "استيراد مصفوفة سلاسل نصية"
type: docs
url: /ar/import-string-array-into-excel-worksheet/
aliases:
  - /ar/import-string-array-into-worksheet/
  - /ar/import-data/string-array/
  - /ar/import/string-array/
keywords: "Aspose.Cells Cloud, استيراد مصفوفة سلاسل نصية, REST API لإكسل, الرفع المتعدد (multipart upload), استيراد بيانات ورقة العمل, SDK السحابي"
description: "تعرّف على كيفية استيراد مصفوفة سلاسل نصية إلى ورقة عمل إكسل باستخدام REST API الخاص بـ Aspose.Cells Cloud (النسخة 3.0). يشمل التنسيق المطلوب في الطلب، المعاملات، وأمثلة SDK."
weight: 40
ArticleTitle: "استيراد مصفوفة سلاسل نصية إلى ورقة عمل إكسل – Aspose.Cells Cloud"
---

استيراد مصفوفة سلاسل نصية إلى ورقة عمل إكسل هو مهمة شائعة عند ملء الجداول ببيانات قائمة مُنظمة. وتُعد هذه العملية مفيدة في سيناريوهات مثل تحميل قيم الإعدادات، أو نقل البيانات من مصادر خارجية، أو تهيئة ورقات العمل بمجموعات محددة مسبقًا من السلاسل النصية.

**المتطلبات المسبقة:**  
- رمز JWT صالح تم الحصول عليه عبر عملية المصادقة في Aspose.Cells Cloud.  
- ملف عمل موجود (أو القدرة على إنشاء واحد) في مساحة التخزين الخاصة بك في Aspose Cloud.  
- إصدار SDK المناسب الذي يدعم نموذج `ImportStringArrayOption`.

تقوم هذه واجهة برمجة التطبيقات (REST API) باستيراد بيانات مصفوفة سلاسل نصية إلى ورقة عمل إكسل.

## واجهة PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معاملات الطلب**

يستخدم الطلب محتوى HTTP متعدد الأجزاء (multipart) (انظر [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
يحتوي الجزء الأول من جسم الطلب المتعدد على حمولة **ImportStringArrayOption**؛ ويحتوي الجزء الثاني على ملف بيانات المصدر.

تُوضّح الجدول التالي المعاملات المهمة:

<caption>معاملات ImportStringArrayOption</caption>
### **ImportStringArrayOption**

| اسم المعاملة         | النوع      | الوصف                                                                                                                                                                                |
| --------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | فهرس الصف الابتدائي (مبنِي على 1) حيث سيتم وضع البيانات.                                                                                                                              |
| FirstColumn          | int        | فهرس العمود الابتدائي (مبنِي على 1) حيث سيتم وضع البيانات.                                                                                                                            |
| IsVertical           | boolean    | `true` لإدراج البيانات عموديًا؛ `false` لإدراجها أفقيًا.                                                                                                                             |
| Data                 | String[]   | المصفوفة النصية المراد استيرادها.                                                                                                                                                    |
| DestinationWorksheet | string     | اسم ورقة العمل التي ستتلقى البيانات.                                                                                                                                                 |
| IsInsert             | boolean    | `true` لإدراج صفوف/أعمدة (نقل الخلايا الحالية)؛ `false` لكتابة البيانات فوق الخلايا الموجودة.                                                                                      |
| ImportDataType       | string     | نوع البيانات قيد الاستيراد (مثل `IntArray`، `DoubleArray`، `StringArray`، `TwoDimensionIntArray`، `TwoDimensionDoubleArray`، `TwoDimensionStringArray`، `BatchData`، `csvData`).     |
| Source               | FileSource | يصف مكان وجود ملف البيانات عندما تكون قيمة **BatchData** فارغة (مثل `CloudFileSystem`، `LocalFile`). مطلوب إذا لم تُقدَّم قيمة `BatchData`.                                          |

### مثال

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### الاستجابة

يُعيد الطلب الناجح رمز الحالة **HTTP 200** مع حمولة JSON مشابهة لما يلي:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

رموز الحالة الممكنة:

| الكود | المعنى                                   |
| ----- | ----------------------------------------- |
| 200   | تم الاستيراد بنجاح                        |
| 400   | طلب غير صالح – بيانات مفقودة أو غير صحيحة |
| 401   | غير مصرّح به – رمز غير صالح أو مفقود      |
| 500   | خطأ داخلي في الخادم                        |


## كيفية استخدام واجهة PostImportData API مع SDKs

### مواصفات واجهة PostImportData API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) واجهة برمجة تطبيقات متاحة للعامة وتسمح لك بإجراء تفاعلات REST مباشرة من خلال متصفح الويب.

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. فتتولى SDK التعامل مع التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---
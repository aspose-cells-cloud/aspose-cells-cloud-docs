---
title: تصدير المصنفات والعناصر الداخلية إلى أنواع الشكل
second_title: Aspose.Cells Cloud Documen
linktitle: إكسبور
type: docs
url: /ar/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API يدعم تصدير ملف Excel وكائنات داخلية لأنواع ملفات النسق. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 31
---
 إذا قمت في الأصل بإنشاء ملف Excel بتنسيق معين ، مثل[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) ، و[CSV](https://docs.fileformat.com/spreadsheet/csv/) ، قد تجد أحيانًا أنه من المفيد تحويل ملف Excel إلى تنسيق آخر حتى تتمكن من الاستفادة من الميزات الخاصة التي يوفرها. على سبيل المثال ، قد ترغب في تصدير ملف Excel إلى[PDF](https://docs.fileformat.com/pdf/) لحماية محتوياتك من أي تعديلات غير مصرح بها وتسهيل قراءتها ومشاركتها في وقت واحد.

 Excel تصدير العنصر هو عملية معقدة. تساهم العديد من العوامل في التعقيد ، وبالتالي ، يجب أخذها في الاعتبار أثناء عملية التصدير. تعد القدرة على تصدير عنصر Excel إلى ملف تنسيق واحد بجودة احترافية دقيقة من أهم ميزات Aspose.Cells Cloud.

 إنه يعمل بشكل مثالي مع المصنف والرسم البياني والشكل والصورة التي تم تصديرها من ملف Excel. يمكنك تصدير التنسيقات:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [ملف TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [المواد المستنفدة للأوزون](https://docs.fileformat.com/spreadsheet/ods/), [رسالة قصيرة](https://docs.fileformat.com/word-processing/txt/) . تنسيقات التصدير فقط:[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [أعداد](https://docs.fileformat.com/spreadsheet/numbers/), [فودس](https://docs.fileformat.com/spreadsheet/fods/).

الطلب عبارة عن طلب HTTP بمحتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على ملف البيانات والثاني يحتوي على خيارات الحفظ.

مصنف REST API `export` والكائنات الداخلية لملف تنسيق مختلف.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| ملف| ملف| بيانات النموذج| ملف للتحميل|
| نوع الكائن| خيط| استفسار|نوع الكائن (مصنف / ورقة عمل / مخطط / شكل / صورة / كائن قائمة / كائن أولي)|
| شكل| خيط| استفسار|[تنسيق الملف](/cells/ar/supported-file-formats/)  |
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
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
 
## عائلة Cloud SDK


 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export.php" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LiteCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


تشرح المقالات التالية كل API بالتفصيل وتحتوي على cURL و SDK أمثلة لكل API:


1. [تصدير مخطط Excel إلى تنسيق ملف مختلف](/cells/ar/export/excel-chart-to-different-formats/)
2. [تصدير Excel عنصر قائمة إلى تنسيق ملف مختلف](/cells/ar/export/excel-listobject-to-different-formats/)
3. [تصدير Excel كائن أول إلى تنسيق ملف مختلف](/cells/ar/export/excel-ole-object/)
4. [تصدير Excel صورة إلى تنسيق ملف مختلف](/cells/ar/export/excel-picture-to-different-formats/)
5. [تصدير شكل Excel إلى تنسيق ملف مختلف](/cells/ar/export/excel-shape-to-different-formats/)
6. [تصدير Excel مصنف إلى تنسيق ملف مختلف](/cells/ar/export/excel-to-different-formats/)
7. [تصدير Excel ورقة العمل إلى تنسيق ملف مختلف](/cells/ar/export/excel-worksheet-to-different-formats//)

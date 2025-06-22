---
title: احصل على عقار Cells
type: docs
url: /ar/get-cells-properties/
weight: 130
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، احصل على خصائص Cells
---
يوضح هذا REST API كيفية `get a specific cell` في ملف Excel.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم الوثيقة.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| اسم الخلية أو الطريقة| خيط| طريق|اسم الخلية أو الطريقة. (قيمة اسم الطريقة: firstcell، endcell، maxrow، maxdatarow، maxcolumn، maxdatacolumn، minrow، mindatarow، mincolumn، mindatacolumn، cellName).|
| مجلد| خيط| استفسار| مجلد المستند.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### **عائلة SDK السحابية**

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### **كيفية الحصول على خلية محددة**

- [الحصول على بيانات الخلية من ورقة عمل](/cells/ar/get-cell-data-from-a-worksheet/)
- [احصل على الخلية الأولى من ورقة العمل Excel](/cells/ar/get-first-cell-from-excel-worksheet/)
- [احصل على الخلية الأخيرة من ورقة العمل Excel](/cells/ar/get-last-cell-of-excel-worksheet/)
- [احصل على MaxRow من ورقة العمل Excel](/cells/ar/get-maxrow-from-excel-worksheet/)
- [احصل على MaxDataRow من ورقة العمل Excel](/cells/ar/get-maxdatarow-from-excel-worksheet/)
- [احصل على MaxColumn من ورقة العمل Excel](/cells/ar/get-maxcolumn-from-excel-worksheet/)
- [احصل على MaxDataColumn من ورقة العمل Excel](/cells/ar/get-maxdatacolumn-from-excel-worksheet/)
- [احصل على MinRow من ورقة العمل Excel](/cells/ar/get-minrow-from-excel-worksheet/)
- [احصل على MinDataRow من ورقة العمل Excel](/cells/ar/get-mindatarow-from-excel-worksheet/)
- [احصل على MinColumn من ورقة العمل Excel](/cells/ar/get-mincolumn-from-excel-worksheet/)
- [احصل على MinDataColumn من ورقة العمل Excel](/cells/ar/get-mindatacolumn-from-excel-worksheet/)

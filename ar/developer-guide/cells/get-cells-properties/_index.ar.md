---
title: احصل على Cells من الممتلكات
type: docs
url: /ar/get-cells-properties/
weight: 130
---
يشير هذا REST API إلى كيفية `get a specific cell` في ملف Excel.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم الملف.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| cellOrMethodName| خيط| طريق|اسم الخلية أو الطريقة. (قيمة اسم الطريقة: firstcell و endcell و maxrow و maxdatarow و maxcolumn و maxdatacolumn و minrow و mindatarow و mincolumn و mindatacolumn و cellName.)|
| مجلد| خيط| استفسار| مجلد المستند.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.


- **كيفية الحصول على خلية معينة**

   - [احصل على بيانات الخلية من ورقة عمل](/cells/ar/get-cell-data-from-a-worksheet/)
   - [احصل على الخلية الأولى من ورقة عمل Excel](/cells/ar/get-first-cell-from-excel-worksheet/)
   - [احصل على الخلية الأخيرة من ورقة عمل Excel](/cells/ar/get-last-cell-of-excel-worksheet/)
   - [احصل على MaxRow من ورقة عمل Excel](/cells/ar/get-maxrow-from-excel-worksheet/)
   - [احصل على MaxDataRow من ورقة عمل Excel](/cells/ar/get-maxdatarow-from-excel-worksheet/)
   - [احصل على MaxColumn من ورقة عمل Excel](/cells/ar/get-maxcolumn-from-excel-worksheet/)
   - [احصل على MaxDataColumn من ورقة عمل Excel](/cells/ar/get-maxdatacolumn-from-excel-worksheet/)
   - [احصل على MinRow من ورقة عمل Excel](/cells/ar/get-minrow-from-excel-worksheet/)
   - [احصل على MinDataRow من ورقة عمل Excel](/cells/ar/get-mindatarow-from-excel-worksheet/)
   - [احصل على MinColumn من ورقة عمل Excel](/cells/ar/get-mincolumn-from-excel-worksheet/)
   - [احصل على MinDataColumn من ورقة عمل Excel](/cells/ar/get-mindatacolumn-from-excel-worksheet/)

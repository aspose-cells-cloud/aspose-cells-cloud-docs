---
title: "العمل مع مخططات إكسل"
second_title: "الوثيقة"
linktype: "المخططات"
type: docs
url: /ar/charts/
aliases: [  /ar/working-with-charts/ ]
keywords: "Aspose, Cells, Excel, مخطط, API, REST, سحابة, جدول بيانات"
description: "تعرّف على كيفية إدارة مخططات إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells السحابية. دلائل خطوة بخطوة وأمثلة على الأكواد ومعالجة الأخطاء لاسترجاع المخططات وإضافتها وتحديثها وحذفها وتحويلها إلى صور."
weight: 100
ArticleTitle: "العمل مع مخططات إكسل – وثائق Aspose.Cells السحابية"
---

## العمل مع المخططات في ملف إكسل

**آخر تحديث:** يوليو 2026  

تمثل مخططات إكسل تمثيلات مرئية للبيانات، مما يساعد المستخدمين على فهم الاتجاهات والأنماط بسرعة.  
تمكن واجهة برمجة تطبيقات Aspose.Cells السحابية المطورين من العمل مع هذه المخططات برمجيًا داخل كتب عمل إكسل المخزَّنة في السحابة. باستخدام هذه الواجهة، يمكنك استرجاع المخططات الموجودة، وإضافة مخططات جديدة، وتعديل خصائصها (مثل العناوين والمحاور والأساطير)، وحذف المخططات غير المرغوب فيها، وتحويل المخططات إلى صيغ صور لغرض إعداد التقارير أو المعالجة اللاحقة. تُوفّر الروابط التالية وصولًا مباشرًا إلى صفحات العمليات التفصيلية لكل إجراء مدعوم مرتبط بالمخططات.

### مرجع سريع

| العملية | طريقة HTTP | نقطة النهاية (قالب) | الوثائق |
|---------|------------|---------------------|---------|
| استرجاع المخطط | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [استرجاع مخطط من ورقة عمل](/cells/get-chart-from-a-worksheet/) |
| إضافة مخطط | POST | `/cells/{file}/worksheets/{sheet}/charts` | [إضافة مخطط في ورقة عمل](/cells/add-a-chart-in-a-worksheet/) |
| حذف جميع المخططات | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [حذف جميع المخططات من ورقة عمل](/cells/delete-all-charts-from-a-worksheet/) |
| حذف مخطط | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [حذف مخطط من ورقة عمل](/cells/delete-a-chart-from-a-worksheet/) |
| تحويل المخطط إلى صورة | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [تحويل المخطط إلى صورة](/cells/convert-chart-to-image/) |
| استرجاع منطقة المخطط | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [استرجاع منطقة المخطط من ورقة عمل](/cells/get-chart-area-from-a-worksheet/) |
| استرجاع تنسيق التعبئة | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [استرجاع تنسيق التعبئة لمنطقة المخطط من ورقة عمل](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| استرجاع الأسطورة | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [استرجاع أسطورة المخطط من ورقة عمل](/cells/get-chart-legend-from-a-worksheet/) |
| تحديث الأسطورة | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [تحديث أسطورة المخطط في ورقة عمل](/cells/update-chart-legend-in-a-worksheet/) |
| إظهار الأسطورة | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [إظهار أسطورة المخطط في ورقة عمل](/cells/show-chart-legend-in-a-worksheet/) |
| إخفاء الأسطورة | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [إخفاء أسطورة المخطط في ورقة عمل](/cells/hide-chart-legend-in-a-worksheet/) |
| استرجاع العنوان | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [استرجاع عنوان المخطط من ورقة عمل](/cells/get-chart-title-from-a-worksheet/) |
| تحديد العنوان | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [تحديد عنوان المخطط في ورقة عمل إكسل](/cells/set-chart-title-in-excel-worksheet/) |
| تحديث العنوان | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [تحديث عنوان المخطط في ورقة عمل إكسل](/cells/update-chart-title-in-excel-worksheet/) |
| حذف العنوان | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [حذف عنوان المخطط في ورقة عمل](/cells/delete-chart-title-in-a-worksheet/) |
| تحديث خصائص المخطط | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [تحديث خصائص المخطط](/cells/charts/properties/update/) |
| استرجاع المحور التصنيفي | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [استرجاع المحور التصنيفي للمخطط](/cells/charts/category-axis/get/) |
| استرجاع المحور القيمي | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [استرجاع المحور القيمي للمخطط](/cells/charts/value-axis/get/) |
| استرجاع المحور التصنيفي الثاني | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [استرجاع المحور التصنيفي الثاني للمخطط](/cells/charts/second-category-axis/get/) |
| استرجاع المحور القيمي الثاني | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [استرجاع المحور القيمي الثاني للمخطط](/cells/charts/second-value-axis/get/) |
| تحديث المحور التصنيفي | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [تحديث المحور التصنيفي للمخطط](/cells/charts/category-axis/update/) |
| تحديث المحور القيمي | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [تحديث المحور القيمي للمخطط](/cells/charts/value-axis/update/) |
| تحديث المحور التصنيفي الثاني | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [تحديث المحور التصنيفي الثاني للمخطط](/cells/charts/second-category-axis/update/) |
| تحديث المحور القيمي الثاني | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [تحديث المحور القيمي الثاني للمخطط](/cells/charts/second-value-axis/update/) |

- [استرجاع مخطط من ورقة عمل](/cells/get-chart-from-a-worksheet/)
- [إضافة مخطط في ورقة عمل](/cells/add-a-chart-in-a-worksheet/)
- [حذف جميع المخططات من ورقة عمل](/cells/delete-all-charts-from-a-worksheet/)
- [حذف مخطط من ورقة عمل](/cells/delete-a-chart-from-a-worksheet/)
- [تحويل المخطط إلى صورة](/cells/convert-chart-to-image/)
- [استرجاع منطقة المخطط من ورقة عمل](/cells/get-chart-area-from-a-worksheet/)
- [استرجاع تنسيق التعبئة لمنطقة المخطط من ورقة عمل](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [استرجاع أسطورة المخطط من ورقة عمل](/cells/get-chart-legend-from-a-worksheet/)
- [تحديث أسطورة المخطط في ورقة عمل](/cells/update-chart-legend-in-a-worksheet/)
- [إظهار أسطورة المخطط في ورقة عمل](/cells/show-chart-legend-in-a-worksheet/)
- [إخفاء أسطورة المخطط في ورقة عمل](/cells/hide-chart-legend-in-a-worksheet/)
- [استرجاع عنوان المخطط من ورقة عمل](/cells/get-chart-title-from-a-worksheet/)
- [تحديد عنوان المخطط في ورقة عمل إكسل](/cells/set-chart-title-in-excel-worksheet/)
- [تحديث عنوان المخطط في ورقة عمل إكسل](/cells/update-chart-title-in-excel-worksheet/)
- [حذف عنوان المخطط في ورقة عمل](/cells/delete-chart-title-in-a-worksheet/)
- [تحديث خصائص المخطط](/cells/charts/properties/update/)
- [استرجاع المحور التصنيفي للمخطط](/cells/charts/category-axis/get/)
- [استرجاع المحور القيمي للمخطط](/cells/charts/value-axis/get/)
- [استرجاع المحور التصنيفي الثاني للمخطط](/cells/charts/second-category-axis/get/)
- [استرجاع المحور القيمي الثاني للمخطط](/cells/charts/second-value-axis/get/)
- [تحديث المحور التصنيفي للمخطط](/cells/charts/category-axis/update/)
- [تحديث المحور القيمي للمخطط](/cells/charts/value-axis/update/)
- [تحديث المحور التصنيفي الثاني للمخطط](/cells/charts/second-category-axis/update/)
- [تحديث المحور القيمي الثاني للمخطط](/cells/charts/second-value-axis/update/)
---
---
title: "العمل مع صفوف ملفات إكسل – واجهة Aspose.Cells Cloud API"
ArticleTitle: "العمل مع صفوف ملفات إكسل – واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktype: "docs"
url: /rows/
aliases: [/working-with-rows/]
keywords: "Aspose.Cells, صفوف إكسل, واجهة REST API, تعديل جداول البيانات"
description: "قم بتعديل الصفوف في ملفات إكسل باستخدام واجهة Aspose.Cells Cloud REST API. يدعم منصات أندرويد، C#، Go، Java، Node.js، Perl، PHP، Python، Ruby، و Swift."
weight: 100
---

## العمل مع الصفوف في ملف إكسل

**آخر تحديث: يوليو 2026**

- [كيفية الحصول على معلومات الصف في ورقة عمل إكسل.](/cells/rows/get/row/)
- [كيفية إضافة صف فارغ في ورقة عمل إكسل.](/cells/rows/add/row/)
- [كيفية نسخ صفوف في ورقة عمل إكسل.](/cells/rows/copy/)
- [كيفية إخفاء صفوف في ورقة عمل إكسل.](/cells/rows/hide/)
- [كيفية إظهار الصفوف المخفية في ورقة عمل إكسل.](/cells/rows/unhide/)
- [كيفية تجميع الصفوف في ورقة عمل إكسل.](/cells/rows/group/)
- [كيفية إلغاء تجميع الصفوف في ورقة عمل إكسل.](/cells/rows/ungroup/)
- [كيفية حذف صف من ورقة العمل](/cells/rows/delete/)

مرجع سريع لواجهة API للعمليات الشائعة على الصفوف:

| العملية | طريقة HTTP | نقطة النهاية | المعلمات الرئيسية |
|---------|-----------|-------------|------------------|
| [الحصول على صف](https://docs.aspose.cloud/cells/rows/get/row/) | GET | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}` | `fileName`, `sheetName`, `rowIndex` |
| [إضافة صف](https://docs.aspose.cloud/cells/rows/add/row/) | POST | `/cells/{fileName}/worksheets/{sheetName}/rows` | `rowIndex`, `height` |
| [نسخ الصفوف](https://docs.aspose.cloud/cells/rows/copy/) | POST | `/cells/{fileName}/worksheets/{sheetName}/rows/copy` | `sourceIndex`, `destinationIndex`, `rowCount` |
| [حذف صف](https://docs.aspose.cloud/cells/rows/delete/) | DELETE | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}` | `fileName`, `sheetName`, `rowIndex` |
| [إخفاء الصفوف](https://docs.aspose.cloud/cells/rows/hide/) | POST | `/cells/{fileName}/worksheets/{sheetName}/rows/hide` | `startIndex`, `endIndex` |
| [إظهار الصفوف المخفية](https://docs.aspose.cloud/cells/rows/unhide/) | POST | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide` | `startIndex`, `endIndex` |
| [تجميع الصفوف](https://docs.aspose.cloud/cells/rows/group/) | POST | `/cells/{fileName}/worksheets/{sheetName}/rows/group` | `startIndex`, `endIndex` |
| [إلغاء تجميع الصفوف](https://docs.aspose.cloud/cells/rows/ungroup/) | POST | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup` | `startIndex`, `endIndex` |

**تفاصيل الطلب والاستجابة**

- **الحصول على صف**  
  *الطلب*: لا يوجد محتوى مطلوب.  
  *الاستجابة (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *الأخطاء*: 400 Bad Request (مؤشر غير صالح)، 404 Not Found (ملف أو ورقة مفقودة).

- **إضافة صف**  
  *محتوى الطلب (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *الاستجابة (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *الأخطاء*: 400 Bad Request (معلمات مفقودة أو غير صالحة)، 401 Unauthorized.

- **نسخ الصفوف**  
  *محتوى الطلب (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *الاستجابة (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *الأخطاء*: 400 Bad Request، 404 Not Found.

- **حذف صف**  
  *الطلب*: لا يوجد محتوى.  
  *الاستجابة (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *الأخطاء*: 400 Bad Request، 404 Not Found.

- **إخفاء الصفوف**  
  *محتوى الطلب (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *الاستجابة (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *الأخطاء*: 400 Bad Request.

- **إظهار الصفوف المخفية** – نفس محتوى الطلب مثل *إخفاء الصفوف*؛ الاستجابة متماثلة، والحالة تكون "Rows unhidden".

- **تجميع الصفوف** – نفس محتوى الطلب مثل *إخفاء الصفوف*؛ حالة الاستجابة تكون "Rows grouped".

- **إلغاء تجميع الصفوف** – نفس محتوى الطلب مثل *إخفاء الصفوف*؛ حالة الاستجابة تكون "Rows ungrouped".

تتطلب جميع العمليات رمز وصول ساري لبروتوكول OAuth 2.0/JWT وإصدارًا مناسبًا من مكتبة SDK.

---
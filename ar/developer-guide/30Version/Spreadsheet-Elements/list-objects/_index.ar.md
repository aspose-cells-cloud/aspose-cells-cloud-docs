---
title: "العمل مع كائن ListObject في Excel"
ArticleTitle: "العمل مع كائن ListObject في Excel"
second_title: "المستند"
linktype: "ListObjects"
type: docs
url: /ar/list-objects/
aliases:
  - /ar/working-with-list-objects/
  - /ar/working-with-list-object-or-table/
keywords: "Aspose.Cells, كائن ListObject في Excel, واجهة برمجة تطبيقات جداول Excel, إضافة جدول, تحديث جدول, حذف جدول, تحويل الجدول إلى نطاق, فرز جدول Excel"
description: "تعرّف على كيفية إضافة وتحديث وحذف واسترجاع وفرز وتحويل كائنات ListObject (الجداول) في Excel باستخدام واجهة Aspose.Cells Cloud REST API. تتضمن أمثلة كود بلغات C# وJava وPython وما إلى ذلك."
weight: 100
---

توفر كائنات ListObject (الجداول) في Excel طريقة منظمة لتنظيم مجموعات البيانات. وتشمل ميزات مثل تنظيم البيانات تلقائيًا، وصفوف الرؤوس، وفلاتر مدمجة، وصفوف مجموعات اختيارية. اتقن هذه القدرات لتحليل بياناتك بسرعة وكفاءة.

**تعريف ListObject:** كائن **ListObject** هو كائن الجدول الأصلي في Excel الذي يجمع الصفوف والأعمدة، ويتيح الفرز والتصفية والتنسيق، ويمكن الوصول إليه عبر واجهة Aspose.Cells Cloud API.

## كيفية العمل مع الجدول (كائن List)

- [كيفية إضافة جدول (كائن List) داخل ورقة العمل](/ar/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [كيفية تحديث جدول (كائن List) داخل ورقة العمل](/ar/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [كيفية تحويل جدول (كائن List) إلى نطاق](/ar/cells/convert-list-object-or-table-to-range/)
- [كيفية فرز بيانات الجدول](/ar/cells/sort-table-data/)
- [كيفية إزالة الصفوف المكرّرة من الجدول](/ar/cells/list-objects/remove-duplicates/)
- [كيفية إدراج عامل تصفية مُبسّط (Slicer) للجدول](/ar/cells/list-objects/insert-slicer/)

**مرجع API (نظرة عامة):**  
تقدم واجهة Aspose.Cells Cloud REST API عمليات ListObject من خلال نقاط نهاية مثل `GET /cells/{fileName}/worksheets/{sheetName}/listobjects` و`POST /cells/{fileName}/worksheets/{sheetName}/listobjects` و`PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` و`DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. وتشمل معلمات الاستعلام المطلوبة `folder` (مطلوبة) و`storage` (اختيارية). وتحتوي أجسام الطلبات على كائنات JSON تصف خصائص الجدول (الاسم، ووجود صف الرؤوس، ووجود صف المجموعات، إلخ)، بينما تُعيد الاستجابات أحمال JSON تحتوي على تفاصيل ListObject التي تم إنشاؤها أو تعديلها.

**المتطلبات المسبقة:**  
- رمز مصادقة صالح لـ Aspose.Cells Cloud.  
- يجب رفع ملف مصنف Excel إلى موقع تخزين مدعوم (الافتراضي: **/**)، ويجب أن تشير معلمة الاستعلام `folder` إلى هذا الموقع.  
- اختياري: اضبط `storage` إذا كنت تستخدم خدمة تخزين غير افتراضية.

**تفاصيل نقاط النهاية**

| الطريقة | نقطة النهاية | معلمات الاستعلام | جسم الطلب (JSON) | استجابة النجاح (مثال) | رموز الحالة |
|--------|----------|------------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (مطلوبة)، `storage` (اختيارية) | *لا شيء* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – ناجح، 400 – طلب غير صالح، 401 – غير مُصرّح، 404 – غير موجود |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (مطلوبة)، `storage` (اختيارية) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – تم الإنشاء، 400 – طلب غير صالح، 401 – غير مُصرّح، 409 – تضارب |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (مطلوبة)، `storage` (اختيارية) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – ناجح، 400 – طلب غير صالح، 401 – غير مُصرّح، 404 – غير موجود |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (مطلوبة)، `storage` (اختيارية) | *لا شيء* | `{ "Code": 200, "Status": "Deleted" }` | 200 – ناجح، 400 – طلب غير صالح، 401 – غير مُصرّح، 404 – غير موجود |

**مقتطفات كود**

*C# (POST – إضافة ListObject)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – استرجاع ListObjects)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – تحديث ListObject)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – إزالة ListObject)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**ملاحظات:**  
- تبدأ فهارس ListObject من الصفر.  
- عند إضافة ListObject، تحدّد `StartRow` و`StartColumn` الخلية العلوية اليسرى للجدول.  
- تدعم الواجهة الترقيم الصفحي عبر معلمتَي الاستعلام `offset` و`limit` (غير مذكورَين في الجدول) للورقات الكبيرة.  
- حدود معدل الطلبات: 100 طلب في الدقيقة لكل حساب؛ ويُعيد تجاوز هذا الحد رمز الحالة **429 Too Many Requests**.

من خلال تضمين مصطلح **Excel ListObject** عدة مرات في الصفحة، يتوافق المحتوى مع الكلمات المفتاحية المستهدفة مثل "Excel ListObject" و"Aspose.Cells Cloud" و"واجهة برمجة تطبيقات جداول Excel"، مما يحسّن محركات البحث (SEO) مع الحفاظ على طبيعة طبيعية للقراء.
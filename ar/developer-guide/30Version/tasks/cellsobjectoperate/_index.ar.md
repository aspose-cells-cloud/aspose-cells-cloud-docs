---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – العمل مع مهمة CellsObjectOperate (REST)"
second_title: "مستند"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "تعرّف على كيفية استخدام مهمة CellsObjectOperate في واجهة برمجة تطبيقات Aspose.Cells Cloud عبر مرجع المعلمات وأمثلة الطلبات/الاستجابات ونصائح الممارسات المثلى للورقات والرسوم البيانية وجداول البيانات المقطعية."
weight: 20
ArticleTitle: "واجهة برمجة تطبيقات Aspose.Cells Cloud – العمل مع مهمة CellsObjectOperate (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "مهمة CellsObjectOperate"
  - "واجهة برمجة تطبيقات Aspose.Cells Cloud"
  - "واجهة برمجة تطبيقات Excel REST"
  - "عملية الرسم البياني"
  - "واجهة برمجة تطبيقات جدول البيانات المقطعية"
  - "واجهة برمجة تطبيقات فاصل الصفحات"
---

**نظرة عامة**  
تتيح لك مهمة **CellsObjectOperate** تنفيذ عمليات إنشاء وقراءة وتحديث وحذف (CRUD) على كائنات Excel مثل كتب العمل والورقات والرسوم البيانية وجداول البيانات المقطعية والأشكال وفاصلات الصفحات وغيرها عبر طلب REST واحد. حدد نوع الكائن باستخدام `OperateObjectType` ووفّر كتلة المعلمات المقابلة (مثل `ChartOperateParameter` للإجراءات المتعلقة بالرسوم البيانية).

---

**OperateObject**

| اسم المعلِم            | النوع  | الوصف |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | نص    | نوع كائن Excel الذي سيتم تنفيذ العملية عليه. القيم المسموحة: `Workbook`، `Worksheet`، `PageSetup`، `Cells`، `Chart`، `Shape`، `ListObject`، `PivotTable`، `WorkbookSettings`، `PageBreak`. |
| OperateObjectPosition   | كائن   | الحاوية التي تحدّد موقع الكائن المستهدف (مثل اسم كتاب العمل أو اسم الورقة أو فهرس الرسم البياني). مطلوبة في معظم العمليات. |

**OperateObjectPosition**

| اسم المعلِم     | النوع  | الوصف |
| -------------- | ------ | ----------- |
| Workbook       | كائن   | كتاب العمل الذي يحتوي على الكائن المستهدف. يجب أن يتضمّن إما `FileName` (لتخزين السحابة) أو `FileContent` (بصيغة مشفرة بـ base‑64). |
| SheetName      | نص     | اسم الورقة التي سيتم تطبيق العملية عليها. مطلوبة لكائنات مستوى الورقة (مثل الرسوم البيانية والأشكال). |
| ChartIndex     | عدد صحيح | الفهرس الصفري لرسم بياني داخل الورقة (يُستخدم عندما تكون قيمة `OperateObjectType` تساوي `Chart`). |
| ShapeIndex     | عدد صحيح | الفهرس الصفري للشكل داخل الورقة (يُستخدم عندما تكون قيمة `OperateObjectType` تساوي `Shape`). |
| CellName       | نص     | مرجع الخلية بنظام A1 (مثل `A1`). تُستخدم في عمليات مستوى الخلية. |
| ListObjectIndex| عدد صحيح | الفهرس الصفري لكائن القائمة (يُستخدم عندما تكون قيمة `OperateObjectType` تساوي `ListObject`). |

**ChartOperateParameter**

| اسم المعلِم           | النوع  | الوصف |
| --------------------- | ------ | ----------- |
| ChartIndex            | عدد صحيح | فهرس الرسم البياني المراد تعديله. مطلوب عند تحديث رسم بياني موجود. |
| ChartType             | نص     | نوع الرسم البياني المراد إنشاؤه (مثل `Bar` أو `Line` أو `Pie`). |
| UpperLeftRow          | عدد صحيح | رقم الصف للزاوية العلوية اليسرى للرسم البياني (صفري). |
| UpperLeftColumn       | عدد صحيح | رقم العمود للزاوية العلوية اليسرى للرسم البياني (صفري). |
| LowerRightRow         | عدد صحيح | رقم الصف للزاوية السفلية اليمنى للرسم البياني. |
| LowerRightColumn      | عدد صحيح | رقم العمود للزاوية السفلية اليمنى للرسم البياني. |
| Area                  | نص     | النطاق البياناتي للرسم البياني (مثل `A1:B5`). |
| IsVertical            | نص     | `true` إذا كان اتجاه الرسم البياني رأسيًا؛ و`false` خلاف ذلك. |
| CategoryData          | نص     | النطاق الذي يوفّر تسميات المحور السيني (محور الفئات). |
| IsAutoGetSerialName   | نص     | `true` لتوليد أسماء المتسلسلات تلقائيًا؛ `false` لاستخدام أسماء مخصصة. |
| Title                 | نص     | نص العنوان المعروض على الرسم البياني. |

**ListObjectOperateParameter**

| اسم المعلِم     | النوع  | الوصف |
| -------------- | ------ | ----------- |
| ListObject     | كائن   | كائن التكوين لعملية القائمة (الجدول). يتضمّن خصائص مثل `ShowHeader` و`ShowTotal` و`Style`. |

**PageBreakOperateParameter**

| اسم المعلِم     | النوع  | الوصف |
| -------------- | ------ | ----------- |
| PageBreakType  | نص     | نوع فاصل الصفحات (`Horizontal` أو `Vertical`). |
| Index          | عدد صحيح | الفهرس الصفري لفاصل الصفحات المراد حذفه أو تعديله. |
| Row            | عدد صحيح | رقم الصف الذي يُوضع فيه فاصل الصفحات الأفقي. |
| Column         | عدد صحيح | رقم العمود الذي يُوضع فيه فاصل الصفحات العمودي. |
| StartIndex     | عدد صحيح | الفهرس الابتدائي لعملية فاصل الصفحات القائمة على النطاق. |
| EndIndex       | عدد صحيح | الفهرس النهائي لعملية فاصل الصفحات القائمة على النطاق. |

**PageSetupOperateParameter**

| اسم المعلِم     | النوع  | الوصف |
| -------------- | ------ | ----------- |
| PageSetup      | كائن   | الإعدادات الخاصة بتنسيق الصفحة (الهوامش والاتجاه وحجم الورقة وما إلى ذلك). |

**PivotTableOperateParameter**

| اسم المعلِم       | النوع        | الوصف |
| ---------------- | ----------- | ----------- |
| DestCellName     | نص          | الخلية العلوية اليسرى لنطاق وجهة جدول البيانات المقطعية (مثل `C5`). |
| SourceData       | نص          | النطاق المصدر لجدول البيانات المقطعية (مثل `A1:D100`). |
| TableName        | نص          | الاسم المُسنَد لجدول البيانات المقطعية الذي تم إنشاؤه. |
| UseSameSource    | نص          | `true` لإعادة استخدام النطاق المصدر الحالي؛ `false` لإنشاء نطاق جديد. |
| PivotTableIndex  | عدد صحيح     | فهرس جدول البيانات المقطعية المراد تحديثه (مطلوبة لإجراءات التعديل والحذف). |
| PivotFieldRows   | عدد صحيح[]   | مجموعة فهارس الحقول التي ستظهر في منطقة الصفوف. |
| PivotFieldColumns| عدد صحيح[]   | مجموعة فهارس الحقول التي ستظهر في منطقة الأعمدة. |
| PivotFieldData   | عدد صحيح[]   | مجموعة فهارس الحقول التي ستظهر في منطقة البيانات. |

**ShapeOperateParameter**

| اسم المعلِم     | النوع  | الوصف |
| -------------- | ------ | ----------- |
| Shape          | كائن   | تعريف الشكل (النوع والموقع والحجم والنص وما إلى ذلك). |

**WorkbookSettingsOperateParameter**

| اسم المعلِم       | النوع  | الوصف |
| ---------------- | ------ | ----------- |
| WorkbookSettings | كائن   | الإعدادات التي تؤثّر على كتاب العمل كاملاً (مثل وضع الحساب والدقة). |

**WorksheetOperateParameter**

| اسم المعلِم     | النوع  | الوصف |
| -------------- | ------ | ----------- |
| Name           | نص     | الاسم الحالي للورقة المراد تنفيذ العملية عليها. |
| SheetType      | نص     | نوع الورقة (`Worksheet` أو `Chart` وما إلى ذلك). |
| NewName        | نص     | الاسم الجديد للورقة عند إعادة تسميتها. |
| MovingRequest  | كائن   | معلمات نقل الورقة (مثل `FromIndex` و`ToIndex`). |

## واجهة برمجة تطبيقات REST

| API                | النوع | الوصف | رابط المورد |
| ------------------ | ---- | ----------- | ------------- |
| /cells/task/runtask| POST | تشغيل المهمة | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### المتطلبات الأساسية
- **المصادقة** – تضمين رأس `Authorization: Bearer <access_token>` صالح.  
- **التخزين** – يجب أن يكون كتاب العمل المصدر مخزنًا في تخزين Aspose Cloud أو يُقدّم كمحتوى مشفر بـ base‑64 في جسم الطلب.  
- **إصدار واجهة برمجة التطبيقات** – يستهدف هذا المستند إصدار **v3.0** من واجهة برمجة تطبيقات Aspose.Cells Cloud.

### مثال على طلب (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

يتّبع جسم الطلب المخطط المعرّف أدناه باسم **CellsObjectOperateRequest**:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* تم حذف التعريفات الإضافية للاختصار */
  }
}
```

### مثال على استجابة (نجاح – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "تم إنشاء الرسم البياني بنجاح."
  }
}
```

تحتوي الاستجابة على الحقول التالية:

| الحقل    | النوع  | الوصف |
| ------- | ------ | ----------- |
| Code    | عدد صحيح| رمز حالة يشبه HTTP يُعيده محرك المهمة. |
| Status  | نص     | حالة مقروءة من قِبل الإنسان (مثل `OK`). |
| TaskId  | نص     | مُعرّف المهمة غير المتزامنة. |
| Result  | كائن   | كائن يحتوي على نتائج محددة للعملية. |
| Result.ChartId | عدد صحيح | مُعرّف الرسم البياني الذي تم إنشاؤه أو تعديله. |
| Result.Message | نص     | رسالة قصيرة تصف النتيجة. |

### معالجة الأخطاء

| حالة HTTP | رمز الخطأ | الوصف | الإجراء المقترح |
| ----------- | ---------- | ----------- | ---------------- |
| 400         | InvalidParameter | معلِم طلب واحد أو أكثر مفقود أو بصيغة غير صحيحة. | تحقق من الحقول المطلوبة وأنواع البيانات. |
| 401         | Unauthorized | رمز مصادقة غير صالح أو مفقود. | حدّث رمز الوصول وأضفه إلى الرأس `Authorization`. |
| 404         | NotFound | كتاب العمل أو الورقة أو الكائن المحدّد غير موجود. | تحقق من `FileName` و`SheetName` وفهارس الكائنات. |
| 500         | ServerError | حدث خطأ غير متوقّع على الخادم. | أعد محاولة الطلب؛ وإذا استمرّت المشكلة، تواصل مع الدعم. |

### حالات الاستخدام الشائعة
- **إضافة رسم بياني جديد** إلى ورقة.  
- **إعادة تسمية ورقة** (`OperateObjectType = "Worksheet"` مع `WorksheetOperateParameter.NewName`).  
- **إدراج فاصل صفحات** (`OperateObjectType = "PageBreak"` مع `PageBreakOperateParameter`).  
- **تحديث بيانات مصدر جدول البيانات المقطعية** (`OperateObjectType = "PivotTable"` مع `PivotTableOperateParameter.SourceData`).  
- **تعديل إعدادات كتاب العمل** مثل وضع الحساب (`OperateObjectType = "WorkbookSettings"`).  

---  

*جميع الأوصاف مستمدة من مواصفة Aspose.Cells Cloud الرسمية لـ OpenAPI.*
---
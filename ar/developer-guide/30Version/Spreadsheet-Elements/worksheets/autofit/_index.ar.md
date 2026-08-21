---
title: "العمل مع ميزة التلاؤم التلقائي في ورقة عمل إكسل"
second_title: "مستند"
linktitle: "التلاؤم التلقائي"
type: docs
url: /ar/worksheets/autofit/
aliases: [  /ar/autofit-rows-and-columns-of-worksheet/ ]
keywords: "التلاؤم التلقائي، عمود، صف، Aspose.Cells، السحابة، إكسل، API، إعادة الحجم"
description: "تعرّف على كيفية إعادة حجم الصفوف والأعمدة تلقائيًا في ورقة عمل إكسل باستخدام Aspose.Cells Cloud REST API. يتضمن أمثلة بلغة cURL و .NET و Java و Python."
weight: 20
ArticleTitle: "العمل مع ميزة التلاؤم التلقائي في ورقة عمل إكسل – Aspose.Cells Cloud API"
---

## العمل مع ميزة التلاؤم التلقائي في ورقة عمل إكسل

- [كيفية تلاؤم عمود واحد تلقائيًا في ورقة عمل إكسل.](/cells/worksheets/autofit/column/)
- [كيفية تلاؤم عدة أعمدة تلقائيًا في ورقة عمل إكسل.](/cells/worksheets/autofit/columns/)
- [كيفية تلاؤم صف واحد تلقائيًا في ورقة عمل إكسل.](/cells/worksheets/autofit/row/)
- [كيفية تلاؤم عدة صفوف تلقائيًا في ورقة عمل إكسل.](/cells/worksheets/autofit/rows/)

**المتطلبات المسبقة**  
قبل استخدام عمليات التلاؤم التلقائي، يجب أن تمتلك ما يلي:

1. حساب Aspose.Cells Cloud مُسجّل ومُفعّل مع **معرف عميل (Client Id)** و**سر عميل (Client Secret)** سارين.
2. ملف مصنف مرفوع إلى مساحة التخزين السحابية لـ Aspose Cloud (أو متاح عبر رابط عام).
3. اسم ورقة العمل التي تنووي تعديلها.

**مرجع واجهة برمجة التطبيقات (API Reference)**  

| العملية | طريقة HTTP | نقطة النهاية (Endpoint) | المعلمات المطلوبة | جسم الطلب (Request Body) | استجابة نموذجية (Sample Response) | رموز الحالة (Status Codes) |
|-----------|-------------|----------|--------------------|--------------|----------------|--------------|
| تلاؤم **عمود** واحد تلقائيًا | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (مسار) <br> `columnIndex` (استعلام) | *بدون* | `{ "code": 200, "status": "OK", "message": "تم تلاؤم العمود تلقائيًا." }` | 200، 400، 401، 404، 500 |
| تلاؤم **أعمدة** متعددة تلقائيًا | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (مسار) <br> `startColumn`, `endColumn` (استعلام) | *بدون* | `{ "code": 200, "status": "OK", "message": "تم تلاؤم الأعمدة تلقائيًا." }` | 200، 400، 401، 404، 500 |
| تلاؤم **صف** واحد تلقائيًا | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (مسار) <br> `rowIndex` (استعلام) | *بدون* | `{ "code": 200, "status": "OK", "message": "تم تلاؤم الصف تلقائيًا." }` | 200، 400، 401، 404، 500 |
| تلاؤم **صفوف** متعددة تلقائيًا | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (مسار) <br> `startRow`, `endRow` (استعلام) | *بدون* | `{ "code": 200, "status": "OK", "message": "تم تلاؤم الصفوف تلقائيًا." }` | 200، 400، 401، 404، 500 |

**أمثلة الكود (Code Samples)**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// المصادقة
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// استدعاء تلاؤم الأعمدة
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// تلاؤم الصفوف تلقائيًا
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# تلاؤم عمود واحد تلقائيًا
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

توضح هذه المقاطع كيفية:

1. المصادقة مع Aspose.Cells Cloud باستخدام **معرف العميل (Client Id)** و**سر العميل (Client Secret)** الخاصين بك.
2. استدعاء نقطة النهاية المناسبة للتلاؤم التلقائي للأعمدة أو الصفوف.
3. معالجة الاستجابة، التي تؤكد نجاح العملية.

**الخطوات التالية**

بعد اكتمال استدعاء التلاؤم التلقائي، يمكنك تنزيل المصنف المُحدَّث:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

لا تتردد في ضبط المعلمات `startColumn` و`endColumn` و`startRow` و`endRow` لاستهداف نطاقات محددة.
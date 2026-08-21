---
title: "نسخ الصفوف في ورقة عمل Excel"
description: "نسخ البيانات والتنسيقات من صفوف كاملة محددة في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار v3.0). يتضمن معلومات عن المصادقة، تفاصيل الطلب والاستجابة، معالجة الأخطاء، وأمثلة باستخدام SDKs."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# نسخ الصفوف في ورقة عمل Excel <span style="float:right;">v3.0</span>

نسخ البيانات والتنسيقات من صفوف كاملة محددة في ورقة العمل.

---

## المتطلبات الأساسية

| # | المتطلب |
|---|----------|
| 1 | رمز **JWT** صالح. راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| 2 | يجب أن يكون ملف المصنف (`{name}`) موجودًا مسبقًا في **المجلد** / **التخزين** المُحدَّد. |
| 3 | يجب أن تكون ورقة العمل المستهدفة (`{sheetName}`) موجودة في المصنف. |
| 4 | (اختياري) معرف **المجلد** و**اسم التخزين** إن لم يكن الملف في الموقع الافتراضي. |

---

## نقطة النهاية

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*جميع معلمات المسار حساسة لحالة الأحرف.*

### معلمات المسار

| المعلمة | النوع | المطلوب | الوصف |
|---------|-------|---------|--------|
| `name` | نص | ✅ | اسم ملف المصنف (مثل `test.xlsx`). |
| `sheetName` | نص | ✅ | اسم ورقة العمل (مثل `Sheet1`). |

### معلمات الاستعلام

| المعلمة | النوع | المطلوب | الوصف |
|---------|-------|---------|--------|
| `sourceRowIndex` | عدد صحيح | ✅ | المؤشر بصفر (zero-based) للصف المصدر. |
| `destinationRowIndex` | عدد صحيح | ✅ | المؤشر بصفر حيث سيتم وضع الصفوف المنسوخة. |
| `rowNumber` | عدد صحيح | ✅ | عدد الصفوف المراد نسخها. |
| `worksheet` | نص | ❌ | معرّف ورقة العمل؛ عادةً يساوي **sheetName**. |
| `folder` | نص | ❌ | مسار المجلد الذي يحتوي على المصنف. |
| `storageName` | نص | ❌ | اسم خدمة التخزين. |

---

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **ملاحظة**  
> استبدل `<jwt token>` برمز JWT صالح تم الحصول عليه من خدمة المصادقة.

---

## الاستجابة الناجحة

| الرمز | الوصف |
|-------|--------|
| **200** | تم نسخ الصفوف بنجاح. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

يحتوي جسم الاستجابة على مثيل من `CellsCloudResponse`.

---

## معالجة الأخطاء

| رمز HTTP | المعنى | مثال على جسم الاستجابة |
|----------|---------|------------------------|
| **400** | طلب غير صالح – معلمات مفقودة أو غير صحيحة. | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401** | غير مصادق عليه – رمز JWT غير صالح أو مفقود. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | غير موجود – المصنف أو ورقة العمل غير موجودين. | `{ "Code": 404, "Message": "File not found." }` |
| **500** | خطأ داخلي في الخادم – حالة غير متوقعة في الخادم. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**إرشادات المعالجة**

* **400** – تحقق من وجود جميع معلمات الاستعلام المطلوبة وصحتها.  
* **401** – أعد توليد أو حدّث رمز JWT.  
* **404** – تأكد من أسماء المصنف وورقة العمل، وتحقق من وجود الملف في المجلد/التخزين المحدَّد.  
* **500** – أعد المحاولة بعد تأخير قصير؛ إن استمرت المشكلة، تواصل مع دعم Aspose.

---

## أمثلة باستخدام SDKs

توضح المقاطع التالية كيفية استدعاء عملية **نسخ الصفوف** باستخدام SDKs الرسمية لـ Aspose.Cells Cloud.

| اللغة | المثال |
|--------|--------|
| **C#** | <details><summary>عرض الكود</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>عرض الكود</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>عرض الكود</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>عرض الكود</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>عرض الكود</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient("clientId", "clientSecret")\n_, err := api.PostCopyWorksheetRows(context.Background(), "test.xlsx", "Sheet1", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>عرض الكود</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>عرض الكود</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>عرض الكود</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*تتوفر ملفات المصدر الكاملة في [مستودع Aspose‑Cells‑Cloud على GitHub](https://github.com/aspose-cells-cloud).*

---

## انظر أيضًا

- [إضافة صف في ورقة عمل Excel](/rows/add/)  
- [حذف صف في ورقة عمل Excel](/rows/delete/)  
- [تحديث صف في ورقة عمل Excel](/rows/update/)  

---

*تم إنشاء هذه الصفحة في **{{DATE}}**. للحصول على أحدث إصدار من هذه الواجهة، راجع [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows).*
---
title: "ضبط ارتفاع الصفوف ل نطاق في إكسل – واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
description: "تغيير ارتفاع الصفوف ضمن نطاق محدّد في ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. تتضمّن عنوان URL للنقطة الطرفية، والمُعطَلات، ومثال cURL، وردود مرجعيّة، ومقتطفات رمزية لواجهات برمجة التطبيقات (SDKs) بلغات برمجة متعددة."
keywords: "Aspose.Cells، ارتفاع الصفوف، النطاق، إكسل، واجهة REST API، الإصدار 3.0، SDK، cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# ضبط ارتفاع الصفوف ل نطاق في إكسل

تُحدّث هذه العملية ارتفاع الصفوف لِنطاق محدّد موجود في ورقة عمل مخزّنة في التخزين السحابي لـ Aspose Cloud.

## الشروط المسبقة / المصادقة

يجب عليك الحصول على رمز وصول JWT من خدمة المصادقة OAuth في Aspose Cloud مع النطاق **Cells.ReadWrite**.

أدرج الرمز في رأس الطلب `Authorization` لكل طلب:

```http
Authorization: Bearer <jwt token>
```

إن لم يكن لديك رمز وصول، اتّبع **دليل مصادقة Aspose Cloud** لطلب رمز.

## طلب HTTP

| الطريقة | عنوان URI |
|--------|-----------|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### المُعطَلات المسار (Path Parameters)

| الاسم | النوع | الوصف |
|------|-------|--------|
| `name` | `string` | **مطلوبة.** اسم ملف إكسل المخزّن في السحابة. |
| `sheetName` | `string` | **مطلوبة.** اسم ورقة العمل التي تحتوي على النطاق المستهدف. |

### المُعطَلات الاستعلامية (Query Parameters)

| الاسم | النوع | المطلوب | الوصف |
|------|-------|----------|--------|
| `value` | `number` | **نعم** | ارتفاع الصف المطلوب تطبيقه على النطاق (بالنقاط). |
| `folder` | `string` | لا | مسار المجلّد داخل التخزين حيث يقع الملف. |
| `storageName` | `string` | لا | اسم خدمة التخزين (في حالة تكوين أكثر من تخزين). |

### جسم الطلب (JSON)

يجب أن يحتوي الجسم على كائن **Range** يُعرّف الصفوف التي سيتأثّر بها الارتفاع.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### مخطط كائن Range بصيغة JSON

| الخاصية | النوع | المطلوب | الوصف |
|----------|-------|----------|--------|
| `FirstRow` | عدد صحيح | **مطلوبة** | الفهرس الصفرِي للصف الأول في النطاق. |
| `RowCount` | عدد صحيح | **مطلوبة** | عدد الصفوف التي سيتم تطبيق الارتفاع عليها. |
| `FirstColumn` | عدد صحيح | لا | الفهرس الصفرِي للعمود الأول (اختياري عند ضبط ارتفاع الصفوف فقط). |
| `ColumnCount` | عدد صحيح | لا | عدد الأعمدة التي يغطيها النطاق (اختياري). |

تُستخدم فقط الخصائص المذكورة أعلاه لعملية ضبط ارتفاع الصفوف؛ ويتم تجاهل أي حقول إضافية.

## مثال على الطلب

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### مثال على الرد (ناجح)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | OK | تمت تطبيق المرشّح بنجاح؛ ويحتوي الردّ على تفاصيل العملية. |
| 400 | Bad Request | مُعطَلات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error | خطأ داخلي غير متوقّع في الخادم. |

تحتوي جميع الردود على `Code` رقمي و`Status` قابل للقراءة (أو `Message` في حالات الأخطاء). قد تُقدّم `ErrorDetails` إضافية عند حدوث خطأ.

## أمثلة على واجهات برمجة التطبيقات (SDKs)

تُظهر المقتطفات التالية كيفية استدعاء **ضبط ارتفاع الصفوف ل نطاق** باستخدام واجهات برمجة التطبيقات الرسمية لـ Aspose.Cells Cloud SDK.

| اللغة | المثال |
|-------|--------|
| **C#** | <details><summary>إظهار الكود</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>إظهار الكود</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>إظهار الكود</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>إظهار الكود</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Row height set'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>إظهار الكود</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>إظهار الكود</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>إظهار الكود</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jwt token>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>إظهار الكود</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **ملاحظة:** تضيف جميع واجهات برمجة التطبيقات (SDKs) الرأس `Authorization: Bearer` تلقائيًا عند تكوين رمز الوصول.

## انظر أيضًا

- **مواصفات OpenAPI** – العقدة التفصيلية لهذه العملية: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **مستودع واجهات برمجة التطبيقات (SDKs) لـ Aspose.Cells Cloud** – الكود المصدري وروابط لغات برمجة إضافية: <https://github.com/aspose-cells-cloud>
- **دليل المصادقة** – كيفية الحصول على رمز JWT: <https://docs.aspose.cloud/cells/authentication/>

---
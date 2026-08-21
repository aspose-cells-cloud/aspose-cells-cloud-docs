---
title: "احصل على التصفية التلقائية"
description: "استرجاع وصف التصفية التلقائية من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API."
keywords: "التصفية التلقائية، Excel، Aspose.Cells Cloud، REST API، SDK، C#، Java، PHP، Ruby، Node.js، Python، Perl، Go"
type: docs
url: /cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# استرجاع وصف التصفية التلقائية من ورقة عمل

**الإصدار:** v3.0  
**النقطة النهائية:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **ملاحظة:** جميع الطلبات التجريبية تستخدم **HTTPS**. لا ترسل أبدًا رموز JWT عبر اتصال غير آمن.

---

## نظرة عامة

تتيح **التصفية التلقائية (AutoFilter)** للمستخدمين تصفية الصفوف في ورقة العمل بناءً على قيم الأعمدة، أو الألوان، أو المعايير المخصصة، وغير ذلك. وتُعيد هذه الواجهة التكوين الكامل للتصفية التلقائية — بما في ذلك أعمدة التصفية، والنطاق، وتفاصيل الفرز — بحيث يمكنك فحص إعدادات التصفية أو إعادة إنتاجها برمجيًا.

---

## المتطلبات الأساسية

| المتطلب | الوصف |
|----------|---------|
| **المصادقة** | مطلوب رمز JWT صالح. راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **مكان الملف** | يجب تخزين الملف المصنف في تخزين Aspose Cloud (أو في تخزين خارجي متصل). |
| **الصيغ المدعومة** | أي تنسيق Excel يدعمه Aspose.Cells (مثل `.xlsx`، `.xls`، `.xlsm`). |
| **حزمة SDK (اختيارية)** | إذا كنت تفضل استخدام SDK، قم بتثبيت الحزمة المناسبة (مثل `dotnet add package Aspose.Cells-Cloud` لـ .NET). |

---

## الطلب

### طلب HTTP

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### معاملات المسار

| المعامل | النوع | الوصف |
|----------|--------|---------|
| `name` | string | **إجباري.** اسم ملف المصنف، بما في ذلك الامتداد. |
| `sheetName` | string | **إجباري.** اسم ورقة العمل التي سيتم استرجاع التصفية التلقائية منها. |

### معاملات الاستعلام

| المعامل | النوع | الوصف |
|----------|--------|---------|
| `folder` | string | مسار المجلد في التخزين حيث يقع المصنف. |
| `storageName` | string | اسم التخزين المراد استخدامه. |

### الأمان

تستخدم الواجهة **المصادقة القائمة على رمز JWT**. تضمن إضافة الرمز في رأس `Authorization`:

```http
Authorization: Bearer <your_jwt_token>
```

---

## مثال على الطلب (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## الاستجابة

ترجع الخدمة كائن JSON يغلف نموذج `AutoFilter`.

### مخطط الاستجابة الناجحة

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### مثال على الاستجابة

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFilter",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**رموز حالة HTTP**

| الكود | المعنى | الوصف |
|--------|----------|---------|
| 200 | OK (نجاح) | تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب خاطئ | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرح به | رمز JWT غير صالح أو مفقود. |
| 413 | حجم البيانات كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

---

## أمثلة باستخدام SDKs

تتوفر هذه العملية في جميع SDKs الخاصة بـ Aspose.Cells Cloud. فيما يلي مقاطع جاهزة للتشغيل.

| اللغة | المثال |
|--------|---------|
| **C#** | <details><summary>عرض الكود</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>عرض الكود</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>عرض الكود</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>عرض الكود</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>عرض الكود</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>عرض الكود</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>عرض الكود</summary>```go\nimport (\n    "fmt"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), "Book1.xlsx", "Sheet1", "MyFolder", "MyStorage")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>عرض الكود</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

لرؤية قائمة كاملة بـ SDKs وتعليمات التثبيت، تفضل بزيارة [مستودع Aspose.Cells Cloud على GitHub](https://github.com/aspose-cells-cloud).

---

## انظر أيضًا

- [التصفية التلقائية – مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [عمليات التخزين](https://docs.aspose.cloud/cells/storage/)  

---
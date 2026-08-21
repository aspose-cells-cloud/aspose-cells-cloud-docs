---
title: "حذف عمود من ورقة عمل Excel باستخدام Aspose.Cells Cloud API"
description: "تعلم كيفية حذف عمود واحد أو أكثر من ورقة عمل Excel عبر واجهة Aspose.Cells Cloud REST API. يشمل المصادقة، وبنية الطلب، والمعلمات، والاستجابات، ومعالجة الأخطاء، وأمثلة SDK."
keywords: ["Aspose.Cells", "حذف عمود", "Excel API", "REST", "Cloud", "Worksheet", "Columns"]
date: 2026-07-30
api_version: "v3.0"
---

# حذف عمود من ورقة عمل Excel

**النقطة الطرفية**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

تقوم هذه العملية بإزالة عمود واحد أو مجموعة أعمدة من ورقة عمل. يمكن تحديث مراجع الخلايا (بما في ذلك الصيغ) تلقائيًا بعد الحذف.

---

## جدول المحتويات
1. [المتطلبات المسبقة](#prerequisites)  
2. [المصادقة](#authentication)  
3. [رابط الطلب وطريقة HTTP](#request-url--http-method)  
4. [المعلمات](#parameters)  
   - [المعلمات في المسار](#path-parameters)  
   - [المعلمات الاستعلامية](#query-parameters)  
5. [مثال باستخدام cURL](#curl-example)  
6. [الاستجابات](#responses)  
7. [رموز الأخطاء](#error-codes)  
8. [عينات SDK](#sdk-samples)  
9. [ملاحظات إضافية](#additional-notes)  

---

## المتطلبات المسبقة
- رمز وصول **JWT** ساري المفعول تم الحصول عليه عبر عملية مصادقة Aspose Cloud.  
- يجب أن يكون المصنف (`{name}`) مرفعًا مسبقًا إلى مساحة التخزين في Aspose Cloud (أو متاحًا عبر معلمات الاستعلام `folder`/`storageName`).  

---

## المصادقة
تتطلب جميع طلبات Aspose.Cells Cloud مصادقة باستخدام رمز **Bearer token**.

```http
Authorization: Bearer <access_token>
```

راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) للحصول على تفاصيل حول كيفية الحصول على رمز JWT.

---

## رابط الطلب وطريقة HTTP
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – اسم ملف المصنف (مثال: `test.xlsx`).  
- **`{sheetName}`** – اسم ورقة العمل (مثال: `Sheet1`).  
- **`{columnIndex}`** – المؤشر الصفري (zero‑based) للعمود الأول المراد حذفه.

---

## المعلمات

| الاسم            | الموقع | النوع    | الإلزام | الوصف |
|-----------------|--------|----------|---------|-------|
| **name**        | path   | string   | ✅ نعم  | اسم ملف المصنف. |
| **sheetName**   | path   | string   | ✅ نعم  | اسم ورقة العمل. |
| **columnIndex** | path   | integer  | ✅ نعم  | المؤشر الصفري للعمود الأول المراد حذفه. |
| **startColumn** | query  | integer  | ❌ لا   | المؤشر الصفري لبداية عملية الحذف. يُفترض القيمة الافتراضية `columnIndex` إذا تُركت فارغة. |
| **totalColumns**| query  | integer  | ❌ لا   | عدد الأعمدة المراد حذفها. إذا تُركت فارغة، سيُحذف فقط العمود المُعرّف بـ `columnIndex`. |
| **updateReference** | query | boolean | ❌ لا | عند القيمة `true`، تُحدَّث مراجع الخلايا (بما في ذلك الصيغ) في المصنف ككل بعد الحذف. |
| **folder**      | query  | string   | ❌ لا   | مسار المجلد الذي يحتوي على المصنف. |
| **storageName** | query  | string   | ❌ لا   | اسم خدمة تخزين Aspose Cloud. |

> **ملاحظة** – معلمة `columns` المذكورة في مواصفات API منخفضة المستوى قد استُبدلت بمعلمات الاستعلام الأقوى `startColumn` و`totalColumns`. وتُقبَل الطريقتان معًا لضمان التوافق مع الإصدارات السابقة.

---

## مثال باستخدام cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### التفسير
- يحذف العمود **B** (`columnIndex = 1`) من `Sheet1` في ملف `test.xlsx`.  
- يُحدِّد `startColumn=1` و`totalColumns=1` حذف عمود واحد فقط.  
- يضمن `updateReference=true` ضبط الصيغ والمراجع الأخرى تلقائيًا.

---

## الاستجابات

| رمز HTTP | الوصف | مثال |
|----------|--------|------|
| **200** | نجاح – تمت إزالة العمود (الأعمدة). | `{ "Code": 200, "Status": "OK" }` |
| **400** | طلب غير صحيح – معلمات مفقودة أو غير صالحة. | `{ "Code": 400, "Message": "قيمة totalColumns غير صحيحة." }` |
| **401** | غير مصرّح – رمز JWT مفقود أو غير صالح. | `{ "Code": 401, "Message": "فشل المصادقة." }` |
| **404** | غير موجود – المصنف أو ورقة العمل غير موجودين. | `{ "Code": 404, "Message": "ورقة العمل 'Sheet1' غير موجودة." }` |
| **500** | خطأ داخلي في الخادم – حالة غير متوقعة على الخادم. | `{ "Code": 500, "Message": "حدث خطأ غير متوقع." }` |

يتبع محتوى الاستجابة النموذج العام **`CellsCloudResponse`**.

---

**رموز حالات HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|---------------------------------------------|
| 200  | نجاح                        | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صحيح                | معلمات مفقودة أو غير صالحة (مثال: نوع ملف غير مدعوم). |
| 401  | غير مصرّح                  | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا        | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500  | خطأ داخلي في الخادم          | خطأ غير متوقع في الخادم. |
---

## عينات SDK

فيما يلي مقتطفات جاهزة للتشغيل لأشهر SDKs. استبدل القيم الوهمية (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>`، إلخ) ببياناتك الخاصة.

| اللغة | المثال |
|--------|--------|
| **C#** | <details><summary>عرض الكود</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>عرض الكود</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>عرض الكود</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>عرض الكود</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>عرض الكود</summary> <br>```go\npackage main\n\nimport (\n    "context"\n    "fmt"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_ACCESS_TOKEN>"\n    cfg.BasePath = "https://api.aspose.cloud"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), "test.xlsx", "Sheet1", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println("Error:", err)\n        return\n    }\n    fmt.Println("Status:", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>عرض الكود</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>عرض الكود</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo "Status: " . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>عرض الكود</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint "Status: ", $response->{Status}, "\n";\n```</details> |

*جميع SDKs تضيف تلقائيًا رأس `Authorization` المطلوب عند تكوين `access_token`.*

---

## ملاحظات إضافية

### رؤوس الأمان (موصى بها للإنتاج)
عند عرض صفحة الوثائق، أضف رؤوس HTTP التالية لتعزيز الأمان:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### نصائح الأداء
- احمّل نصوص تحليل الطرف الثالث (`gtag.js`, `containerize.js`) باستخدام السمة `async` أو أخّر تحميلها حتى بعد اكتمال عرض الصفحة.  
- قلّص حزم JavaScript/CSS المخصصة.  
- سبق تحميل أيقونات SVG الصغيرة إن كانت تُعيق العرض:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### تحسينات تحسين محركات البحث (JSON‑LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Delete Column from Excel Worksheet using Aspose.Cells Cloud API",
  "description": "Learn how to delete one or more columns from an Excel worksheet via Aspose.Cells Cloud REST API.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Delete Column", "Excel", "REST API"]
}
```

ضع المقتطف داخل كتلة `<script type="application/ld+json">` في رأس HTML.

### إمكانية الوصول
- جميع الصور الزخرفية تستخدم `alt=""` أو تُخفي باستخدام `aria-hidden="true"`.  
- تتضمن صورة Open Graph الآن سمة `alt` في وسم meta للإكمال.  

---

## انظر أيضًا
- [مواصفة OpenAPI لـ DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [نظرة عامة على المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [SDKs لـ Aspose.Cells Cloud على GitHub](https://github.com/aspose-cells-cloud)  

---
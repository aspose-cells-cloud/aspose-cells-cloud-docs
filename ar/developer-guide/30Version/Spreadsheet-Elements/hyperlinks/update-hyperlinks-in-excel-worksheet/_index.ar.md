---
title: "تحديث رابط تشعبي في ورقة عمل إكسل – دليل واجهة برمجة التطبيقات Aspose.Cells Cloud"
description: "تعرّف على كيفية تحديث رابط تشعبي في ورقة عمل إكسل باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يشمل الرابط، والمتغيرات، ومخطط جسم الطلب، ومثال cURL، وأجزاء كود SDK، والتعامل مع الأخطاء، وتحديد معدل الطلبات، والمتطلبات الأساسية."
keywords:
  - "Aspose.Cells"
  - "تحديث رابط تشعبي"
  - "واجهة برمجة تطبيقات إكسل"
  - "واجهة REST API"
  - "جدول بيانات سحابي"
  - "الإصدار 3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# تحديث رابط تشعبي في ورقة عمل إكسل  

**إصدار الواجهة:** v3.0  

تقوم العملية **PostWorksheetHyperlink** بتحديث رابط تشعبي موجود في ورقة عمل محددة باستخدام فهرسها الصفري‑الأساسي.

---

## جدول المحتويات
1. [المتطلبات الأساسية](#prerequisites)  
2. [تحديد معدل الطلبات](#rate-limiting)  
3. [الرابط (Endpoint)](#endpoint)  
4. [المتغيرات](#parameters)  
   - [المتغيرات المسار](#path-parameters)  
   - [المتغيرات الاستعلام](#query-parameters)  
   - [مخطط جسم الطلب](#request-body-schema)  
5. [الاستجابات](#responses)  
   - [الاستجابة الناجحة](#success-response)  
   - [استجابات الأخطاء](#error-responses)  
6. [مثال باستخدام cURL](#curl-example)  
7. [أجزاء كود SDK](#sdk-code-samples)  
8. [انظر أيضًا](#see-also)  

---

## المتطلبات الأساسية <a name="prerequisites"></a>

| المتطلب | الوصف |
|---------|---------|
| **المصادقة** | تعتمد المصادقة على رمز JWT. احصل على الرمز كما هو موضح في [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **التخزين** | يجب أن يكون الملف المصنف مخزنًا في مستودع Aspose Cloud المدعوم (الافتراضي هو **Default**). |
| **الصلاحيات** | يجب أن يحتوي رمز JWT على صلاحية قراءة وكتابة الملف المصنف المستهدف. |
| **الرؤوس** | يتطلب كل طلب وجود الرأسين `Content-Type: application/json` و `Accept: application/json`. |

---

## تحديد معدل الطلبات <a name="rate-limiting"></a>

تحدّ واجهة Aspose.Cells Cloud من عدد الطلبات إلى **60 طلبًا كحد أقصى في الدقيقة لكل رمز وصول**. يؤدي تجاوز هذا الحد إلى إرجاع رمز HTTP **429 Too Many Requests**. نفّذ خوارزمية التأخير الأُسي (exponential back‑off) أو التزم بقيمة الرأس `Retry-After` عند حدوث تقييد.

---

## الرابط (Endpoint) <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*تحديث الرابط التشعبي المُعرّف بـ `hyperlinkIndex` في ورقة العمل `sheetName` من الملف `name`.*

---

## المتغيرات <a name="parameters"></a>

### المتغيرات المسار <a name="path-parameters"></a>

| الاسم | النوع | الإلزام | الوصف |
|-------|--------|---------|--------|
| `name` | سلسلة نصية | ✅ | اسم ملف إكسل (مع امتداد الملف). |
| `sheetName` | سلسلة نصية | ✅ | اسم ورقة العمل التي يحتوي الرابط التشعبي فيها. |
| `hyperlinkIndex` | عدد صحيح | ✅ | الفهرس الصفري‑الأساسي للرابط التشعبي المراد تحديثه. |

### متغيرات الاستعلام <a name="query-parameters"></a>

| الاسم | النوع | الإلزام | الوصف |
|-------|--------|---------|--------|
| `folder` | سلسلة نصية | ❌ | مسار المجلد داخل المستودع الذي يوجد فيه الملف المصنف. |
| `storageName` | سلسلة نصية | ❌ | اسم خدمة التخزين (مثل `Default`). |

### مخطط جسم الطلب <a name="request-body-schema"></a>

يجب أن يحتوي جسم الطلب على كائن **`hyperlink`**. يمكنك تزويد الحقول التي ترغب في تغييرها فقط؛ وتبقى الحقول الاختيارية غير المُحدّدة على قيمها الحالية.

| الحقل | النوع | الإلزام | الوصف |
|--------|--------|---------|--------|
| `Address` | سلسلة نصية | ✅ | عنوان URL الهدف للرابط التشعبي. |
| `Area` | كائن | ✅ | نطاق الخلايا التي يوضع فيها الرابط التشعبي. يجب أن يحتوي على `StartRow`، `StartColumn`، `EndRow`، `EndColumn` (جميعها أعداد صحيحة، فهرسها صفري‑الأساسي). |
| `ScreenTip` | سلسلة نصية | ❌ | النص المنبثق (Tooltip) الذي يظهر عند تمرير الماوس فوق الرابط. |
| `TextToDisplay`| سلسلة نصية| ❌ | النص المعروض داخل الخلية. |
| `link` | كائن| ❌ | روابط هايبرميديا (`Href`، `Rel`، `Title`، `Type`). عمومًا لا يُدرج في أحمال الطلبات. |

**تعريف كائن `Area`**

| الحقل الفرعي | النوع | الإلزام | الوصف |
|-------------|--------|---------|--------|
| `StartRow` | عدد صحيح | ✅ | فهرس الصف الابتدائي (صفري‑الأساسي). |
| `StartColumn`| عدد صحيح | ✅ | فهرس العمود الابتدائي (صفري‑الأساسي). |
| `EndRow` | عدد صحيح | ✅ | فهرس الصف النهائي (صفري‑الأساسي). |
| `EndColumn` | عدد صحيح | ✅ | فهرس العمود النهائي (صفري‑الأساسي). |

---

## الاستجابات <a name="responses"></a>

### الاستجابة الناجحة <a name="success-response"></a>

| الحقل | النوع | الوصف |
|-------|--------|--------|
| `Code`| عدد صحيح| رمز حالة HTTP (200 للنجاح). |
| `Status`| سلسلة نصية| حالة نصية (`OK`). |
| `Hyperlink`| كائن (اختياري) | كائن الرابط التشعبي المحدّث، ويُعاد فقط عند طلب كائن `link` الفرعي. |

**مثال JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### استجابات الأخطاء <a name="error-responses"></a>

| رمز HTTP | السبب | مثال جسم الاستجابة |
|-----------|--------|--------------------|
| **400** | طلب غير صالح – متغيرات مفقودة أو غير صحيحة. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | غير مصرّح – رمز JWT مفقود أو غير صالح. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | غير موجود – الملف المصنف أو ورقة العمل أو الرابط التشعبي غير موجود. | `{ "Code":"404", "Message":"File not found." }` |
| **429** | طلبات كثيرة جدًا – تم تجاوز الحد الأقصى للطلبات. | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | خطأ داخلي في الخادم – فشل غير متوقع في الخادم. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## مثال باستخدام cURL <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**الاستجابة**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*نصيحة:* احفظ حمولة JSON في ملف (مثل `payload.json`) واستخدمها عبر `--data @payload.json` لنسخ ولصق أبسط.

---

## أجزاء كود SDK <a name="sdk-code-samples"></a>

توضح الأجزاء التالية كيفية استدعاء **PostWorksheetHyperlink** باستخدام SDKs الرسمية لـ Aspose.Cells Cloud. استبدل القيم الوهمية (`<YOUR_JWT_TOKEN>`، `<FILE_NAME>`، إلخ) ببيانات حقيقية.

| اللغة | المثال |
|--------|--------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*جميع SDKs مفتوحة المصدر، ويمكن العثور عليها في [مستودع Aspose.Cells Cloud على GitHub](https://github.com/aspose-cells-cloud).*

---

## انظر أيضًا <a name="see-also"></a>

- **المصادقة** – [البدء باستخدام رموز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **عمليات التخزين** – [رفع ملف](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **عمليات روابط تشعبية أخرى** – [إضافة رابط تشعبي](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [حذف رابط تشعبي](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **مواصفات OpenAPI** – التعريف الكامل للرابط: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*آخر تحديث للمستند: 2026‑07‑30*
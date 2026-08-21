---
title: "تحويل كائن OLE إلى صورة – واجهة Aspose.Cells Cloud REST API"
description: "استرجاع كائن OLE مُضمّن من ورقة عمل Excel وتحويله إلى تنسيق PNG أو JPEG أو TIFF أو GIF أو EMF أو BMP باستخدام واجهة Aspose.Cells Cloud REST API."
keywords:
  - "تحويل كائن OLE إلى صورة"
  - "Aspose.Cells Cloud"
  - "واجهة REST API"
  - "Excel"
  - "OLE"
  - "تحويل الصور"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# تحويل كائن OLE إلى صورة

استرجاع كائن OLE مُضمّن من ورقة عمل وإرجاعه بالتنسيق المطلوب للصورة.

---

## المتطلبات المسبقة

قبل استدعاء هذه النقطة النهائية، تأكّد من توفر ما يلي:

1. **حساب Aspose.Cells Cloud** – سجّل الدخول في [بوابة Aspose Cloud](https://dashboard.aspose.cloud/).  
2. **ملف المصنف المرفوع إلى مساحة التخزين السحابية** – استخدم واجهة **رفع ملف** API أو واجهة Aspose Cloud UI.  
3. **رمز وصول JWT** – احصل على رمز مميز اتبعًا [دليل المصادقة](/total/getting-started/rest-api-overview/authenticating-api-requests/).  

---

## الأمان والمصادقة

تتطلب جميع واجهات Aspose.Cells Cloud **مصادقة تعتمد على رمز JWT**. تضمين الرمز في رأس `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

تدعم فقط نقاط النهاية HTTPS؛ لا تستخدم أبدًا `http://`.

---

## الطلب

### طريقة HTTP
`GET`

### النقطة النهائية
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### معاملات المسار

| الاسم          | النوع   | الإلزامي | الوصف                              |
|---------------|--------|----------|------------------------------------------|
| `name`        | سلسلة نصية | ✅       | اسم ملف المصنف (مثل `Book1.xlsx`). |
| `sheetName`   | سلسلة نصية | ✅       | ورقة العمل التي تحتوي على كائن OLE. |
| `objectNumber`| عدد صحيح| ✅       | المؤشر المُعدّ من الصفر لكائن OLE.      |

### معاملات الاستعلام

| الاسم        | النوع   | الإلزامي | الوصف |
|-------------|--------|----------|-------------|
| `format`    | سلسلة نصية | ❌       | تنسيق الصورة المطلوب (`png` أو `jpeg` أو `tiff` أو `gif` أو `emf` أو `bmp`). إذا تم تخطيه، الافتراضي هو `png`. |
| `folder`    | سلسلة نصية | ❌       | مسار المجلد الذي يوجد فيه المصنف. |
| `storageName`| سلسلة نصية| ❌       | اسم خدمة التخزين (مثل `MyCloud`). |

---

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*استبدل `<jwt-token>` برمز JWT صالح.*

---

## الاستجابة

| الحالة | نوع المحتوى            | الوصف |
|--------|-------------------------|-------------|
| `200`  | `image/png` (أو التنسيق المطلوب) | بيانات الصورة الثنائية التي تمثّل كائن OLE. |
| `400`  | `application/json`      | معاملات طلب غير صالحة. |
| `401`  | `application/json`      | فشلت المصادقة ( JWT مفقود أو غير صالح). |
| `404`  | `application/json`      | لم يتم العثور على المصنف أو ورقة العمل أو كائن OLE المحدّد. |
| `500`  | `application/json`      | خطأ من جانب الخادم. |

### التعامل مع الحمولة الثنائية

تُعيد الواجهة بايتات الصورة الخام. يمكنك:

* **الحفظ مباشرةً في ملف** (مثال لينكس/ماك أو إس):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **الترميز إلى Base64** لغرض التحقق من الأخطاء أو التضمين في JSON:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *مثال مختصر لمخرجات Base64:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## استجابات الأخطاء

| حالة HTTP | الرمز                   | الرسالة |
|-----------|------------------------|---------|
| `400`     | `InvalidParameter`     | أحد معاملات الطلب أو أكثر غير صالحة. |
| `401`     | `AuthenticationFailed`| رمز JWT مفقود أو غير صالح. |
| `404`     | `PropertyNotFound`     | المصنف أو ورقة العمل أو كائن OLE المطلوب غير موجود. |
| `500`     | `InternalError`        | حدث خطأ غير متوقّع على الخادم. |

---

## أمثلة لواجهات برمجة التطبيقات (SDK)

توضّح المقاطع التالية كيفية استدعاء العملية باستخدام واجهات برمجة التطبيقات الرسمية. استبدل `YOUR_JWT_TOKEN` وغيره من الأماكن المخصّصة بقيمك الفعلية.

| اللغة | المثال |
|-------|--------|
| **C#** | <details><summary>عرض الكود</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>عرض الكود</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>عرض الكود</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>عرض الكود</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>عرض الكود</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>عرض الكود</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>عرض الكود</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>عرض الكود</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(تتوافر القائمة الكاملة لواجهات برمجة التطبيقات (SDK) في [مستودع GitHub](https://github.com/aspose-cells-cloud).)*

---

## العمليات ذات الصلة

- **إضافة كائن OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **تحديث كائن OLE** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **حذف كائن OLE** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **الحصول على قائمة كائنات OLE** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

لمزيد من التفاصيل، راجع صفحات المرجع المقابلة لواجهة API.

---

## موارد إضافية

- **مواصفات OpenAPI** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **دليل المصادقة** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **مستودعات واجهات برمجة التطبيقات (SDK)** – <https://github.com/aspose-cells-cloud>
- **الأداء والوصول** – نفّذ تحليلات Lighthouse وaxe-core لضمان أوقات تحميل مثالية والامتثال لمتطلبات WCAG 2.1 AA.
---
title: "OLE Nesnesini Görüntüye Dönüştür – Aspose.Cells Cloud REST API"
description: "Excel bir çalışma sayfasından gömülü bir OLE nesnesini alın ve Aspose.Cells Cloud REST API kullanarak PNG, JPEG, TIFF, GIF, EMF veya BMP formatına dönüştürün."
keywords:
  - "OLE nesnesini görüntüye dönüştür"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "görüntü dönüşümü"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# OLE Nesnesini Görüntüye Dönüştür

Bir çalışma sayfasından gömülü bir OLE nesnesini alın ve istenen görüntü formatında döndürün.

---

## Öncelikli Gereksinimler

Bu uç noktayı çağırmadan önce şunların olduğundan emin olun:

1. **Aspose.Cells Cloud hesabı** – [Aspose Cloud portalında](https://dashboard.aspose.cloud/) kaydolun.  
2. **Bulut depolama alanına yüklenmiş çalışma kitabınız** – **Dosya Yükle** API’sini veya Aspose Cloud arayüzünü kullanın.  
3. **JWT erişim belirteci** – [kimlik doğrulama kılavuzunu](/total/getting-started/rest-api-overview/authenticating-api-requests/) izleyerek bir belirteç alın.  

---

## Güvenlik ve Kimlik Doğrulama

Tüm Aspose.Cells Cloud API’leri **JWT belirteci tabanlı kimlik doğrulama** gerektirir. Belirteci `Authorization` başlığında sağlayın:

```http
Authorization: Bearer <jwt-token>
```

Yalnızca HTTPS uç noktaları desteklenir; asla `http://` kullanmayın.

---

## İstek

### HTTP Yöntemi
`GET`

### Uç Nokta
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Yol Parametreleri

| Ad            | Tür    | Gerekli  | Açıklama                              |
|---------------|--------|----------|------------------------------------------|
| `name`        | string | ✅       | Çalışma kitabının dosya adı (örneğin `Book1.xlsx`). |
| `sheetName`   | string | ✅       | OLE nesnesini içeren çalışma sayfası. |
| `objectNumber`| integer| ✅       | OLE nesnesinin sıfır tabanlı indeksi.      |

### Sorgu Parametreleri

| Ad            | Tür    | Gerekli  | Açıklama |
|---------------|--------|----------|----------|
| `format`      | string | ❌       | İstenen görüntü formatı (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). Atlanırsa varsayılan `png`’dir. |
| `folder`      | string | ❌       | Çalışma kitabının bulunduğu klasör yolu. |
| `storageName` | string | ❌       | Depolama hizmetinin adı (örneğin `MyCloud`). |

---

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*`<jwt-token>` ifadesini geçerli bir JWT belirteciyle değiştirin.*

---

## Yanıt

| Durum | İçerik Türü             | Açıklama |
|-------|-------------------------|----------|
| `200` | `image/png` (veya istenen format) | OLE nesnesini temsil eden ikili görüntü verisi. |
| `400` | `application/json`      | Geçersiz istek parametreleri. |
| `401` | `application/json`      | Kimlik doğrulama başarısız (eksik/geçersiz JWT). |
| `404` | `application/json`      | Belirtilen çalışma kitabını, çalışma sayfasını veya OLE nesnesini bulunamadı. |
| `500` | `application/json`      | Sunucu tarafında hata oluştu. |

### İkili Yükün İşlenmesi

API ham görüntü baytlarını döndürür. Aşağıdakileri yapabilirsiniz:

* **Doğrudan bir dosyaya kaydetme** (Linux/macOS örneği):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **Hata ayıklama veya JSON’a gömmek için Base64’e kodlama**:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *Örnek (kısaltılmış) Base64 çıktısı:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## Hata Yanıtları

| HTTP Durumu | Kod                    | Mesaj |
|-------------|------------------------|-------|
| `400`       | `InvalidParameter`     | Bir veya daha fazla istek parametresi geçersiz. |
| `401`       | `AuthenticationFailed` | Eksik veya geçersiz JWT belirteci. |
| `404`       | `PropertyNotFound`     | İstenen çalışma kitabını, çalışma sayfasını veya OLE nesnesini bulunamadı. |
| `500`       | `InternalError`        | Sunucuda beklenmeyen bir hata oluştu. |

---

## SDK Örnekleri

Aşağıdaki kod parçacıkları, resmi SDK’larla bu işlemi çağırma yöntemini göstermektedir. `YOUR_JWT_TOKEN` ve diğer yer tutucuları gerçek değerlerinizle değiştirin.

| Dil      | Örnek |
|----------|-------|
| **C#** | <details><summary>Kodu göster</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>Kodu göster</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>Kodu göster</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>Kodu göster</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>Kodu göster</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>Kodu göster</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>Kodu göster</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>Kodu göster</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(SDK’ların tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.)*

---

## İlgili İşlemler

- **OLE Nesnesi Ekle** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **OLE Nesnesini Güncelle** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **OLE Nesnesini Sil** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **OLE Nesne Listesini Al** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

Ayrıntılar için ilgili API referans sayfalarına bakın.

---

## Ek Kaynaklar

- **OpenAPI Spesifikasyonu** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **Kimlik Doğrulama Kılavuzu** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **SDK Deposu** – <https://github.com/aspose-cells-cloud>
- **Performans ve Erişilebilirlik** – Lighthouse ve axe-core denetimlerini çalıştırarak en iyi yükleme sürelerini ve WCAG 2.1 AA uyumluluğunu sağlayın.

---
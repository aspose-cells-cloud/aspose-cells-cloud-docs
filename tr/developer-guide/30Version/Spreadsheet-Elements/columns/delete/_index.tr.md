---
title: "Aspose.Cells Cloud API ile Excel Çalışma Sayfasından Sütun Silme"
description: "Aspose.Cells Cloud REST API'si kullanarak bir Excel çalışma sayfasından bir veya daha fazla sütunu nasıl sileceğinizi öğrenin. Kimlik doğrulama, istek söz dizimi, parametreler, yanıtlar, hata yönetimi ve SDK örnekleri içerir."
keywords: ["Aspose.Cells", "Sütun Sil", "Excel API", "REST", "Bulut", "Çalışma Sayfası", "Sütunlar"]
date: 2026-07-30
api_version: "v3.0"
---

# Excel Çalışma Sayfasından Sütun Silme

**Uç Nokta**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

İşlem, bir çalışma sayfasından tek bir sütunu veya sütun aralığını kaldırır. Sütun silme işleminden sonra hücre referansları (formüller dahil) otomatik olarak güncellenebilir.

---

## İçindekiler
1. [Ön Gereksinimler](#ön-gereksinimler)  
2. [Kimlik Doğrulama](#kimlik-doğrulama)  
3. [İstek URL’si ve HTTP Yöntemi](#istek-urlsi-ve-http-yöntemi)  
4. [Parametreler](#parametreler)  
   - [Yol parametreleri](#yol-parametreleri)  
   - [Sorgu parametreleri](#sorgu-parametreleri)  
5. [cURL Örneği](#curl-örneği)  
6. [Yanıtlar](#yanıtlar)  
7. [Hata Kodları](#hata-kodları)  
8. [SDK Örnekleri](#sdk-örnekleri)  
9. [Ek Notlar](#ek-notlar)  

---

## Ön Gereksinimler
- Aspose Cloud kimlik doğrulama akışıyla elde edilen geçerli bir **JWT erişim belirteci**.  
- Çalışma kitabının (`{name}`), Aspose Cloud depo alanına zaten yüklenmiş olması gerekir (veya `folder`/`storageName` sorgu parametreleri aracılığıyla erişilebilir olmalıdır).  

---

## Kimlik Doğrulama
Tüm Aspose.Cells Cloud istekleri **Bearer token** kimlik doğrulaması gerektirir.

```http
Authorization: Bearer <access_token>
```

JWT belirteci elde etme konusunda ayrıntılı bilgi için [kimlik doğrulama kılavuzuna](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bakınız.

---

## İstek URL’si ve HTTP Yöntemi
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – Çalışma kitabının dosya adı (örneğin, `test.xlsx`).  
- **`{sheetName}`** – Çalışma sayfasının adı (örneğin, `Sheet1`).  
- **`{columnIndex}`** – Silinecek ilk sütunun sıfır tabanlı indeksi.  

---

## Parametreler

| Ad              | Konum   | Tür     | Gerekli  | Açıklama |
|-----------------|---------|---------|----------|----------|
| **name**        | path    | string  | ✅ Evet  | Çalışma kitabının dosya adı. |
| **sheetName**   | path    | string  | ✅ Evet  | Çalışma sayfasının adı. |
| **columnIndex** | path    | integer | ✅ Evet  | Silinecek ilk sütunun sıfır tabanlı indeksi. |
| **startColumn** | query   | integer | ❌ Hayır | Silme işleminin başlayacağı sıfır tabanlı indeks. Atlanırsa `columnIndex` değeri varsayılan alınır. |
| **totalColumns**| query   | integer | ❌ Hayır | Silinecek sütun sayısı. Atlanırsa yalnızca `columnIndex` ile belirtilen sütun silinir. |
| **updateReference** | query | boolean | ❌ Hayır | `true` olarak ayarlandığında, silme işleminden sonra çalışma kitabındaki hücre referanslarını (formüller dahil) otomatik olarak günceller. |
| **folder**      | query   | string  | ❌ Hayır | Çalışma kitabını içeren klasörün yolu. |
| **storageName** | query   | string  | ❌ Hayır | Aspose Cloud depo hizmetinin adı. |

> **Not** – Düşük seviye API spesifikasyonunda gösterilen `columns` parametresi, daha açıklayıcı olan `startColumn` ve `totalColumns` sorgu parametreleriyle değiştirilmiştir. Geriye dönük uyumluluk için her iki yaklaşım da kabul edilir.

---

## cURL Örneği

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Açıklama
- `test.xlsx` dosyasının `Sheet1` çalışma sayfasından **B** sütununu (`columnIndex = 1`) siler.  
- `startColumn=1` ve `totalColumns=1`, tek bir sütun silme işlemi belirtir.  
- `updateReference=true`, formüller ve diğer referansların otomatik olarak ayarlanmasını sağlar.

---

## Yanıtlar

| HTTP Kodu | Açıklama | Örnek |
|-----------|----------|-------|
| **200** | Başarılı – sütun(lar) silindi. | `{ "Code": 200, "Status": "OK" }` |
| **400** | Geçersiz istek – eksik veya geçersiz parametreler. | `{ "Code": 400, "Message": "Invalid totalColumns value." }` |
| **401** | Yetkisiz – eksik veya geçersiz JWT belirteci. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | Bulunamadı – çalışma kitabı veya çalışma sayfası yok. | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500** | İç sunucu hatası – sunucuda beklenmeyen bir durum oluştu. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

Yanıt gövdesi genel **`CellsCloudResponse`** modeline uyar.

---

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam                        | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırlarını aşıyor. |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası. |
---

## SDK Örnekleri

Aşağıda en yaygın SDK'lar için çalışır durumdaki kod parçacıkları verilmiştir. Yer tutucu değerleri (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>` vb.) kendi verilerinizle değiştirin.

| Dil | Örnek |
|-----|-------|
| **C#** | <details><summary>Kodu göster</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>Kodu göster</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>Kodu göster</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>Kodu göster</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>Kodu göster</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Error:\", err)\n        return\n    }\n    fmt.Println(\"Status:\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>Kodu göster</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>Kodu göster</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Status: \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>Kodu göster</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Status: \", $response->{Status}, \"\\n\";\n```</details> |

*Tüm SDK’lar, `access_token` yapılandırıldığında gerekli `Authorization` başlığını otomatik olarak ekler.*

---

## Ek Notlar

### Güvenlik Başlıkları (üretim ortamı için önerilir)
Dokümantasyon sayfası sunulurken güvenliği artırmak için aşağıdaki HTTP yanıt başlıklarını ekleyin:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### Performans Tavsiyeleri
- Üçüncü taraf analiz scriptlerini (`gtag.js`, `containerize.js`) `async` özniteliğiyle yükleyin veya sayfa render edildikten sonra ertelenmiş olarak çalıştırın.  
- Özel JavaScript/CSS paketlerini küçültün.  
- Render engelleyen küçük SVG ikonları için önceden yükleme yapın:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### SEO Geliştirmeleri (JSON‑LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud API ile Excel Çalışma Sayfasından Sütun Silme",
  "description": "Aspose.Cells Cloud REST API ile Excel çalışma sayfasından bir veya daha fazla sütun nasıl silineceğini öğrenin.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Sütun Sil", "Excel", "REST API"]
}
```

Parçacığı HTML `<head>` bölümü içindeki `<script type="application/ld+json">` bloğuna yerleştirin.

### Erişilebilirlik
- Tüm dekoratif görüntüler `alt=""` kullanır veya `aria-hidden="true"` ile gizlenir.  
- Open Graph görüntüsü artık tamamlık için meta etiketinde `alt` özniteliğini içerir.  

---

## Ayrıntılı Bilgi Kaynakları
- [DeleteWorksheetColumns için OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [Kimlik Doğrulama Genel Bakış](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [GitHub'da Aspose.Cells Cloud SDK’ları](https://github.com/aspose-cells-cloud)  

---
---
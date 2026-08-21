---
title: "Excel Çalışma Sayfasında Satırları Kopyalama"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasındaki belirli tüm satırlardan veri ve biçimleri kopyalayın. Kimlik doğrulama, istek/yanıt ayrıntıları, hata işleme ve SDK örneklerini içerir."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Excel Çalışma Sayfasında Satırları Kopyalama <span style="float:right;">v3.0</span>

Bir çalışma sayfasından belirli tüm satırlardan veri ve biçimleri kopyalayın.

---

## Ön Gereksinimler

| # | Gereksinim |
|---|-------------|
| 1 | Geçerli bir **JWT** belirteci. [Kimlik doğrulama kılavuzuna](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bakınız. |
| 2 | Çalışma kitabının (`{name}`) seçilen **klasör**/**depolar** içinde zaten mevcut olması gerekir. |
| 3 | Hedef çalışma sayfasının (`{sheetName}`) çalışma kitabında mevcut olması gerekir. |
| 4 | (İsteğe bağlı) Dosya varsayılan konumda değilse **klasör** ve **storageName** bilgilerini bilmek. |

---

## Uç Nokta

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*Tüm yol parametreleri büyük/küçük harfe duyarlıdır.*

### Yol Parametreleri

| Parametre | Tür    | Gerekli | Açıklama |
|-----------|--------|---------|----------|
| `name`    | string | ✅ | Çalışma kitabının dosya adı (örn. `test.xlsx`). |
| `sheetName` | string | ✅ | Çalışma sayfasının adı (örn. `Sheet1`). |

### Sorgu Parametreleri

| Parametre            | Tür     | Gerekli | Açıklama |
|----------------------|---------|---------|----------|
| `sourceRowIndex`     | integer | ✅ | Kaynak satırın sıfır tabanlı indeksi. |
| `destinationRowIndex`| integer | ✅ | Satırların yerleştirileceği sıfır tabanlı indeks. |
| `rowNumber`          | integer | ✅ | Kopyalanacak satır sayısı. |
| `worksheet`          | string  | ❌ | Çalışma sayfası tanımlayıcısı; genellikle **sheetName** ile aynıdır. |
| `folder`             | string  | ❌ | Çalışma kitabını içeren klasörün yolu. |
| `storageName`        | string  | ❌ | Depolama hizmetinin adı. |

---

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Not**  
> `<jwt token>` ifadesini, kimlik doğrulama hizmetinden elde edilen geçerli bir JWT belirteci ile değiştirin.

---

## Başarılı Yanıt

| Kod | Açıklama |
|-----|----------|
| **200** | Satırlar başarıyla kopyalandı. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Yanıt gövdesi `CellsCloudResponse` türünden bir örnektir.

---

## Hata İşleme

| HTTP Kodu | Anlamı                               | Örnek Gövde |
|-----------|--------------------------------------|-------------|
| **400**   | Geçersiz İstek – eksik/geçersiz parametreler. | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**   | Yetkisiz – geçersiz veya eksik JWT belirteci. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Bulunamadı – çalışma kitabı veya çalışma sayfası mevcut değil. | `{ "Code": 404, "Message": "File not found." }` |
| **500**   | Sunucu İç Hatası – beklenmeyen sunucu koşulu. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**İşleme yönergeleri**

* **400** – Gerekli tüm sorgu parametrelerinin mevcut ve doğru biçimlendirildiğinden emin olun.  
* **401** – JWT belirtecini yeniden oluşturun veya yenileyin.  
* **404** – Çalışma kitabı ve çalışma sayfası adlarını doğrulayın ve dosyanın belirtilen klasör/depolamada mevcut olduğundan emin olun.  
* **500** – Kısa bir gecikmeden sonra yeniden deneyin; sorun devam ederse Aspose desteğiyle iletişime geçin.

---

## SDK Örnekleri

Aşağıdaki kod parçacıkları, resmi Aspose.Cells Cloud SDK'larıyla **Satırları Kopyala** işlemini nasıl çağıracağınızı göstermektedir.

| Dil | Örnek |
|-----|-------|
| **C#**   | <details><summary>Kodu göster</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>Kodu göster</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>Kodu göster</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>Kodu göster</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>Kodu göster</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>Kodu göster</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>Kodu göster</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>Kodu göster</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*Tüm kaynak dosyalar [Aspose‑Cells‑Cloud GitHub deposunda](https://github.com/aspose-cells-cloud) mevcuttur.*

---

## Ayrıntılı Bilgi

- [Excel Çalışma Sayfasında Satır Ekle](/rows/add/)  
- [Excel Çalışma Sayfasında Satır Sil](/rows/delete/)  
- [Excel Çalışma Sayfasında Satır Güncelle](/rows/update/)  

--- 

*Sayfa **{{DATE}}** tarihinde oluşturuldu. Bu API'nin en son sürümü için [OpenAPI spesifikasyonuna](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows) bakınız.*
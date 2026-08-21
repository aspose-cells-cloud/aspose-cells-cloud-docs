---
---
title: "Excel'de Bir Aralık İçin Satır Yüksekliğini Ayarla – Aspose.Cells Cloud API (v3.0)"
description: "Aspose.Cells Cloud REST API'sini kullanarak bir Excel çalışma sayfasındaki belirli bir aralıktaki satır yüksekliğini değiştirin.uç nokta, parametreler, cURL örneği, örnek yanıtlar ve birden fazla dil için SDK snippet'leri içerir."
keywords: "Aspose.Cells, satır yüksekliği, aralık, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Excel'de Bir Aralık İçin Satır Yüksekliğini Ayarla

Bu işlem, Aspose Cloud deposunda depolanan bir çalışma sayfasında belirtilen bir aralığın satır yüksekliğini günceller.

## Ön Gereksinimler / Kimlik Doğrulama

**Cells.ReadWrite** kapsamdaki Aspose Cloud OAuth hizmetinden bir JWT erişim belirteci almanız gerekir.

Belirteci, her isteğin `Authorization` başlığında şu şekilde dahil edin:

```http
Authorization: Bearer <jwt token>
```

Eğer bir belirteciniz yoksa, bir talepte bulunmak için **Aspose Cloud kimlik doğrulama kılavuzunu** takip edin.

## HTTP İsteği

| Yöntem | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Yol Parametreleri

| Ad | Tür | Açıklama |
|----|-----|----------|
| `name` | `string` | **Gerekli.** Bulutta depolanan Excel dosyasının adı. |
| `sheetName` | `string` | **Gerekli.** Hedef aralığı içeren çalışma sayfası. |

### Sorgu Parametreleri

| Ad | Tür | Gerekli | Açıklama |
|----|-----|---------|----------|
| `value` | `number` | **Evet** | Aralığa uygulanacak istenen satır yüksekliği (nokta cinsinden). |
| `folder` | `string` | Hayır | Dosyanın bulunduğu depodaki klasör yolu. |
| `storageName` | `string` | Hayır | Kullanılacak depolama hizmetinin adı (birden fazla depo yapılandırılmışsa). |

### İstek Gövdesi (JSON)

Gövde, hangi satırların etkileneceğini tanımlayan bir **Range** (Aralık) nesnesi içermelidir.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Range (Aralık) JSON Şeması

| Özellik | Tür | Gerekli | Açıklama |
|---------|-----|---------|----------|
| `FirstRow` | tamsayı | **Evet** | Aralıktaki ilk satırın sıfır tabanlı indeksi. |
| `RowCount` | tamsayı | **Evet** | Yüksekliğin uygulanacağı satır sayısı. |
| `FirstColumn` | tamsayı | Hayır | İlk sütunun sıfır tabanlı indeksi (sadece satır yüksekliği için isteğe bağlı). |
| `ColumnCount` | tamsayı | Hayır | Aralığın kapsadığı sütun sayısı (isteğe bağlı). |

Yalnızca yukarıda listelenen özellikler satır yüksekliği işlemi için kullanılır; ekstra alanlar yok sayılır.

## Örnek İstek

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

### Örnek Yanıt (Başarılı)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

Tüm yanıtlar bir sayısal `Code` ve insanın okuyabileceği bir `Status` (veya hata durumunda `Message`) içerir. Hata oluşursa ek olarak `ErrorDetails` bilgileri de sağlanabilir.

## SDK Örnekleri

Aşağıdaki snippet'ler, resmi Aspose.Cells Cloud SDK'larını kullanarak **Set Row Height for a Range** (Bir Aralık İçin Satır Yüksekliğini Ayarla) işlemini nasıl çağıracağınızı göstermektedir.

| Dil | Örnek |
|-----|-------|
| **C#** | <details><summary>Kodu göster</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>Kodu göster</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Kodu göster</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Kodu göster</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Row height set'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Kodu göster</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Kodu göster</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Kodu göster</summary>```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"context\"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = \"<jwt token>\"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ \"FirstRow\": 9, \"RowCount\": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), \"test.xlsx\", \"Sheet1\", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Kodu göster</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **Not:** Tüm SDK’lar, erişim belirteci yapılandırıldığında gerekli `Authorization: Bearer` başlığını otomatik olarak ekler.

## Ayrıca Bakınız

- **OpenAPI Specification** – Bu işlem için detaylı sözleşme: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Aspose.Cells Cloud SDK Repository** – Kaynak kodu ve ek dil bağlamaları: <https://github.com/aspose-cells-cloud>
- **Authentication Guide** – JWT belirteci nasıl alınır: <https://docs.aspose.cloud/cells/authentication/>

---
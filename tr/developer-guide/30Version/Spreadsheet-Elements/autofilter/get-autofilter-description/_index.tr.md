---
title: "Otomatik Filtre Al"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından Otomatik Filtre açıklamasını alın."
keywords: "Otomatik Filtre, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /tr/cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# Çalışma Sayfasından Otomatik Filtre Açıklamasını Alma

**Sürüm:** v3.0  
**Uç nokta:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **Not:** Tüm örnek istekler **HTTPS** kullanır. JWT jetonlarını güvenli olmayan bir bağlantı üzerinden asla göndermeyin.

---

## Genel Bakış

Bir **Otomatik Filtre**, kullanıcıların bir çalışma sayfasındaki satırları sütun değerlerine, renklere, özel kriterlere ve daha fazlasına göre filtrelemesini sağlar. Bu API, filtre sütunlarını, aralığını ve sıralama ayrıntılarını içeren tam Otomatik Filtre yapılandırmasını döndürür; böylece filtre ayarlarını programatik olarak inceleyebilir veya yeniden oluşturabilirsiniz.

---

## Ön Gereksinimler

| Gereksinim | Açıklama |
|-----------|----------|
| **Kimlik Doğrulama** | Geçerli bir JWT jetonu gerekli. [Kimlik doğrulama kılavuzuna](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bakın. |
| **Dosya konumu** | Çalışma kitabının Aspose Cloud Deposu'nda (veya bağlı harici bir depoda) bulunması gerekir. |
| **Desteklenen formatlar** | Aspose.Cells tarafından desteklenen tüm Excel formatları (örneğin, `.xlsx`, `.xls`, `.xlsm`). |
| **SDK (isteğe bağlı)** | SDK kullanmayı tercih ediyorsanız, uygun paketi yükleyin (örneğin, .NET için `dotnet add package Aspose.Cells-Cloud`). |

---

## İstek

### HTTP İsteği

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### Yol Parametreleri

| Parametre | Tür   | Açıklama |
|-----------|-------|----------|
| `name`      | string | **Gerekli.** Uzantısıyla birlikte çalışma kitabı dosya adı. |
| `sheetName` | string | **Gerekli.** Otomatik Filtre’nin alınacağı çalışma sayfası adı. |

### Sorgu Parametreleri

| Parametre   | Tür   | Açıklama |
|-------------|-------|----------|
| `folder`      | string | Çalışma kitabının bulunduğu depodaki klasör yolu. |
| `storageName` | string | Kullanılacak depo adı. |

### Güvenlik

API, **JWT jeton tabanlı kimlik doğrulama** kullanır. Jetonu `Authorization` başlığına ekleyin:

```http
Authorization: Bearer <your_jwt_token>
```

---

## İstek Örneği (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Yanıt

Hizmet, `AutoFilter` modelini sarmalayan bir JSON nesnesi döndürür.

### Başarılı Yanıt Şeması

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

### Yanıt Örneği

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

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|-----|-----------------------------|-----------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek                | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT jetonu. |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut limitini aşıyor. |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası. |
---

## SDK Örnekleri

İşlem, tüm Aspose.Cells Cloud SDK’larında mevcuttur. Aşağıda çalıştırılabilir örnek kod parçacıkları verilmiştir.

| Dil | Örnek |
|-----|-------|
| **C#** | <details><summary>Kodu göster</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>Kodu göster</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>Kodu göster</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>Kodu göster</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Kodu göster</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>Kodu göster</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>Kodu göster</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>Kodu göster</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

SDK’ların tam listesi ve kurulum talimatları için [Aspose.Cells Cloud GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

---

## Aşağıdakilere Bakın

- [Otomatik Filtre – OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [Kimlik doğrulama kılavuzu](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Depo işlemleri](https://docs.aspose.cloud/cells/storage/)  

---
---
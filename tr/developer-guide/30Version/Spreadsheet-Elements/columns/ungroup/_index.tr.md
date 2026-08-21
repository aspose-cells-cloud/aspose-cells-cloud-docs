---
title: Excel'de Sütunları Gruplamayı Kaldır – Aspose.Cells Cloud API  
description: Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasındaki sütun gruplamasını kaldırın. Uç nokta, parametreler, kimlik doğrulama, cURL örneği, yanıt biçimi ve SDK kod parçacıklarını içerir.  
keywords: Aspose.Cells, grup kaldırma, sütunlar, Excel, API, REST, bulut, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# Excel'de Sütunları Gruplamayı Kaldır  

Aspose.Cells Cloud, belirli bir çalışma sayfasından sütun gruplamasını kaldıran bir **POST** işlemi sağlar. Bu sayfa, istek biçimi, gerekli parametreler, kimlik doğrulama yöntemi, örnek çağrılar ve SDK kullanımı hakkında ayrıntılı bilgi verir.

---  

## Ön Gereksinimler  

| Gereksinim | Neden Gerekli |
|-----------|---------------|
| **Aspose Cloud hesabı** | Aspose.Cells Cloud hizmetlerine erişim için. |
| **JWT erişim belirteci** | Tüm API çağrıları, bearer token ile yetkilendirilmelidir. [JWT kimlik doğrulama kılavuzuna](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bakınız. |
| **Aspose Cloud depoda saklanan çalışma kitabı** | API, bulut depolama (veya bağlı harici depolama) içindeki dosyalar üzerinde çalışır. |
| **Çalışma sayfası adı** | Hedef çalışma sayfası, çalışma kitabında mevcut olmalıdır. |

---  

## Kimlik Doğrulama  

Tüm istekler, geçerli bir JWT belirteci içeren bir **Authorization** başlığı gerektirir:

```http
Authorization: Bearer <access_token>
```

Belirteç, Aspose Cloud OAuth akışı aracılığıyla elde edilir. Belirteçler sınırlı bir süre için geçerlidir; gerekli olduğunda yenilemelisiniz.

---  

## Uç Nokta  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Yol** – Çalışma kitabı dosya adı (örneğin `test.xlsx`).  
* `{sheetName}` – **Yol** – Çalışma sayfası adı (örneğin `Sheet1`).  

---  

## Parametreler  

### Yol Parametreleri  

| Ad | Tür | Gerekli | Açıklama |
|-----|-----|---------|----------|
| `name` | string | Evet | Çalışma kitabı dosya adı. |
| `sheetName` | string | Evet | Çalışma sayfası adı. |

### Sorgu Parametreleri  

| Ad | Tür | Gerekli | Açıklama |
|-----|-----|---------|----------|
| `firstIndex` | integer | Evet | Grubu kaldırılacak ilk sütunun sıfır tabanlı indeksi. |
| `lastIndex` | integer | Evet | Grubu kaldırılacak son sütunun sıfır tabanlı indeksi. |
| `folder` | string | Hayır | Çalışma kitabının bulunduğu klasör yolu. |
| `storageName` | string | Hayır | Dosyanın bulunduğu depolama hizmetinin adı. |

---  

## İstek Örneği (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*`<access_token>` ifadesini geçerli bir JWT belirteci ile değiştirin.*

---  

## Başarılı Yanıt  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

Yanıt nesnesi (`CellsCloudResponse`), başarıyla gruplaması kaldırılan sütun aralığını içerir.

### Hata Yanıtı  

İstek başarısız olursa, hizmet aşağıdaki alanları içeren bir JSON yükü döndürür:

| Alan | Anlamı |
|------|--------|
| `Code` | HTTP tarzı hata kodu (örneğin 400, 401). |
| `Status` | Hatayı kısa olarak tanımlar. |
| `ErrorMessage` | Hatanın ayrıntılı açıklaması. |

---  

**HTTP Durum Kodları**

| Kod | Anlam                      | Açıklama                                             |
|-----|----------------------------|------------------------------------------------------|
| 200 | OK                         | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                | Eksik veya geçersiz parametreler (örneğin desteklenmeyen dosya türü). |
| 401 | Unauthorized               | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large          | Yüklenecek dosya boyut sınırlarını aşıyor. |
| 500 | Internal Server Error      | Beklenmeyen sunucu hatası. |
---  

## SDK Kod Örnekleri  

Aşağıda, en popüler SDK’lar için çalışan hazır kod parçacıkları yer almaktadır. Yer tutucu değerleri (`<YourAccessToken>`, `<YourFileName>` vb.) kendi verilerinizle değiştirin.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Gruplaması kaldırılan sütunlar: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Gruplaması kaldırılan sütunlar: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Gruplaması kaldırılan sütunlar: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Gruplaması kaldırılan sütunlar: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Gruplaması kaldırılan sütunlar: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **Not:** PHP, Ruby, Perl ve diğer diller için SDK’lar aynı parametre sırasını takip eder. Tam örnekler için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakınız.

---  

## Kaynaklar  

* **OpenAPI Spesifikasyonu:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **Kimlik Doğrulama Kılavuzu:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **SDK Deposu:** <https://github.com/aspose-cells-cloud>

---  

## Değişiklik Geçmişi  

| Tarih | Yazar | Değişiklik |
|------|--------|------------|
| 2026‑07‑30 | AI Optimizer | UTF‑8 kodlaması düzeltildi, Ön Gereksinimler eklendi, meta anahtar kelimeler temizlendi, başlık hiyerarşisi iyileştirildi ve SDK kod parçacıkları eklendi. |
| 2026‑07‑29 | Orijinal | İlk belge taslağı. |

---
---
title: Dikey Sayfa Sonrasını Sil – Aspose.Cells Cloud REST API
description: Aspose.Cells Cloud REST API (v3.0) kullanarak bir Excel çalışma sayfasından dikey sayfa sonrasını kaldırın. İstek sözdizimi, parametreler, örnekler, yanıt kodları ve SDK kod parçacıklarını içerir.
keywords: dikey sayfa sonrasını sil, Aspose.Cells Cloud, REST API
slug: dikey-sayfa-sonrasi-sil
api_version: v3.0
---

# Dikey Sayfa Sonrasını Sil

Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabındaki bir çalışma sayfasından dikey sayfa sonrasını silin.

---

## Ön Gereksinimler

* `Authorization` başlığında bir **JWT kimlik doğrulama belirteci** sağlanmalıdır.  
* Çalışma kitabının (`{name}`), belirtilen **klasörde** veya **depolama biriminde** saklanmalı ve API istemcisine erişilebilir olmalıdır.

---

## HTTP İsteği

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| Parametre | Tür   | Konum | Zorunlu | Açıklama |
|-----------|--------|----------|----------|-------------|
| **name**      | string | yolda   | Evet | Excel dosyasının adı. |
| **sheetName** | string | yolda   | Evet | Sayfa sonrasını içeren çalışma sayfasının adı. |
| **index**     | integer| yolda   | Evet | Silinecek dikey sayfa sonrasının sıfır tabanlı indeksi. |
| **folder**    | string | sorgu  | Hayır | Dosyanın saklandığı klasör yolu. |
| **storageName**| string| sorgu  | Hayır | Depolama hizmetinin adı. |

---

## İstek Örneği

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Başarılı Yanıt

| Kod | Açıklama |
|------|-------------|
| **200** | Dikey sayfa sonrası başarıyla silindi. |

**Örnek yük**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Hata Yanıtları

| HTTP Kodu | Açıklama |
|-----------|-------------|
| **401** | Yetkisiz – eksik veya geçersiz belirteç. |
| **404** | Bulunamadı – belirtilen dosya, çalışma sayfası veya sayfa sonrası indeksi mevcut değil. |
| **400** | Geçersiz İstek – hatalı istek sözdizimi veya geçersiz parametreler. |
| **500** | Sunucu İç Hatası – beklenmeyen bir durumla karşılaşıldı. |

**Örnek hata yükleri**

*401 – Yetkisiz*

```json
{
  "Code": 401,
  "Message": "Geçersiz kimlik doğrulama belirteci."
}
```

*404 – Bulunamadı*

```json
{
  "Code": 404,
  "Message": "Belirtilen dosya, çalışma sayfası veya sayfa sonrası indeksi bulunamadı."
}
```

*400 – Geçersiz İstek*

```json
{
  "Code": 400,
  "Message": "İstek parametreleri geçersiz veya bozuk."
}
```

*500 – Sunucu İç Hatası*

```json
{
  "Code": 500,
  "Message": "Beklenmeyen bir sunucu hatası oluştu."
}
```

---

## SDK Kod Örnekleri

Aşağıdaki örnekler, çeşitli Aspose.Cells Cloud SDK’ları kullanarak **DeleteVerticalPageBreak** işlemini nasıl çağıracağınızı göstermektedir.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(PHP, Ruby, Perl ve diğer diller için SDK kod parçacıkları aynı deseni takip eder ve resmi GitHub Deposu’nda mevcuttur.)*

---

## İlgili Kaynaklar

* **OpenAPI Spesifikasyonu** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **Aspose.Cells Cloud SDK’ları** – <https://github.com/aspose-cells-cloud>  
* **Kimlik Doğrulama Kılavuzu** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*Belge son güncelleme tarihi: 2026‑07‑30*
---
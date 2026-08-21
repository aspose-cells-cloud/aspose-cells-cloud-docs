---
title: "Aspose.Cells Cloud API – Çalışma Sayfasından Liste Nesnesi (Tablo) Alın"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından bir ListObject (tablo) alın. Birden fazla formata (PDF, CSV, JSON, …) dışa aktarmayı destekler."
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - Tablo
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – Çalışma Sayfasından Liste Nesnesi (Tablo) Alın

Bir Excel çalışma kitabında belirli bir çalışma sayfasından bir **liste nesnesi** (aynı zamanda *tablo* olarak da bilinir) alın. Uç nokta, isteğe bağlı `format` sorgu parametresini kullanarak tabloyu doğrudan seçilen bir forma dışa aktarabilir.

---

## Öntanımlı Gereksinimler

| Gereksinim | Detaylar |
|----------|---------|
| **Kimlik Doğrulama** | Geçerli bir **JWT** (Bearer) jetonu gereklidir. Jetonu, [Kimlik Doğrulama kılavuzunda](/authentication/) açıklanan **OAuth2** kimlik doğrulama akışıyla edinin. |
| **Depolama** | Çalışma kitabının bir Aspose Cloud depolama konumunda bulunması gerekir. Dosya öntanımlı olmayan bir depolamada yer alıyorsa, `storageName` sorgu parametresini belirtin. |
| **Ortam Sınırları** | API, standart Aspose Cloud ortam sınırlama politikasını (öntanımlı = 100 istek/dakika/hesap) izler. |
| **SDK’lar (isteğe bağlı)** | Resmi SDK’lardan birini (C#, Java, Python, …) kullanmak, istek oluşturma ve yanıt işleme işlemlerini basitleştirir. Aşağıdaki **SDK Örnekleri** bölümüne bakın. |

---

## İstek

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Parametre | Tür | Konum | Gerekli | Açıklama |
|----------|-----|-------|---------|----------|
| **name** | `string` | Yol | ✔️ | Excel dosyasının adı (uzantı dahil). |
| **sheetName** | `string` | Yol | ✔️ | Liste nesnesini içeren çalışma sayfası. |
| **listobjectindex** | `integer` | Yol | ✔️ | Alınacak liste nesnesinin sıfır tabanlı indeksi. |
| **format** | `string` | Sorgu | ❌ | İstenen dışa aktarma formatı (örn. `pdf`, `csv`, `json`). |
| **folder** | `string` | Sorgu | ❌ | Çalışma kitabının bulunduğu klasör yolu. |
| **storageName** | `string` | Sorgu | ❌ | Kullanılacak Aspose Cloud depolama adı. |

#### Notlar

* Tüm çağrılar **mutlaka** HTTPS üzerinden yapılmalıdır.  
* `format` parametresi verildiğinde, yanıt gövdesi dışa aktarılan dosya akışıdır (örn. `application/pdf`).  
* `format` olmadan API, ListObject’in JSON açıklamasını döndürür.

---

## cURL Örneği

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*`<your_jwt_token>` ifadesini, kimlik doğrulama uç noktasından elde edilen geçerli bir JWT ile değiştirin.*

---

## Başarılı Yanıt (JSON)

**`format` parametresi verilmediğinde**, API ListObject’in açıklamasını içeren bir JSON yükü döndürür.

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**`format` parametresi verildiğinde**, yanıt gövdesi istenen dosya türünün ikili akışıdır (örn. `Content-Type: text/csv`).

---

## Hata Yönetimi

| HTTP Kodu | Anlamı | Örnek JSON |
|----------|--------|------------|
| **400** | Geçersiz istek – eksik veya geçersiz parametreler. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | Yetkisiz – eksik veya geçersiz JWT jetonu. | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | Bulunamadı – çalışma kitabı, çalışma sayfası veya liste nesnesi mevcut değil. | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | İç sunucu hatası. | `{"Code":500,"Message":"Unexpected server error."}` |

### Yaygın Hatalar (Notlar)

* **Sıfır tabanlı indeks** – `listobjectindex` **0**’dan başlar. İndeks `1` istendiğinde sayfadaki ikinci tablo döndürülür.  
* **Klasör ve depolama** – Çalışma kitabının bir alt klasörde bulunuyorsa, `folder` sorgu parametresini dahil edin (örn. `?folder=Reports/2024`).  
* **Dışa aktarma formatı** – Yalnızca Aspose.Cells dönüştürme motoru tarafından desteklenen formatlar geçerlidir (`pdf`, `xlsx`, `csv`, `json`, …). Desteklenmeyen bir değer verildiğinde **400** hatası oluşur.

---

## SDK Örnekleri

Aşağıdaki kod parçacıkları, resmi Aspose.Cells Cloud SDK’larını kullanarak uç noktayı çağırma yöntemlerini göstermektedir. Yer tutucu değerleri (`<YOUR_CLIENT>`, `<YOUR_JWT>` vb.) gerçek yapılandırma bilgilerinizle değiştirin.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API istemcisini başlat
var apiInstance = new ListObjectsApi();

// İsteği oluştur
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // örn. dışa aktarmak için "csv"
    folder: null,
    storageName: null
);

// Gerçekleştir
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## Ayrıca Bakınız

| İlgili uç nokta | Açıklama |
|----------------|----------|
| **Liste Nesnesi Ekle** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – yeni bir tablo oluşturur. |
| **Liste Nesnesini Güncelle** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – tablo özelliklerini değiştirir. |
| **Liste Nesnesini Sil** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – bir tabloyu kaldırır. |
| **Tüm Liste Nesnelerini Listele** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – bir çalışma sayfasındaki tabloları numaralandırır. |

---

## Kaynaklar

* **OpenAPI belirtimi** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **Kimlik Doğrulama kılavuzu** – <https://docs.aspose.cloud/cells/authentication/>  
* **GitHub deposu (SDK’lar)** – <https://github.com/aspose-cells-cloud>  

---
---
---
---
title: Koşullu Biçimlendirmeye Hücre Alanı Ekle
description: Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasındaki bir koşullu biçimlendirme kuralına bir hücre alanı ekleyin. Endpoint, parametreler, cURL ve SDK örnekleri, yanıt şeması ve hata işleme içerir.
keywords: Aspose.Cells, Koşullu Biçimlendirme, CellArea, REST API, Excel, Bulut SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# Koşullu Biçimlendirmeye Hücre Alanı Ekle

**Özet** – Çalışma sayfasındaki mevcut bir koşullu biçimlendirme kuralına bir hücre alanı ekler.

---

## Önyüklemeler

1. **Aspose.Cells Cloud hesabı** – **Uygulama SID'nizi** ve **Uygulama Anahtarınızı** edinin.  
2. **JWT jetonu** – Uygulama SID/Anahtarını kullanarak bir JWT jetonu oluşturun (bakınız [Kimlik Doğrulama Kılavuzu](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. Hedef Excel dosyası, belirtilen depolama/klasörde zaten mevcut olmalıdır.

---

## Kimlik Doğrulama

Tüm çağrılar **JWT jeton tabanlı kimlik doğrulama** gerektirir. Jetonu `Authorization` başlığına ekleyin:

```http
Authorization: Bearer <jwt token>
```

---

## HTTP İsteği

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Yol Parametreleri

| Ad          | Tür    | Açıklama                                  |
|-------------|--------|-------------------------------------------|
| `name`      | string | Excel dosyası adı (örn. `Book1.xlsx`).    |
| `sheetName` | string | Kuralı içeren çalışma sayfası (örn. `Sheet1`). |
| `index`     | integer| Koşullu biçimlendirme kuralının sıfır tabanlı indeksi. |

### Sorgu Parametreleri

| Ad             | Tür    | Gerekli | Açıklama                                      |
|----------------|--------|---------|-----------------------------------------------|
| `cellArea`     | string | **Evet**| Eklenecek hücre aralığı, A1 gösterimiyle (örn. `A1:C3`). |
| `folder`       | string | Hayır   | Dosyanın depolandığı klasör yolu.             |
| `storageName`  | string | Hayır   | Depolama hizmeti adı.                         |

---

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Beklenen Başarılı Yanıt

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**Yanıt şeması – `CellArea`**

| Özellik        | Tür | Açıklama                              |
|----------------|-----|---------------------------------------|
| `StartRow`     | int | İlk satırın sıfır tabanlı indeksi.    |
| `StartColumn`  | int | İlk sütunun sıfır tabanlı indeksi.    |
| `EndRow`       | int | Son satırın sıfır tabanlı indeksi.    |
| `EndColumn`    | int | Son sütunun sıfır tabanlı indeksi.    |

---

**HTTP Durum Kodları**

| Kod | Anlam                     | Açıklama                                              |
|-----|---------------------------|-------------------------------------------------------|
| 200 | OK (Tamam)                | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)| Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT jetonu.                       |
| 413 | Payload Too Large (İçerik Çok Büyük)| Yüklenecek dosya boyut sınırını aşıyor.       |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                 |
---

## SDK Örnekleri

Aşağıda en yaygın SDK'lar için kısa kod parçaları verilmiştir. `YOUR_APP_SID` ve `YOUR_APP_KEY` değerlerini kendi kimlik bilgilerinizle değiştirin ve gerektiği yerde oluşturulan JWT jetonunu ayarlayın.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## Notlar ve İpuçları

- **Hücre Alanı biçimi** – Geçerli bir A1 aralığı olmalıdır (`A1`, `A1:C3`, `Sheet2!B2:D5`). Geçersiz biçimler **400 Hatalı İstek** döndürür.
- **Örtüşen alanlar** – Aynı kuralın mevcut bir alanı ile örtüşen bir aralık eklemek **409 Çakışma** hatasına neden olur.
- **Sıfır tabanlı indeksleme** – Yanıttaki satır/sütun indeksleri `0` ile başlar. Gerekirse Excel'in 1‑tabanlı gösterimine dönüştürün.
- **Depolama** – `folder` ve `storageName` parametrelerini atlerseniz API varsayılan depolama/kök klasörü kullanır.

---

## İlgili İşlemler

- **Hücre Alanını Sil** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **Koşullu Biçimlendirmeye Koşul Ekle** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **Koşullu Biçimlendirmeyi Al** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

Bu işlemler bir araya getirilerek tam koşullu biçimlendirme iş akışları oluşturulabilir.

---
---
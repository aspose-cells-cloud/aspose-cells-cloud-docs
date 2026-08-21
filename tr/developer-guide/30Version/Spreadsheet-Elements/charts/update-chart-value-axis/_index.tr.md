---
title: "Aspose.Cells Cloud API – Grafik Değer Ekseni Güncelle (POST /valueaxis)"
description: "Aspose.Cells Cloud REST API'sini kullanarak bir Excel çalışma sayfasındaki bir grafik değer eksenisini güncelleyin.uç nokta, parametreler, istek-gövdesi şeması, örnekler (cURL ve SDK’lar), yanıtlar ve hata işleme içerir."
keywords:
  - Aspose.Cells Cloud
  - Grafik Değer Ekseni Güncelle
  - REST API
  - Excel grafik eksen
  - POST valueaxis
  - cURL örneği
  - SDK
  - JSON yükü
  - grafik eksen ayarları
last_updated: 2026-07-30
---

# Grafik Değer Ekseni Güncelle (POST /valueaxis)

**Özet:**  
Aspose Cloud deposunda depolanan bir Excel çalışma kitabında belirli bir grafik değer eksenini değiştirin. Tek bir istekte sınırları, küçük ve büyük ölçek birimlerini, logaritmik ölçeklendirmeyi ve diğer eksen özelliklerini ayarlayabilirsiniz.

---

## Ön Koşullar

1. **JWT erişim belirteci** – Belirteci [Kimlik Doğrulama kılavuzunda](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) açıklanan şekilde edinin.  
2. Hedef **çalışma kitabının** zaten Aspose Cloud deposuna (veya varsayılan depoya) yüklenmiş olması gerekir.  
3. Değiştirmek istediğiniz **çalışma sayfası adını** ve **sıfırdan başlayarak grafik dizinini** bilmelisiniz.

---

## Uç Nokta

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*Yer tutucuları gerçek değerlerinizle değiştirin.*

| Yer Tutucu | Açıklama |
|-----------|----------|
| `{name}` | Excel dosyasının adı (örneğin, `Book1.xlsx`). |
| `{sheetName}` | Grafik içeren çalışma sayfası (örneğin, `Sheet1`). |
| `{chartIndex}` | Grafik için sıfırdan başlayarak dizin (örneğin, `0`). |

---

## Kimlik Doğrulama

API, **JWT belirteci tabanlı kimlik doğrulama** kullanır. Belirteci `Authorization` başlığına ekleyin:

```
Authorization: Bearer <jwt token>
```

---

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

## İstek Parametreleri

| Ad            | Konum   | Tür     | Gerekli | Açıklama |
|---------------|---------|---------|---------|----------|
| **name**      | Yol     | string  | Evet    | Bulutta depolanan Excel dosyası adı. |
| **sheetName** | Yol     | string  | Evet    | Grafik içeren çalışma sayfası. |
| **chartIndex**| Yol     | int     | Evet    | Güncellenecek grafik için sıfırdan başlayarak dizin. |
| **axis**      | Gövde   | object  | Evet    | Eksen ayarları (*İstek Gövdesi Şeması* bölümüne bakın). |
| **folder**    | Sorgu   | string  | Hayır   | Dosyanın bulunduğu bulut klasör yolu. |
| **storageName**| Sorgu  | string  | Hayır   | Kullanılacak depolama hizmetinin adı. |

---

## İstek Gövdesi Şeması (`axis` nesnesi)

Yalnızca değiştirmek istediğiniz özellikleri belirtmeniz yeterlidir.

| Özellik        | Tür      | Gerekli | Açıklama |
|----------------|----------|---------|----------|
| `minimum`      | number   | Hayır   | Eksenin alt sınırı. |
| `maximum`      | number   | Hayır   | Eksenin üst sınırı. |
| `majorUnit`    | number   | Hayır   | Büyük işaretleme aralığı. |
| `minorUnit`    | number   | Hayır   | Küçük işaretleme aralığı. |
| `logBase`      | number   | Hayır   | `isLogarithmic` değeri `true` olduğunda kullanılan logaritma tabanı. |
| `isLogarithmic`| boolean  | Hayır   | Eksenin logaritmik ölçek kullanıp kullanmadığı. |
| `displayUnit`  | string   | Hayır   | Eksen üzerinde gösterilen birim etiketi (örneğin, `"Binlerce"`). |
| `tickMark`     | string   | Hayır   | İşaret stili (`"inside"`, `"outside"`, vb.). |
| `crossAt`      | number   | Hayır   | Eksenin dik eksenle kesiştiği konum. |

### Örnek İstek Gövdesi

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Birimler",
  "tickMark": "inside",
  "crossAt": 0
}
```

---

## Örnek İstekler

### cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/<code class=\"placeholder\">{name}</code>/worksheets/<code class=\"placeholder\">{sheetName}</code>/charts/<code class=\"placeholder\">{chartIndex}</code>/valueaxis?folder=<code class=\"placeholder\">{folder}</code>&storageName=<code class=\"placeholder\">{storageName}</code>" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false,
        "displayUnit": "Birimler",
        "tickMark": "inside",
        "crossAt": 0
      }'
```

### SDK Örnekleri  

{{< tabs tabTotal="10" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new ChartsApi("client_id", "client_secret");
var axis = new Axis()
{
    Minimum = 0,
    Maximum = 200,
    MajorUnit = 20,
    MinorUnit = 5,
    LogBase = 10,
    IsLogarithmic = false,
    DisplayUnit = "Birimler",
    TickMark = "inside",
    CrossAt = 0
};

var response = api.PostChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
Console.WriteLine($"Durum: {response.Status}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.Axis;

ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Birimler")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
System.out.println("Değer eksen güncellendi.");
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ChartsApi;
use Aspose\Cells\Cloud\Model\Axis;

$api = new ChartsApi('client_id', 'client_secret');
$axis = new Axis([
    'minimum' => 0,
    'maximum' => 200,
    'majorUnit' => 20,
    'minorUnit' => 5,
    'logBase' => 10,
    'isLogarithmic' => false,
    'displayUnit' => 'Birimler',
    'tickMark' => 'inside',
    'crossAt' => 0
]);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
echo "Değer eksen güncellendi.\n";
?>
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ChartsApi.new('client_id', 'client_secret')
axis = AsposeCellsCloud::Axis.new(
  minimum: 0,
  maximum: 200,
  majorUnit: 20,
  minorUnit: 5,
  logBase: 10,
  isLogarithmic: false,
  displayUnit: 'Birimler',
  tickMark: 'inside',
  crossAt: 0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
puts 'Değer eksen güncellendi.'
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```python
from asposecellscloud import ChartsApi, Axis

api = ChartsApi('client_id', 'client_secret')
axis = Axis(
    minimum=0,
    maximum=200,
    majorUnit=20,
    minorUnit=5,
    logBase=10,
    isLogarithmic=False,
    displayUnit='Birimler',
    tickMark='inside',
    crossAt=0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
print('Değer eksen güncellendi.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Node.js örneği
const { ChartsApi, Axis } = require('asposecellscloud');

const api = new ChartsApi('client_id', 'client_secret');
const axis = new Axis({
    minimum: 0,
    maximum: 200,
    majorUnit: 20,
    minorUnit: 5,
    logBase: 10,
    isLogarithmic: false,
    displayUnit: 'Birimler',
    tickMark: 'inside',
    crossAt: 0
});

api.postChartValueAxis('Book1.xlsx', 'Sheet1', 0, axis)
   .then(response => console.log('Değer eksen güncellendi.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Android (Java) örneği
ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Birimler")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```swift
import AsposeCellsCloud

let api = ChartsApi(clientId: "client_id", clientSecret: "client_secret")
var axis = Axis()
axis.minimum = 0
axis.maximum = 200
axis.majorUnit = 20
axis.minorUnit = 5
axis.logBase = 10
axis.isLogarithmic = false
axis.displayUnit = "Birimler"
axis.tickMark = "inside"
axis.crossAt = 0

api.postChartValueAxis(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, axis: axis) { result, error in
    if let error = error {
        print("Hata: \\(error)")
    } else {
        print("Değer eksen güncellendi.")
    }
}
```
{{< /tab >}}

{{< tab tabNum="9" >}}
```perl
use Aspose::Cells::Cloud::Api::ChartsApi;
use Aspose::Cells::Cloud::Model::Axis;

my $api  = ChartsApi->new('client_id', 'client_secret');
my $axis = Axis->new(
    minimum        => 0,
    maximum        => 200,
    majorUnit      => 20,
    minorUnit      => 5,
    logBase        => 10,
    isLogarithmic  => JSON::false,
    displayUnit    => 'Birimler',
    tickMark       => 'inside',
    crossAt        => 0
);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
print "Değer eksen güncellendi.\n";
```
{{< /tab >}}

{{< tab tabNum="10" >}}
```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client_id", "client_id")
    cfg.AddDefaultHeader("client_secret", "client_secret")
    client := api.NewAPIClient(cfg)

    axis := model.Axis{
        Minimum:       0,
        Maximum:       200,
        MajorUnit:     20,
        MinorUnit:     5,
        LogBase:       10,
        IsLogarithmic: false,
        DisplayUnit:   "Birimler",
        TickMark:      "inside",
        CrossAt:       0,
    }

    _, err := client.ChartsApi.PostChartValueAxis(context.Background(), "Book1.xlsx", "Sheet1", 0, axis)
    if err != nil {
        fmt.Println("Hata:", err)
    } else {
        fmt.Println("Değer eksen güncellendi.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## Yanıtlar

### Başarılı (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Yanıt türü `CellsCloudResponse`'dır.

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |
---

## Ek Kaynaklar

- **OpenAPI Spesifikasyonu** – [JSON‑YAML’i görüntüle / indir](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **SDK Depo** – <https://github.com/aspose-cells-cloud>  
- **Kimlik Doğrulama kılavuzu** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*Herhangi bir sorunuz veya geri bildiriminiz için lütfen Aspose.Cells Cloud destek ekibiyle iletişime geçin.*
---
title: "Grafiğin İkinci Kategori Ekseni Alın"
type: docs
url: /tr/charts/second-category-axis/get/
weight: 60
keywords: "Grafiğin İkinci Kategori Ekseni Alın, Aspose.Cells Cloud API, Excel grafik eksi, REST API, ikinci-kategori eksen, Aspose.Cells"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki bir grafiğin ikinci kategori eksenini alın. İstek formatını, parametreleri, örnek cURL’i, yanıt şemasını, durum kodlarını ve kullanım notlarını içerir."
ArticleTitle: "Grafiğin İkinci Kategori Ekseni Alın – Aspose.Cells Cloud API"
---

Bu REST API, bir grafiğin **ikinci kategori eksenini** alır.

## GetChartSecondCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür    | Parametre Konumu (yol/sorgu) | Açıklama                                            |
| -------------- | ------- | ------------------------------- | ------------------------------------------------------ |
| name           | string  | path                            | Bulutta depolanan Excel dosyasının adı.            |
| sheetName      | string  | path                            | Grafiği içeren çalışma sayfasının adı.         |
| chartIndex     | integer | path                            | Ekseni istenen grafiğin sıfır tabanlı dizini. |
| folder         | string  | query                           | Dosyanın bulunduğu depodaki klasör yolu.  |
| storageName    | string  | query                           | Kullanılacak Aspose Cloud depo adı (isteğe bağlı).    |

### **Yanıt**

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "İkinci Kategori Ekseni",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                     | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (Tamam)                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)                 | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)                | Geçersiz veya eksik JWT belirteci. |
| 413  | Payload Too Large (Çok Büyük Yük)           | Yüklenecek dosya boyut sınırını aşıyor. |
| 500  | Internal Server Error (İç Sunucu Hatası)       | Beklenmeyen sunucu hatası. |
## GetChartSecondCategoryAxis API’sinin SDK’larla Nasıl Kullanılır

### GetChartSecondCategoryAxis API Spesifikasyonu

**GetChartSecondCategoryAxis** işlemi, [OpenAPI Spesifikasyonu’nda](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) tanımlanmıştır ve bir web tarayıcısından veya herhangi bir HTTP istemcisinden doğrudan REST etkileşimlerini sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için `cURL` komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, API’yi `cURL` ile nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "İkinci Kategori Ekseni",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

Bu API’yi projenize entegre etmenin en hızlı yolu SDK kullanmaktır. SDK’lar, kimlik doğrulama, istek oluşturma ve yanıt ayrıştırma gibi düşük seviye ayrıntıları işler, böylece iş mantığına odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesine [GitHub deposunda](https://github.com/aspose-cells-cloud) ulaşabilirsiniz.

Aşağıdaki kod örnekleri, **Grafiğin İkinci Kategori Ekseni Alın** işlemini çeşitli SDK’larla nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API istemcisini yapılandır
var config = new Configuration
{
    ClientId = "<your-client-id>",
    ClientSecret = "<your-client-secret>"
};
var apiInstance = new ChartsApi(config);

// İsteği oluştur
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// Çalıştır
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Eksen Adı: {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // API istemcisini yapılandır
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // İsteği oluştur
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // Çalıştır
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Eksen Adı: " + response.getAxis().getName());
    }
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
use Aspose\Cells\Cloud\Sdk\Api\ChartsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;
use Aspose\Cells\Cloud\Sdk\Model\Requests\GetChartSecondCategoryAxisRequest;

// Yapılandır
$config = new Configuration();
$config->setClientId('<your-client-id>');
$config->setClientSecret('<your-client-secret>');

$apiInstance = new ChartsApi($config);

$request = new GetChartSecondCategoryAxisRequest(
    'Sample.xlsx',       // name
    'Sheet1',            // sheetName
    0,                   // chartIndex
    'Documents',         // folder
    null                 // storageName
);

try {
    $result = $apiInstance->getChartSecondCategoryAxis($request);
    echo "Eksen Adı: " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'ChartsApi->getChartSecondCategoryAxis çağrılırken istisna: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# SDK’yı yapılandır
config = AsposeCellsCloud::Configuration.new
config.client_id = '<your-client-id>'
config.client_secret = '<your-client-secret>'

api_instance = AsposeCellsCloud::ChartsApi.new

begin
  result = api_instance.get_chart_second_category_axis(
    name: 'Sample.xlsx',
    sheet_name: 'Sheet1',
    chart_index: 0,
    folder: 'Documents'
  )
  puts "Eksen Adı: #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "ChartsApi->get_chart_second_category_axis çağrılırken istisna: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# API istemcisini yapılandır
config = asposecellscloud.Configuration()
config.client_id = '<your-client-id>'
config.client_secret = '<your-client-secret>'

api_instance = ChartsApi(asposecellscloud.ApiClient(config))

request = GetChartSecondCategoryAxisRequest(
    name='Sample.xlsx',
    sheet_name='Sheet1',
    chart_index=0,
    folder='Documents'
)

try:
    response = api_instance.get_chart_second_category_axis(request)
    print('Eksen Adı:', response.axis.name)
except ApiException as e:
    print('ChartsApi->get_chart_second_category_axis çağrılırken istisna:', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Aspose.Cells Cloud SDK kullanarak Node.js örneği
const { ChartsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    clientId: '<your-client-id>',
    clientSecret: '<your-client-secret>'
});
const api = new ChartsApi(config);

(async () => {
    try {
        const response = await api.getChartSecondCategoryAxis({
            name: 'Sample.xlsx',
            sheetName: 'Sheet1',
            chartIndex: 0,
            folder: 'Documents'
        });
        console.log('Eksen Adı:', response.axis.name);
    } catch (error) {
        console.error('Hata:', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) örneği; Aspose.Cells Cloud SDK for Android kullanır
import com.aspose.cells.cloud.sdk.api.ChartsApi;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.model.requests.*;

public class GetSecondCategoryAxisAndroid {
    public void execute() {
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        try {
            AxisResponse response = api.getChartSecondCategoryAxis(request);
            System.out.println("Eksen Adı: " + response.getAxis().getName());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
import AsposeCellsCloud

let config = Configuration(clientId: "<your-client-id>", clientSecret: "<your-client-secret>")
let api = ChartsApi(configuration: config)

let request = GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: nil
)

api.getChartSecondCategoryAxis(request: request) { result, error in
    if let axis = result?.axis {
        print("Eksen Adı: \(axis.name ?? "")")
    } else if let err = error {
        print("Hata: \(err)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
use Aspose::Cells::Cloud::Sdk::Api::ChartsApi;
use Aspose::Cells::Cloud::Sdk::Configuration;

my $config = Aspose::Cells::Cloud::Sdk::Configuration->new(
    client_id     => '<your-client-id>',
    client_secret => '<your-client-secret>'
);
my $api = Aspose::Cells::Cloud::Sdk::Api::ChartsApi->new($config);

my $response = $api->get_chart_second_category_axis(
    name        => 'Sample.xlsx',
    sheet_name  => 'Sheet1',
    chart_index => 0,
    folder      => 'Documents'
);
print "Eksen Adı: " . $response->axis->name . "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.ClientId = "<your-client-id>"
    cfg.ClientSecret = "<your-client-secret>"

    apiInstance := api.NewChartsApi(cfg)

    request := asposecellscloud.GetChartSecondCategoryAxisRequest{
        Name:      "Sample.xlsx",
        SheetName: "Sheet1",
        ChartIndex: 0,
        Folder:    "Documents",
        StorageName: nil,
    }

    result, _, err := apiInstance.GetChartSecondCategoryAxis(request)
    if err != nil {
        fmt.Println("Hata:", err)
        return
    }
    fmt.Println("Eksen Adı:", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}
---
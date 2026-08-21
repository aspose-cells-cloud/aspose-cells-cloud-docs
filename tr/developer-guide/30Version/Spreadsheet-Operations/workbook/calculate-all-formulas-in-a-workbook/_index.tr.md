---
title: "Excel Çalışma Kitabındaki Tüm Formülleri Hesapla"
second_title: "Belge"
linktitle: "Hesapla"
type: docs
url: /tr/calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, formülleri hesapla, Excel API, bulut SDK"
description: "Aspose.Cells Cloud REST API aracılığıyla bir Excel çalışma kitabındaki her formülü hesaplayın. cURL örneği, istek parametreleri, yanıt şeması, ön koşullar ve birden fazla dil için SDK kod parçacıklarını içerir."
weight: 140
ArticleTitle: "Excel Çalışma Kitabındaki Tüm Formülleri Hesapla"
---

Bu REST API, bir Excel çalışma kitabındaki **tüm formülleri** hesaplar.

**Ön Koşullar:** Bu uç noktayı çağırmadan önce şunlardan emin olun:
- Geçerli bir JWT kimlik doğrulama belirteci. ([Kimlik Doğrulama Kılavuzu](/tr/authentication/) bakın.)
- Aspose.Cells Cloud istemci kimliğiniz ve sırrınız.
- Hedef çalışma kitabının belirlenmiş depolama konumuna yüklenmiş olması. ([Depolama Kurulumu](/tr/storage/) bakın.)

## PostWorkbookCalculateFormula API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı   | Tür                 | Konum  | Açıklama                                                                                |
| ----------------- | ------------------- | ------ | ----------------------------------------------------------------------------------------- |
| **name**          | string              | path   | Çalışma kitabının dosya adı.                                                              |
| **options**       | CalculationOptions  | body   | Hesaplama ayarlarını belirleyen JSON nesnesi (örn. `CalcStackSize`, `IgnoreError`).     |
| **ignoreError**   | boolean             | query  | `true` olarak ayarlandığında, hesaplama sırasında karşılaşılan hatalar yoksayılır.       |
| **folder**        | string              | query  | Çalışma kitabını içeren klasörün yolu.                                                    |
| **storageName**   | string              | query  | Çalışma kitabının depolandığı depolama hizmetinin adı.                                   |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### Yanıt Detayları

| Alan               | Tür    | Açıklama                                                               |
| ------------------ | ------ | ----------------------------------------------------------------------- |
| **Code**           | int    | HTTP benzeri durum kodu (200 başarıyı belirtir).                         |
| **Status**         | string | Sonucun kısa metinsel açıklaması (örn. `OK`).                            |
| **WorkbookUrl**    | string | Güncellenmiş çalışma kitabının indirilebileceği doğrudan URL.            |
| **ErrorMessage**   | string | İstek başarısız olduğunda detaylı hata bilgisi; başarı durumunda `null`. |

#### Sonraki Adımlar / Yaygın Hatalar

- **Hesaplama hatalarını yönetin** – Bir formül değerlendirilemediğinde hata yanıtı almak için `ignoreError=false` ayarlayın.
- **Oran sınırlama farkındalığı** – `X-RateLimit-Remaining` başlığını kontrol edin; `0` değerine ulaşırsa yeniden denemeden önce bekleyin.
- **HTTP durum kodu yönlendirmesi**:
  - `400` – Geçersiz istek parametreleri.
  - `401` – Kimlik doğrulama başarısız (geçersiz veya süresi dolmuş JWT).
  - `404` – Çalışma kitabı bulunamadı.
  - `500` – Sunucu tarafı hatası; devam ederse Aspose desteğiyle iletişime geçin.

| Kod | Anlamı                | Ne Zaman Döndürülür                                        |
|-----|------------------------|-------------------------------------------------------------|
| 400 | Bad Request (Geçersiz İstek) | Geçersiz istek parametreleri veya bozuk JSON.                |
| 401 | Unauthorized (Yetkisiz)      | Eksik, geçersiz veya süresi dolmuş JWT belirteci.             |
| 404 | Not Found (Bulunamadı)       | Belirtilen çalışma kitabı depolamada mevcut değil.            |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu tarafı hatası; Aspose desteğiyle iletişime geçin. |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}
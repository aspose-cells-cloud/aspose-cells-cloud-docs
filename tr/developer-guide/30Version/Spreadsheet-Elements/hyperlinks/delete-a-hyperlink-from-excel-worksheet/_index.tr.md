---
title: "Çalışma Sayfası Bağlantısını Sil"
type: docs
url: /tr/hyperlinks/delete/
description: "Aspose.Cells Cloud API'si ile bir çalışma sayfası bağlantısını dizin numarasına göre silin. Gerekli parametreleri, kimlik doğrulamayı öğrenin ve C#, Java, Python ve daha fazlası için kod örneklerini görün."
keywords: "Aspose.Cells, Bulut, bağlantı sil, Excel API, REST, çalışma sayfası bağlantısı"
ArticleTitle: "Çalışma Sayfası Bağlantısını Sil – Aspose.Cells Cloud API Dokümantasyonu"
weight: 40
---

Bu REST API, bir Excel çalışma sayfasındaki bir bağlantı dizin numarasına göre bağlantıyı siler.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

### REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### İstek Parametreleri

| Parametre Adı      | Tür     | Konum | Zorunlu | Açıklama                                                      |
| ------------------ | ------- | ----- | ------- | ------------------------------------------------------------- |
| **name**           | string  | path  | ✅      | Excel belgesinin adı.                                         |
| **sheetName**      | string  | path  | ✅      | Çalışma sayfasının adı.                                        |
| **hyperlinkIndex** | integer | path  | ✅      | Silinecek bağlantının sıfır tabanlı dizin numarası.           |
| **folder**         | string  | query | ❌      | Belgeyi içeren klasör (varsayılan: root).                     |
| **storageName**    | string  | query | ❌      | Depolama hizmetinin adı (atlanırsa varsayılan depolama kullanılır). |

#### Yanıtlar

| Durum Kodu                    | Açıklama                                                | Örnek Gövde                                        |
| ----------------------------- | ------------------------------------------------------- | ------------------------------------------------- |
| **200 OK**                    | Bağlantı başarıyla silindi.                             | `{"Code":200,"Status":"OK"}`                      |
| **400 Bad Request**           | Eksik veya geçersiz parametreler.                       | `{"Code":400,"Message":"Geçersiz hyperlinkIndex."}` |
| **401 Unauthorized**          | Kimlik doğrulama belirteci eksik veya geçersiz.         | `{"Code":401,"Message":"Geçersiz erişim belirteci."}` |
| **404 Not Found**             | Dosya, çalışma sayfası veya bağlantı dizin numarası yok. | `{"Code":404,"Message":"Kaynak bulunamadı."}`     |
| **500 Internal Server Error** | Beklenmeyen sunucu hatası.                             | `{"Code":500,"Message":"İç sunucu hatası."}`      |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API'yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Paketi

Bir SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviyeli detayları yöneterek projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK'lar kullanarak nasıl çağıracağınızı göstermektedir. Güvenlik amacıyla satır içi kod parçacıkları sağlanmıştır; referans olması için orijinal Gist bağlantısı korunmuştur.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// Kaynak: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// Kaynak: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// Kaynak: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
// Kaynak: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// Kaynak: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Bağlantı silindi"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
// Kaynak: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Bağlantı silindi')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
// Kaynak: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// Kaynak: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Bağlantı silindi")
    }
}
```

{{< /tab >}}

{{< /tabs >}}
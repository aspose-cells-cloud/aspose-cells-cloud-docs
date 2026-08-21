---
title: "Excel Çalışma Sayfalarında Hücre Formülü Ayarlama"
type: docs
url: /tr/set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, Formül Ayarla, Çalışma Sayfası, Hücre, Bulut SDK, cURL"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki belirli bir hücreye formül nasıl ayarlanacağını öğrenin. cURL örneği, tüm parametre listesi, hata yönetimi ve SDK kod örnekleri içerir."
---

Bu REST API, bir Excel dosyasında **hücre formülünü** ayarlar.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

**İstek Parametreleri**

| Parametre Adı | Tür    | Konum  | Gerekli | Açıklama                                      |
|---------------|--------|--------|---------|-----------------------------------------------|
| name          | string | path   | Evet    | Excel belgesinin adı.                         |
| sheetName     | string | path   | Evet    | Çalışma sayfasının adı.                        |
| cellName      | string | path   | Evet    | Hedef hücrenin adresi (örneğin, **A1**).      |
| value         | string | query  | Hayır   | Hücreye atanacak değer.                       |
| type          | string | query  | Hayır   | Değerin veri türü (örneğin, **string**).      |
| formula       | string | query  | Hayır   | Hücreye uygulanacak formül (örneğin, **sum(A1,A2)**). |
| folder        | string | query  | Hayır   | Belgeyi içeren klasör.                         |
| storageName   | string | query  | Hayır   | Depolama hizmetinin adı.                      |

## **Yanıt**

CellResponse döndürür.

- **Yanıt Alanları Genel Bakış**

| Alan            | Tür     | Açıklama                                           |
| --------------- | ------- | --------------------------------------------------- |
| `Name`          | string  | Hücrenin adresi (örneğin, `F341`).                 |
| `Row`           | integer | Sıfır tabanlı satır indeksi.                       |
| `Column`        | integer | Sıfır tabanlı sütun indeksi.                       |
| `Value`         | string  | Hücrenin gösterilen değeri.                        |
| `Type`          | string  | Hücrenin veri türü (örneğin, `IsString`).         |
| `Formula`       | string  | Hücre bir formül içeriyorsa formül metni.         |
| `IsFormula`     | bool    | Hücrenin bir formül içerip içermediğini belirtir.  |
| `IsMerged`      | bool    | Hücrenin birleştirilmiş bir aralığın parçası olup olmadığını belirtir. |
| `IsArrayHeader` | bool    | Hücrenin bir dizi başlığı olup olmadığını belirtir. |
| `IsInArray`     | bool    | Hücrenin bir diziye ait olup olmadığını belirtir.  |
| `IsErrorValue`  | bool    | Hücrenin bir hata değeri içerip içermediğini belirtir. |
| `IsInTable`     | bool    | Hücrenin bir tablo içinde olup olmadığını belirtir. |
| `IsStyleSet`    | bool    | Hücreye bir stil uygulanıp uygulanmadığını belirtir. |
| `HtmlString`    | string  | Hücre değerinin HTML ile kodlanmış temsili.        |
| `Style.link`    | object  | Stil kaynağına yönelik hiperbağlantı.             |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                          |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.               |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.          |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.             |

## SDK'lar ile PostWorksheetCellSetValue API Nasıl Kullanılır

### PostWorksheetCellSetValue API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerini çağırmak için cURL komut satırı aracını kullanın.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yönetir; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web hizmetlerine nasıl istekte bulunulacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# örneği – hücre için formül ayarla
// <access-token>, <file-name> vb. değerleri kendi değerlerinizle değiştirin.
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java örneği – hücre için formül ayarla
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP örneği – hücre için formül ayarla
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby örneği – hücre için formül ayarla
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python örneği – hücre için formül ayarla
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js örneği – hücre için formül ayarla
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) örneği – hücre için formül ayarla
// Standart Java örneğine benzerdir; Android ile uyumlu SDK kullandığınızdan emin olun.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Swift örneği mevcut değil.** Swift SDK’sı şu anda geliştirme aşamasındadır.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl örneği – hücre için formül ayarla
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go örneği – hücre için formül ayarla
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}
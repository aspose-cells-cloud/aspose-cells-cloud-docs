---
title: "Çalışma Sayfasından Grafik Başlığını Alın"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Grafik Başlığı"
  - "Excel"
  - "REST API"
  - "Grafik Başlığını Al"
  - "cURL"
  - "SDK"
  - "Excel grafik otomasyonu"
  - "GRAFİK BAŞLIĞINI AL"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından bir grafik başlığını nasıl alacağınızı öğrenin. Uç nokta, parametreler, kimlik doğrulama, örnek cURL ve SDK kodunu içerir."
ArticleTitle: "Çalışma Sayfasından Grafik Başlığını Alın"
---

Bu REST API, bir Excel çalışma kitabının bir çalışma sayfasında depolanan bir grafik başlığını alır.

**Önkoşullar**: Bu uç noktayı çağırmak için `Cells.Read` kapsamdaki geçerli bir Aspose.Cells Cloud OAuth2/JWT erişim belirteciniz olmalıdır. Çalışma kitabının zaten belirtilen depolama konumuna yüklenmiş olması gerekir.

## GetWorksheetChartTitle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                                      |
| ------------- | ------ | ----- | --------------------------------------------- |
| name          | string | path  | Çalışma kitaplığı dosyasının adı.             |
| sheetName     | string | path  | Grafiği içeren çalışma sayfasının adı.        |
| chartIndex    | integer | path | Grafiğin sıfır tabanlı dizini.                |
| folder        | string | query | Çalışma kitabının depolandığı klasör yolu.    |
| storageName   | string | query | Depolama hizmetinin adı.                      |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "Sales Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Yanıt alanları**

| Alan                | Açıklama                                         |
| ------------------- | ------------------------------------------------ |
| `Title.Text`        | Grafik başlığı olarak görüntülenen gerçek metin. |
| `Title.Font.Name`   | Başlık için kullanılan yazı tipi ailesi (örn. _Arial_). |
| `Title.Font.Size`   | Nokta cinsinden yazı tipi boyutu.                |
| `Title.Font.IsBold` | Başlık metninin kalın olup olmadığını belirtir.   |

**Yanıt durum kodları**

| Kod | Açıklama |
|-----|----------|
| 200 OK | Grafik başlığı başarıyla alındı. |
| 401 Unauthorized | Kimlik doğrulama başarısız oldu veya belirteç eksik/geçersiz. |
| 404 Not Found | Belirtilen çalışma kitabısı, çalışma sayfası veya grafik mevcut değil. |
| 500 Internal Server Error | Beklenmeyen bir sunucu hatası oluştu. |

**Notlar**: Grafik dizini sıfır tabanlıdır; grafiğin mevcut olduğundan emin olun. Çalışma kitabısı yüklenmediyse, önce uygun API kullanılarak yüklenmelidir.

**Komut dosyasında başlığı nasıl çıkaracağınız (jq kullanarak)**

```bash
# Yanıt JSON'unun response.json içinde kaydedildiğini varsayalım
title=$(jq -r '.Title.Text' response.json)
echo "Grafik başlığı: $title"
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en hızlı şekilde artıracaktır. SDK, alt seviye detayları yönetir, böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# örneği, Aspose.Cells Cloud SDK kullanılarak
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java örneği, Aspose.Cells Cloud SDK kullanılarak
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP örneği, Aspose.Cells Cloud SDK kullanılarak
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby örneği, Aspose.Cells Cloud SDK kullanılarak
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python örneği, Aspose.Cells Cloud SDK kullanılarak
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js örneği, Aspose.Cells Cloud SDK kullanılarak
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt token>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) örneği, Aspose.Cells Cloud SDK kullanılarak
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift örneği, Aspose.Cells Cloud SDK kullanılarak
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Grafik başlığı: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl örneği, Aspose.Cells Cloud SDK kullanılarak
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt token>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

Gelişmiş senaryolar için (örneğin grafik başlığını güncelleme veya silme) ayrıca tekil SDK belgelerine de başvurabilirsiniz.

**Ayrıca bakın**: [Grafik Başlığını Güncelle](/charts/title/put/), [Grafik Başlığını Sil](/charts/title/delete/).
---
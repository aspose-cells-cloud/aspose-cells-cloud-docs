---
title: "Grafiğin İkinci Değer Ekseni Güncelleme"
ArticleTitle: "Grafiğin İkinci Değer Ekseni Güncelleme – Aspose.Cells Cloud REST API"
type: docs
url: /charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Grafik API, İkinci Değer Ekseni, Excel, REST, Bulut SDK"
description: "Aspose.Cells Cloud REST API kullanılarak bir Excel çalışma sayfasındaki grafiğin ikinci değer eksenini günceller. İstek örnekleri, yanıt kodları ve önkoşulları içerir."
---

Bu REST API, bir grafiğin ikinci değer eksenini günceller.

**Önkoşullar:**  
- Geçerli bir JWT erişim belirteci (bkz. [Kimlik Doğrulama Kılavuzu](https://docs.aspose.cloud/cells/authentication/)).  
- Hedef Excel dosyası Aspose Cloud depolama alanında saklanmalıdır (`folder` ve isteğe bağlı `storageName` sağlayın).  
- API sürümü v3.0 kullanılmaktadır; temel URL'nin `https://api.aspose.cloud/v3.0` olduğundan emin olun.

## PostChartSecondValueAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür     | Konum | Açıklama                                         |
| ------------- | ------- | ----- | ------------------------------------------------ |
| name          | string  | path  | Excel dosyasının adı.                            |
| sheetName     | string  | path  | Grafiği içeren çalışma sayfasının adı.           |
| chartIndex    | integer | path  | Değiştirilecek grafiğin sıfır tabanlı indeksi.   |
| axis          | object  | body  | İkinci değer ekseni için ayarlar.                |
| folder        | string  | query | Dosyanın bulunduğu depolama klasör yolu.         |
| storageName   | string  | query | Depolama hizmetinin adı.                         |

**Örnek istek gövdesi (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "İkincil Eksen"
  }
}
```

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis), herkese açık erişilebilir bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine istek nasıl yapılır gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.             |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                      |

**Ayrıca bakınız:**  
- [Grafiğin İkinci Değer Ekseni Alma](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [Grafiğin Değer Ekseni Güncelleme](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// İkinci değer eksenini güncellemek için C# örneği
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// İkinci değer eksenini güncellemek için Java örneği
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// İkinci değer eksenini güncellemek için PHP örneği
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
// İkinci değer eksenini güncellemek için Ruby örneği
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# İkinci değer eksenini güncellemek için Python örneği
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) örneği – yukarıdaki Java kod parçası ile aynıdır
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// İkinci değer eksenini güncellemek için Swift örneği
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# İkinci değer eksenini güncellemek için Perl örneği
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// İkinci değer eksenini güncellemek için Go örneği
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}
---
title: "Tüm Bağlantıları Al – Aspose.Cells Cloud REST API"
type: docs
url: /tr/hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, Tüm Bağlantıları Al, Excel API, REST API, Bulut SDK, cURL Örneği, Elektronik Tablo Bağlantıları"
description: "Aspose.Cells Cloud REST API (v3.0) kullanarak bir Excel dosyasındaki bir çalışma sayfasından tüm bağlantıları alın. HTTPS uç noktasını, gerekli parametreleri, cURL örneğini, yanıt şemasını ve SDK kod örneklerini içerir."
weight: 10
ArticleTitle: "Tüm Bağlantıları Al – Aspose.Cells Cloud REST API Dokümantasyonu"
---

Bu REST API, bir Excel defterindeki belirli bir çalışma sayfasından **tüm bağlantıları** getirir.

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerek duyar.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### İstek Parametreleri

| Parametre Adı | Tür    | Konum | Gerekli | Varsayılan | Açıklama                            |
| ------------- | ------ | ----- | ------- | --------- | ----------------------------------- |
| name          | string | path  | Evet    | –         | Excel belgesinin adı.               |
| sheetName     | string | path  | Evet    | –         | Çalışma sayfasının adı.             |
| folder        | string | query | Hayır   | –         | Belgenin bulunduğu klasör.          |
| storageName   | string | query | Hayır   | –         | Kullanılacak depolama hizmetinin adı. |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, API’yi cURL ile nasıl çağırayacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

JSON yanıtı, bir `Hyperlinks` nesnesi içerir.

- **Count** – çalışma sayfasındaki toplam bağlantı sayısı.
- **HyperlinkList** – her biri bir `link` nesnesi içeren bir dizi. `Href` özelliği bağlantı adresini saklar; `Rel`, `Title` ve `Type` ek meta verileri sağlar (basit bağlantılar için genellikle `null` olur).

### Hata Yanıtları

| HTTP Kodu | Neden                                              | Örnek Gövde                                                         |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Geçersiz İstek – eksik veya geçersiz parametreler. | `{ "Code":"400", "Message":"Geçersiz parametre değeri." }`          |
| **401**   | Yetkisiz – eksik veya geçersiz JWT belirteci.     | `{ "Code":"401", "Message":"Erişim belirteci eksik veya geçersiz." }` |
| **404**   | Bulunamadı – defter veya çalışma sayfası mevcut değil. | `{ "Code":"404", "Message":"Dosya bulunamadı." }`                  |
| **500**   | Sunucu İç Hatası – beklenmeyen sunucu arızası.     | `{ "Code":"500", "Message":"Beklenmeyen bir hata oluştu." }`        |

## Bulut SDK Ailesi

Bu işlevselliği entegre etmenin en hızlı yolu bir SDK kullanmaktır. SDK’lar düşük seviye detayları yöneterek iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}
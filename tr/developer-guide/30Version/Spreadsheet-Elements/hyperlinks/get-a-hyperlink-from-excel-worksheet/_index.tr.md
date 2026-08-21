---
title: "Çalışma Sayfası Bağlantısını Al"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, Çalışma Sayfası Bağlantısını Al, Excel bağlantı API'si, REST, JWT kimlik doğrulama, Excel çalışma sayfası, API uç noktası"
description: "Aspose.Cells Cloud API'sini (v3.0) kullanarak bir Excel çalışma sayfasından belirli bir bağlantıyı alın. Uç nokta, parametreler, cURL örneği, kimlik doğrulama ayrıntıları, hata işleme ve SDK kod parçacıklarını içerir."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Çalışma Sayfası Bağlantısını Al"
---

Bu REST API, **Aspose.Cells Bağlantı Al API'sini** kullanarak bir çalışma sayfasının **bağlantısını** getirir.

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerek duyar.  
Uç noktayı çağırmadan önce, istemci kimliğiniz ve gizli anahtarınızla bir JWT erişim belirteci edinin ve `Authorization: Bearer <jwt token>` başlığına ekleyin.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### İstek Parametreleri

| Parametre Adı    | Tür      | Konum  | Açıklama                                         |
| ---------------- | -------- | ------ | ------------------------------------------------ |
| name             | string   | path   | Excel dosyasının adı.                            |
| sheetName        | string   | path   | Bağlantının bulunduğu çalışma sayfasının adı.    |
| hyperlinkIndex   | integer  | path   | Alınacak bağlantının sıfır tabanlı indeksi.      |
| folder           | string   | query  | Belgenin depolandığı klasör.                     |
| storageName      | string   | query  | Depolama hizmetinin adı.                         |

### Hata Yanıtları

| HTTP Kodu | Neden                                                | Örnek Gövde                                                        |
| --------- | ---------------------------------------------------- | ----------------------------------------------------------------- |
| **400**   | Bad Request – eksik veya geçersiz parametreler.      | `{ "Code":"400", "Message":"Geçersiz parametre değeri." }`        |
| **401**   | Unauthorized – eksik veya geçersiz JWT belirteci.    | `{ "Code":"401", "Message":"Erişim belirteci eksik veya geçersiz." }` |
| **404**   | Not Found – çalışma kitapçası veya çalışma sayfası yok. | `{ "Code":"404", "Message":"Dosya bulunamadı." }`                |
| **500**   | Internal Server Error – beklenmeyen sunucu hatası.   | `{ "Code":"500", "Message":"Beklenmeyen bir hata oluştu." }`      |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Kiti

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkânı verir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)'na bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK'lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}
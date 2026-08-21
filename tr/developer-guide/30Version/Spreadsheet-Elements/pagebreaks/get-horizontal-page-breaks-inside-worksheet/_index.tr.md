---
title: "Yatay Sayfa Sonları Alın"
second_title: "Belge"
linktitle: "Yatay Sayfa Sonları Alın"
type: docs
url: /tr/page-breaks/get-horizontal-page-breaks/
aliases: [  /tr/get-horizontal-page-breaks-inside-worksheet/ ]
keywords: "yatay sayfa sonları, Aspose.Cells Cloud, REST API, Excel çalışma sayfası, SDK"
description: "Aspose.Cells Cloud API aracılığıyla bir Excel çalışma sayfasından yatay sayfa sonlarını alın. Endpoint, parametreler, cURL örneği, yanıt formatı ve C#, Java, Python ve diğerleri için SDK snippet'lerini içerir."
ArticleTitle: "Yatay Sayfa Sonları Alın - Aspose.Cells Cloud API Dökümantasyonu"
weight: 10
---

**Yatay sayfa sonu** – Belirtilen satırdan sonra yeni bir yazdırma sayfasının başlamasını zorlayan, satır tabanlı bir kesme noktasıdır. Bu REST API, bu yatay sayfa sonlarını getirir.

## Güvenlik ve Yetkilendirme

Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) ihtiyaç duyar.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### İstek Parametreleri

| Parametre Adı | Tür     | Konum  | Açıklama                                                         |
| ------------- | ------- | ------ | ---------------------------------------------------------------- |
| name          | string  | path   | Excel dosyasının adı.                                            |
| sheetName     | string  | path   | Çalışma sayfasının adı.                                          |
| folder        | string  | query  | Dosyanın bulunduğu depo içindeki klasör yolu. _(isteğe bağlı)_  |
| storageName   | string  | query  | Depo adı. _(isteğe bağlı)_                                       |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="GetHorizontalPageBreaks için OpenAPI spesifikasyonu">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## Hata Yönetimi

| HTTP Durumu | Açıklama                                                     | Örnek JSON                                             |
| ----------- | ------------------------------------------------------------ | ------------------------------------------------------ |
| 400         | Geçersiz istek – eksik veya geçersiz parametreler.          | `{ "Code": 400, "Message": "Invalid parameter." }`     |
| 401         | Yetkisiz erişim – JWT belirteci eksik veya geçersiz.        | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404         | Bulunamadı – belirtilen dosya veya çalışma sayfası yok.     | `{ "Code": 404, "Message": "Resource not found." }`    |
| 500         | Sunucu iç hatası – sunucuda beklenmeyen bir durum oluştu.   | `{ "Code": 500, "Message": "Server error." }`          |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)'na bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini farklı SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}
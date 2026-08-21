---
title: "Bağlantıları Temizle"
type: docs
url: /tr/hyperlinks/clear/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, bağlantıları temizle, bağlantıları sil, REST API, çalışma sayfası, SDK"
description: "Aspose.Cells Cloud REST API’si veya desteklenen SDK’lardan herhangi birini (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl vb.) kullanarak bir Excel çalışma sayfasından tüm bağlantıları nasıl kaldıracağınızı öğrenin."
weight: 40
ArticleTitle: "Bağlantıları Temizle – Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, bir Excel çalışma sayfasındaki **tüm bağlantıları** siler.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### İstek Parametreleri

| Parametre Adı | Tür     | Konum  | Açıklama                              |
| ------------- | ------- | ------ | ------------------------------------- |
| name          | string  | path   | Excel dosyasının adı.                 |
| sheetName     | string  | path   | Çalışma sayfasının adı.               |
| folder        | string  | query  | Belgeyi içeren klasör.                |
| storageName   | string  | query  | Depolama hizmetinin adı.              |

### Hata Yanıtları

| HTTP Kodu | Neden                                              | Örnek Gövde                                                         |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Geçersiz İstek – eksik veya geçersiz parametreler. | `{ "Code":"400", "Message":"Geçersiz parametre değeri." }`          |
| **401**   | Yetkisiz – eksik veya geçersiz JWT belirteci.     | `{ "Code":"401", "Message":"Erişim belirteci eksik veya geçersiz." }` |
| **404**   | Bulunamadı – çalışma kitabı veya çalışma sayfası yok. | `{ "Code":"404", "Message":"Dosya bulunamadı." }`                  |
| **500**   | Sunucu İç Hatası – beklenmeyen sunucu hatası.      | `{ "Code":"500", "Message":"Beklenmeyen bir hata oluştu." }`        |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks), bir web tarayıcısından doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık bir programlama arayüzü tanımlar.

**cURL** komut satırı aracını Aspose.Cells web hizmetlerini çağırmak için kullanabilirsiniz. Aşağıdaki örnek, bir çalışma sayfasından tüm bağlantıları silmeyi göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
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

## Bulut SDK Ailesi
Bir SDK kullanmak, düşük seviye ayrıntıları sizin için yöneterek geliştirme sürecini hızlandırır. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’larla çalışma sayfası bağlantılarını nasıl sileceğinizi göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}
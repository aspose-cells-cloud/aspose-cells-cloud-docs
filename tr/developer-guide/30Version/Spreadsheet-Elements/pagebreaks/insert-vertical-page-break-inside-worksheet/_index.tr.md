---
title: "Dikey Sayfa Sonrası Ekle"
second_title: "Belge"
linktype: "Dikey Sayfa Sonrası Ekle"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, dikey sayfa sonrası, REST API, Excel, SDK, cURL"
description: "Aspose.Cells Cloud REST API (v3.0) kullanarak bir Excel çalışma sayfasına dikey sayfa sonrası nasıl ekleneceğini öğrenin. İstek söz dizimi, cURL örneği, SDK örnekleri, kimlik doğrulama kılavuzu ve hata işleme ayrıntılarını içerir."
weight: 40
ArticleTitle: "Dikey Sayfa Sonrası Ekle – Aspose.Cells Cloud API"
---

Bu REST API, bir çalışma sayfasına dikey sayfa sonrası ekler.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerek duyar.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### İstek Parametreleri

| Parametre Adı | Tür      | Konum  | Açıklama                                                                 |
| ------------- | -------- | ------ | ------------------------------------------------------------------------ |
| name          | string   | path   | Excel çalışma kitabının adı.                                             |
| sheetName     | string   | path   | Sayfa sonrasının ekleneceği çalışma sayfasının adı.                      |
| cellname      | string   | query  | Sayfa sonrası konumunu belirleyen hücre başvurusu (örn. **A1**).         |
| column        | integer  | query  | Sayfa sonrasının başladığı sütunun sıfır tabanlı indeksi.               |
| row           | integer  | query  | Sayfa sonrasının başladığı satırın sıfır tabanlı indeksi.               |
| startRow      | integer  | query  | Sayfa sonrası aralığının ilk satırı.                                     |
| endRow        | integer  | query  | Sayfa sonrası aralığının son satırı.                                     |
| folder        | string   | query  | Çalışma kitabının bulunduğu depolama alanındaki klasör yolu.             |
| storageName   | string   | query  | Depolama hizmetinin adı.                                                |

**Gerekli parametreler** – `cellname` **veya** `column` parametrelerinden biri sağlanmalıdır. `column` kullanıldığında, bir aralık tanımlamak için `row`, `startRow` ve `endRow` parametrelerini de sağlayabilirsiniz. Diğer tüm alanlar isteğe bağlıdır.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### cURL Örneği

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Yanıt

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                    |
|-----|-----------------------------|-------------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.                          |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.                       |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                                  |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en hızlı şekilde artıracak en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yönetir ve size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
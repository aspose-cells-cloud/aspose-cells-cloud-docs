---
title: "Excel Çalışma Sayfası İçin Sayfa Sayısını Alın"
second_title: "Belge"
linktitle: "SayfaSayısı"
type: docs
url: /tr/worksheets/page-count/
keywords: "Aspose.Cells, Excel API, çalışma sayfası sayfa sayısı, REST, bulut SDK'sı, Excel sayfalama"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasındaki yazdırılabilir sayfa sayısını alın. HTTPS istek formatını, kimlik doğrulama adımlarını, örnek cURL isteğini, tam JSON yanıtını, durum kodlarını ve SDK kod örneklerini içerir."
weight: 10
ArticleTitle: "Excel Çalışma Sayfası İçin Sayfa Sayısını Alın – Aspose.Cells Cloud API"
---

Bu REST API, bir çalışma sayfası için **sayfa sayısını** döndürür.

**Kimlik Doğrulama:** Tüm Aspose.Cells Cloud uç noktaları, OAuth2 akışı aracılığıyla elde edilen Bearer belirteci gerektirir. Belirteci aşağıda gösterilen cURL örneğinde olduğu gibi `Authorization` başlığında dahil edin.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### İstek Parametreleri

| Parametre   | Tür    | Konum  | Açıklama                              |
| ----------- | ------ | ------ | ------------------------------------- |
| name        | string | path   | Belge adı.                            |
| sheetName   | string | path   | Çalışma sayfası adı.                  |
| folder      | string | query  | Belgeyi içeren klasör.                |
| storageName | string | query  | Depo adı.                             |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca ulaşmak için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Yanıt Detayları

| HTTP Durumu | Anlamı                                                  |
| ----------- | ------------------------------------------------------- |
| **200**     | Başarılı – yukarıda gösterilen JSON yükünü döndürür.    |
| **401**     | Yetkisiz – eksik veya geçersiz belirteç.               |
| **404**     | Bulunamadı – dosya veya çalışma sayfası mevcut değil.   |
| **500**     | Sunucu iç hatası – beklenmeyen sunucu durumu.          |

### Versiyon Geçmişi

_API versiyonu **v3.0** (yayınlandı 2025). Daha yeni bir sürüm kullanıyorsanız, güncellenmiş uç nokta belgelerine bakın._

## Bulut SDK Kütüphanesi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Notlar

- Sayfa sayısı, sayfa kırılımlarını, kenar boşluklarını ve ölçeklemeyi dikkate alarak yazdırılabilir düzeni yansıtır. Gizli satır veya sütunlar sonucu etkileyebilir.
- İsteği yapmadan önce hedef çalışma sayfasının mevcut olduğundan ve dosyanın belirtilen `folder` ve `storageName` konumunda depolandığından emin olun.
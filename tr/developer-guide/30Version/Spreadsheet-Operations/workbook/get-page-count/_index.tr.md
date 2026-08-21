---
title: "Bir Excel Dosyasından Sayfa Sayısını Alma"
second_title: "Belge"
linktitle: "Sayfalar"
type: docs
url: /get-page-count-from-an-excel-file/
aliases: [/workbook/page-count/, /workbook/get/page-count/]
keywords: "Aspose.Cells, Bulut API’si, Excel sayfa sayısı, defter sayfalandırma"
description: "Aspose.Cells Cloud REST API’si (v3.0) aracılığıyla bir Excel defterindeki yazdırılabilir toplam sayfa sayısını alın. İstek formatını, gerekli parametreleri, cURL örneğini, yanıt şemasını, hata yönetimi ve birden fazla dil için SDK snippet’lerini içerir."
weight: 10
version: "v3.0"
ArticleTitle: "Aspose.Cells Cloud API’yi Kullanarak Bir Excel Dosyasından Sayfa Sayısını Alma"
---

Bu REST API, bir defter için **sayfa sayısını** döndürür.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### İstek parametreleri

| Parametre Adı | Tür   | Konum | Gerekli | Açıklama                               |
| ------------- | ----- | ----- | ------- | -------------------------------------- |
| name          | string | path  | Evet    | Excel belgesinin adı.                  |
| folder        | string | query | Hayır   | Belgeyi içeren klasör.                 |
| storageName   | string | query | Hayır   | Kullanılacak depo adı.                |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells REST API’ye kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile endpoint’e nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/YourFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*`YourFile.xlsx` ifadesini, sorgulamak istediğiniz defterin gerçek dosya adıyla değiştirin.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### Yanıt Şeması

| HTTP Durum Kodu | Veri Türü | Açıklama                                                       |
| --------------- | --------- | -------------------------------------------------------------- |
| 200             | integer   | Defterdeki toplam yazdırılabilir sayfa sayısı (örneğin, `13`). |
| 4xx‑5xx         | JSON      | Hata nesnesi (bkz. _Hata Yönetimi_ bölümü).                    |

## Bulut SDK’sı Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları kendisi yönetir ve sizin projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposunu](https://github.com/aspose-cells-cloud) ziyaret edin.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerine çeşitli SDK’lar kullanılarak nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Hata Yönetimi

| HTTP Durum Kodu | Açıklama                                       | Örnek JSON Gövdesi                                                                           |
| --------------- | --------------------------------------------- | ------------------------------------------------------------------------------------------- |
| 401             | Geçersiz veya eksik JWT belirteci.            | `{ "Code": "InvalidAuthenticationToken", "Message": "Erişim belirteci eksik veya geçersiz." }` |
| 404             | Belirtilen defter bulunamadı.                 | `{ "Code": "FileNotFound", "Message": "İstenen dosya mevcut değil." }`                      |
| 400             | Hatalı istek – gerekli parametre eksik.       | `{ "Code": "BadRequest", "Message": "'name' gerekli parametresi eksik." }`                  |
| 500             | İç sunucu hatası.                              | `{ "Code": "InternalError", "Message": "Beklenmeyen bir hata oluştu." }`                   |
---
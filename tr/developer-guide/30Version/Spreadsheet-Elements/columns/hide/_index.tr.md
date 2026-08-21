---
title: "Excel çalışma sayfasında sütunları gizle"
second_title: "Belge"
linktitle: "Gizle"
type: docs
url: /columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, sütun gizleme API'si, Excel sütun gizleme, REST API ile sütun gizleme, Aspose.Cells SDK, hesap tablosu otomasyonu"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasında bir veya daha fazla sütunu nasıl gizleyeceğinizi öğrenin. Endpoint, parametreler, cURL örneği, SDK kod örnekleri ve hata işleme içerir."
weight: 40
---

Bu REST API, bir çalışma sayfasında sütunları gizler.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### İstek parametreleri

| Parametre Adı | Tür      | Konum  | Açıklama                                                                 |
| ------------- | -------- | ------ | ------------------------------------------------------------------------ |
| name          | string   | path   | Çalışma kitabının dosya adı.                                             |
| sheetName     | string   | path   | Sütunların gizleneceği çalışma sayfasının adı.                          |
| startColumn   | integer  | query  | Gizlenecek ilk sütunun sıfır tabanlı indeksi.                           |
| totalColumns  | integer  | query  | **startColumn**'dan başlayarak ardışık olarak gizlenecek sütun sayısı.  |
| folder        | string   | query  | Çalışma kitabını içeren klasörün yolu.                                  |
| storageName   | string   | query  | Dosyanın bulunduğu depolama hizmetinin adı.                            |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerini kolayca çağırmak için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile bir sütunu nasıl gizleyeceğinizi göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Mümkün olan yanıt kodları**

| HTTP Kodu | Anlamı                                    | Örnek JSON (hata)                                     |
| --------- | ----------------------------------------- | ----------------------------------------------------- |
| 200       | Başarılı                                   | `{ "Code": 200, "Status": "OK" }`                     |
| 400       | Geçersiz istek (örneğin, geçersiz parametreler) | `{ "Code": 400, "Message": "Geçersiz sütun aralığı." }` |
| 401       | Yetkisiz erişim (eksik/geçersiz belirteç)  | `{ "Code": 401, "Message": "Geçersiz erişim belirteci." }` |
| 404       | Bulunamadı (çalışma kitabı veya çalışma sayfası) | `{ "Code": 404, "Message": "Dosya bulunamadı." }`       |
| 500       | İç sunucu hatası                           | `{ "Code": 500, "Message": "Beklenmeyen hata." }`     |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Kiti

SDK kullanmak, geliştirmenin en hızlı yoludur. Bir SDK, düşük seviye ayrıntıları soyutlar ve iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
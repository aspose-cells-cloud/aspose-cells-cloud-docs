---
title: "Hücre Alanını Sil – Aspose.Cells Cloud API Dokümantasyonu"
type: docs
url: /tr/conditional-formattings/delete-cell-area/
aliases: [  /tr/remove-cell-area-from-conditional-formatting/ ]
keywords: "Aspose.Cells Cloud, Hücre Alanını Sil, Koşullu Biçimlendirme API'si, Excel REST API"
description: "Aspose.Cells Cloud REST API'sini kullanarak bir Excel çalışma sayfasındaki koşullu biçimlendirmeden belirli bir hücre alanını silin. ASP.NET, Java ve Python örneklerini içerir."
ArticleTitle: "Hücre Alanını Sil – Aspose.Cells Cloud API Dokümantasyonu"
weight: 70
---

Bu REST API, bir koşullu biçimlendirme kuralından bir hücre alanını kaldırır.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### İstek Parametreleri

| Parametre Adı   | Tür      | Konum  | Açıklama                                                                |
|-----------------|----------|--------|-------------------------------------------------------------------------|
| `name`          | string   | path   | Excel dosyasının adı.                                                    |
| `sheetName`     | string   | path   | Koşullu biçimlendirme içeren çalışma sayfasının adı.                      |
| `startRow`      | integer  | query  | Kaldırılacak alanın ilk satırının sıfır tabanlı indeksi.                 |
| `startColumn`   | integer  | query  | Kaldırılacak alanın ilk sütununun sıfır tabanlı indeksi.                 |
| `totalRows`     | integer  | query  | Kaldırılacak alandaki satır sayısı.                                      |
| `totalColumns`  | integer  | query  | Kaldırılacak alandaki sütun sayısı.                                      |
| `folder`        | string   | query  | Dosyanın bulunduğu bulut depolama klasörü (isteğe bağlı).                |
| `storageName`   | string   | query  | Depolama hizmetinin adı (isteğe bağlı).                                  |

### Hata Yanıtları

| HTTP Durum Kodu | Kod          | Açıklama                                                    | Örnek JSON                                                       |
|-----------------|--------------|-------------------------------------------------------------|------------------------------------------------------------------|
| 400             | `BadRequest` | Eksik veya geçersiz parametreler.                           | `{ "Code": "400", "Message": "Geçersiz istek parametreleri." }` |
| 401             | `Unauthorized` | Eksik veya geçersiz JWT belirteci.                         | `{ "Code": "401", "Message": "Kimlik doğrulama başarısız." }`     |
| 404             | `NotFound`   | Dosya, çalışma sayfası veya koşullu biçimlendirme bulunamadı. | `{ "Code": "404", "Message": "Kaynak bulunamadı." }`             |
| 500             | `InternalError` | Beklenmeyen sunucu hatası.                                 | `{ "Code": "500", "Message": "İç sunucu hatası." }`               |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells Cloud hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, **Hücre Alanını Sil** uç noktasını cURL ile nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Seti Ailesi

Gelişmeyi hızlamanın en iyi yolu bir SDK kullanmaktır. Bir SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}
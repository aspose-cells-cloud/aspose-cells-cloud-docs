---
title: "Koşullu Biçimlendirmeyi Temizle"
type: docs
url: /conditional-formattings/clear/
aliases: [/clear-all-condition-formattings/]
keywords: "Aspose.Cells Cloud, REST API, koşullu biçimlendirmeyi temizle, Excel, çalışma sayfaları, JWT, v3.2"
description: "Aspose.Cells Cloud API’si (v3.2) ile bir çalışma sayfasından tüm koşullu biçimlendirme kurallarını silin. İstek sözdizimi, gerekli parametreler, kimlik doğrulama adımları ve birden fazla SDK'da örnek kodu öğrenin."
weight: 80
---

Bu REST API, bir çalışma sayfasından tüm koşullu biçimlendirme kurallarını temizler.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### İstek Parametreleri

| Parametre Adı   | Tür     | Konum  | Açıklama                                                               |
| ---------------- | ------- | ------ | ---------------------------------------------------------------------- |
| **name**         | string  | path   | Çalışma kitabının dosya adı (örneğin, `Book1.xlsx`).                  |
| **sheetName**    | string  | path   | Koşullu biçimlendirmenin kaldırılacağı çalışma sayfasının adı.         |
| **folder**       | string  | query  | _(İsteğe bağlı)_ Çalışma kitabının bulunduğu depolamadaki klasör yolu. |
| **storageName**  | string  | query  | _(İsteğe bağlı)_ Depolama hizmetinin adı.                             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings), herkese açık bir programlama arayüzü tanımlar ve **OpenAPI Specification**, REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapılır gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
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

### Hata Yanıtları

| HTTP Kodu | Neden                                              | Örnek Gövde                                                        |
| --------- | -------------------------------------------------- | ----------------------------------------------------------------- |
| **400**   | İstek Hatası – eksik veya geçersiz parametreler.  | `{ "Code":"400", "Message":"Geçersiz parametre değeri." }`       |
| **401**   | Yetkisiz – eksik veya geçersiz JWT jetonu.        | `{ "Code":"401", "Message":"Erişim jetonu eksik veya geçersiz." }` |
| **404**   | Bulunamadı – çalışma kitabı veya çalışma sayfası yok. | `{ "Code":"404", "Message":"Dosya bulunamadı." }`                |
| **500**   | Sunucu İç Hatası – beklenmeyen sunucu hatası.     | `{ "Code":"500", "Message":"Beklenmeyen bir hata oluştu." }`     |

## SDK Örnekleri

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}
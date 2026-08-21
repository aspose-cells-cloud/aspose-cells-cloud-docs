---
title: "Koşullu Biçimlendirme Kurallarını Al"
type: docs
url: /conditional-formattings/get-all/
aliases: [/get-conditional-formattings-of-worksheet/]
keywords: "Aspose.Cells Cloud, REST API, Excel, Koşullu Biçimlendirme, Çalışma Sayfası, Koşullu Biçimlendirme API'si"
description: "Aspose.Cells Cloud REST API kullanarak bir çalışma sayfasına uygulanan tüm koşullu biçimlendirme kurallarını alın. İstek sözdizimi, kimlik doğrulama adımları, parametreler, özet yanıt örnekleri ve hata yönetimi içerir."
weight: 20
---

Bu REST API, bir çalışma sayfasına uygulanan koşullu biçimlendirme kurallarını alır.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### İstek Parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                                    |
| ------------- | ------ | ----- | ------------------------------------------- |
| name          | string | path  | Excel dosyasının adı.                       |
| sheetName     | string | path  | Çalışma sayfasının adı.                     |
| folder        | string | query | Dosyanın saklandığı klasör yolu.            |
| storageName   | string | query | Depolama hizmetinin adı (isteğe bağlı).     |

### Hata Yanıtları

| HTTP Kodu | Neden                                                | Örnek Gövde                                                        |
| --------- | ---------------------------------------------------- | ----------------------------------------------------------------- |
| **400**   | Geçersiz İstek – eksik veya geçersiz parametreler.  | `{ "Code":"400", "Message":"Invalid parameter value." }`         |
| **401**   | Yetkisiz – eksik veya geçersiz JWT belirteci.       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Bulunamadı – çalışma kitapçası veya çalışma sayfası yok. | `{ "Code":"404", "Message":"File not found." }`                 |
| **500**   | İç Sunucu Hatası – beklenmeyen sunucu hatası.        | `{ "Code":"500", "Message":"An unexpected error occurred." }`    |

<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye istek yapmayı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_Yukarıdaki örnek, yükü özet tutmak amacıyla yalnızca en alakalı alanları göstermektedir._

**Yanıt Parametreleri**

| Parametre                        | Tür     | Açıklama                                           |
|----------------------------------|---------|----------------------------------------------------|
| Status                           | string  | İsteğin sonuç durumu (örn., **OK**).               |
| ConditionalFormattings           | object  | Koşullu biçimlendirme verilerinin kapsayıcısı.     |
| ConditionalFormattings.Count     | integer | Döndürülen koşullu biçimlendirme kuralı sayısı.    |
| ConditionalFormattings.ConditionalFormattingList | array | Koşullu biçimlendirme nesnelerinin listesi.        |
| ConditionalFormattingList[].sqref | string  | Biçimlendirmenin uygulandığı hücre aralığı (örn., **A1:B10**). |
| ConditionalFormattingList[].FormatConditions | array | Aralığa ait format koşulu nesneleri koleksiyonu.  |
| FormatConditions[].Priority      | integer | Koşulun değerlendirilme önceliği.                  |
| FormatConditions[].Type          | string  | Koşul türü (örn., **CellValue**).                 |
| FormatConditions[].Operator      | string  | Koşulda kullanılan operatör (örn., **GreaterThan**). |
| FormatConditions[].Formula1      | string  | Koşul için ilk formül veya değer.                  |
| FormatConditions[].Style         | object  | Koşul sağlandığında uygulanacak stil.              |
| Style.Font.Color                 | object  | Yazı tipi için RGBA renk tanımlaması.              |
| Style.Font.IsBold                | boolean | Yazı tipinin kalın olup olmadığını gösterir.       |

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.              |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor.           |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası.                      |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en çok artıracak en iyi yoldur. Bir SDK, düşük seviye detayları yönetir; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerinin çeşitli SDK'larla nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}
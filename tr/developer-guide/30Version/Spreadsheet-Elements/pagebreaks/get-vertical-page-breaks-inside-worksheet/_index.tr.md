---
title: "Dikey Sayfa Sonu Ayırıcıları Al"
second_title: "Belge"
linktitle: "Dikey Sayfa Sonu Ayırıcıları Al"
type: docs
url: /page-breaks/get-vertical-page-breaks/
aliases: [/get-vertical-page-breaks-inside-worksheet/]
keywords: "Aspose.Cells, dikey sayfa sonu ayırıcıları, Excel API, bulut hesap tablosu, REST API"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasından dikey sayfa sonu ayırıcılarını alın. HTTPS uç noktasını, gerekli parametreleri, cURL örneğini, yanıt ayrıntılarını, hata işleme ve SDK örneklerini içerir."
weight: 20
---

Bu REST API, bir çalışma sayfasından **dikey** sayfa sonu ayırıcılarını alır.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### İstek Parametreleri

| Parametre Adı | Tür   | Konum | Açıklama                                                   | Gerekli |
| -------------- | ------ | -------- | ---------------------------------------------------- | -------- |
| `name`         | string | path     | Excel dosyasının adı.                          | Evet      |
| `sheetName`    | string | path     | Ayırıcıların okunacağı çalışma sayfasının adı. | Evet      |
| `folder`       | string | query    | Dosyayı içeren depodaki klasör.        | Hayır       |
| `storageName`  | string | query    | Kullanılacak Aspose Cloud depo adı.         | Hayır       |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks), herkese açık bir erişilebilir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için **cURL** kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
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

### Yanıt Ayrıntıları

| Alan                    | Tür   | Açıklama                                                                         |
| ----------------------- | ------ | ----------------------------------------------------------------------------------- |
| `VerticalPageBreakList` | array  | Dikey sayfa sonu nesnelerinden oluşan bir koleksiyon.                                        |
| `Column`                | int    | Ayırıcının oluştuğu sütun indeksi (sıfır tabanlı).                               |
| `StartRow`              | int    | Ayırıcı aralığının ilk satırı (sıfır tabanlı).                                      |
| `EndRow`                | int    | Ayırıcı aralığının son satırı (sıfır tabanlı, genellikle son satır için `1048575`). |
| `link.Href`             | string | Kaynağın kendine referans veren URL'si (HTTPS).                                      |
| `Code`                  | int    | Servis tarafından döndürülen HTTP durum kodu.                                           |
| `Status`                | string | HTTP durumunun metinsel açıklaması.                                             |

### Hata İşleme

| HTTP Kodu | Anlamı               | Tipik Neden                               |
| --------- | --------------------- | ------------------------------------------- |
| 401       | Yetkisiz erişim          | Eksik veya geçersiz JWT belirteci.               |
| 404       | Bulunamadı             | Belirtilen dosya veya çalışma sayfası mevcut değil. |
| 400       | Geçersiz İstek           | Geçersiz veya bozuk sorgu parametreleri.      |
| 500       | Sunucu İç Hatası | Beklenmeyen sunucu tarafı durumu.           |

Ek ayrıntılar için JSON yanıtındaki `Code` ve `Status` alanlarını kontrol edin.

## Bulut SDK的家庭i

Aspose.Cells Cloud ile geliştirmek için SDK kullanmak en hızlı yoldur. Bir SDK, düşük seviye detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose.Cells web servislerine nasıl istek atılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}
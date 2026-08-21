---
title: "Aspose.Cells Cloud API – Çalışma Sayfasından Resim Alma"
second_title: "Belge"
linktitle: "Al"
type: docs
url: /pictures/get/
aliases: [/convert-picture-to-image/]
keywords: "Aspose.Cells, Resim Al, API, Excel, Bulut, REST"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından belirli bir resmi alın. Uç nokta, parametreler, kimlik doğrulama adımları, yanıt kodları ve kod örneklerini içerir."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Çalışma Sayfasından Resim Alma"
---

Bu REST API, bir Excel çalışma sayfasından sıfır tabanlı indeksine göre bir resmi alır.

## REST API

Bu uç noktayı çağırmak için **Authorization** başlığına geçerli bir JWT erişim belirteci eklemeniz gerekir. Belirteçler, Aspose.Cells Cloud kimlik doğrulama akışı aracılığıyla elde edilir ve dosya erişimi için uygun kapsamlara sahip olmak gerekir. Belirteç alma hakkında ayrıntılı bilgi için genel **Kimlik Doğrulama** kılavuzuna bakın.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### İstek Parametreleri

| Parametre Adı | Tür      | Konum | Açıklama                                                                                                             |
| ------------- | -------- | ----- | -------------------------------------------------------------------------------------------------------------------- |
| name          | string   | path  | Excel belgesinin adı.                                                                                                |
| sheetName     | string   | path  | Çalışma sayfasının adı.                                                                                              |
| pictureIndex  | integer  | path  | Resmin sıfır tabanlı indeksi.                                                                                        |
| format        | string   | query | İstenen dışa aktarma formatı (örneğin, png, jpg, bmp, gif, tiff). Belirtilmezse, resim orijinal formatında döndürülür. |
| folder        | string   | query | Belgeyi içeren klasör.                                                                                               |
| storageName   | string   | query | Depolama konumunun adı.                                                                                              |

### Hata Yanıtları

| HTTP Kodu | Açıklama                                                                      |
| --------- | ----------------------------------------------------------------------------- |
| 401       | Yetkisiz – eksik veya geçersiz belirteç.                                      |
| 404       | Bulunamadı – belirtilen dosya, çalışma sayfası veya sayfa sonu indeksi mevcut değil. |
| 400       | Geçersiz İstek – hatalı istek sözdizimi veya geçersiz parametreler.           |
| 500       | İç Sunucu Hatası – beklenmeyen bir koşulla karşılaşıldı.                       |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sinin nasıl çağrılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# Yanıt gövdesinde döndürülen ikili resim verisi (PNG).
# Örnek: base64 ile kodlanmış alıntı
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Kiti

SDK kullanmak, geliştirmenin en hızlı yoludur. Bir SDK, düşük seviye ayrıntıları işler ve projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
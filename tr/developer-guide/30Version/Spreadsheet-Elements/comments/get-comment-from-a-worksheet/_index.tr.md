---
title: "Çalışma Sayfası Yorumunu Al – Aspose.Cells Cloud API Dokümantasyonu"
type: docs
url: /tr/comments/get/
aliases: [  /tr/get-comment-from-a-worksheet/ ]
keywords: "Aspose.Cells, çalışma sayfası yorumu, API, GET, Excel"
description: "Aspose.Cells Cloud API’si (v3.0) kullanarak bir hücre adına göre çalışma sayfası yorumunu nasıl alacağınızı öğrenin. İstek URL’si, parametreler, cURL örneği, yanıt detayları ve SDK kod parçacıklarını içerir."
weight: 10
ArticleTitle: "Çalışma Sayfası Yorumunu Al – Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, **Aspose.Cells Cloud** kullanarak bir hücre adına göre çalışma sayfası yorumunu getirir.

**Önkoşullar:** Bu işlemi çağırmak için `Authorization` başlığına geçerli bir JWT erişim belirteci (`Bearer <jwt token>`) dahil etmelisiniz. Belirteçler, [Kimlik Doğrulama kılavuzunda](/cells/authentication/) açıklanan Aspose.Cells Cloud kimlik doğrulama akışıyla elde edilebilir.

## GetWorksheetComment API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür    | Konum (URL Yolu / Sorgu Dizesi) | Açıklama                                                           |
| ------------- | ------ | -------------------------------- | ------------------------------------------------------------------ |
| name          | string | URL Yolu                         | Excel dosyasının adı.                                              |
| sheetName     | string | URL Yolu                         | Yorumun bulunduğu çalışma sayfasının adı.                          |
| cellName      | string | URL Yolu                         | Yorumu alınacak hücrenin adresi (örn. **A1**).                    |
| folder        | string | Sorgu Dizesi                     | Belgenin depolandığı klasör yolu.                                  |
| storageName   | string | Sorgu Dizesi                     | Depolama hizmetinin adı.                                           |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">OpenAPI Specification</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye bir istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Yanıt:** API, aşağıdaki alanları içeren bir `Comment` nesnesi barındıran bir JSON nesnesi döndürür:

| Alan                       | Tür     | Açıklama                                              |
| -------------------------- | ------- | ----------------------------------------------------- |
| `CellName`                 | string  | Hücrenin adresi (örn. **A1**).                        |
| `Author`                   | string  | Yorumun yazarının adı.                                |
| `HtmlNote`                 | string  | Yorum içeriği HTML formatında (varsa).               |
| `Note`                     | string  | Yorumun düz metin versiyonu.                          |
| `AutoSize`                 | boolean | Yorum kutusunun otomatik boyutlandırma yapılandırılıp yapılmadığını gösterir. |
| `IsVisible`                | boolean | Yorumun görünürlüğünü belirler.                       |
| `Width`                    | integer | Yorum kutusunun genişliği (karakter cinsinden).       |
| `Height`                   | integer | Yorum kutusunun yüksekliği (karakter cinsinden).      |
| `TextHorizontalAlignment` | string  | Metnin yatay hizalaması (örn. **Bottom**).            |
| `TextOrientationType`      | string  | Metnin yönü (örn. **TopToBottom**).                   |
| `TextVerticalAlignment`    | string  | Metnin dikey hizalaması (örn. **Bottom**).            |

## Yaygın Hatalar

- **401 Yetkisiz** – JWT belirtecinin geçerli olduğunu, süresinin dolmadığını ve `Authorization` başlığında doğru yerleştirildiğini doğrulayın.
- **404 Bulunamadı** – Dosya adı, çalışma sayfası adı ve hücre adresinin doğru olduğundan ve dosyanın belirtilen klasör/depolamada mevcut olduğundan emin olun.
- **500 İç Sunucu Hatası** – İstek yükünde bozuk veri olup olmadığını kontrol edin ve hizmetin çalışır durumda olduğundan emin olun.

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.               |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırlamasını aşıyor.       |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası.                       |

## Bulut SDK Grubu

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yönetir ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine istek nasıl yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}
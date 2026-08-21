---
title: "Excel çalışma sayfasındaki tüm resimleri alın"
second_title: "Belge"
linktitle: "Tümünü al"
type: docs
url: /tr/pictures/get-all/
aliases: [  /tr/get-picture-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel çalışma sayfası, resim API'si, tüm resimleri al, REST API, SDK"
description: "Aspose.Cells Cloud REST API aracılığıyla bir Excel çalışma sayfasından tüm resim nesnelerini alın."
ArticleTitle: "Excel çalışma sayfasındaki tüm resimleri alın - Aspose.Cells Cloud API"
weight: 10
---

Bu REST API, bir Excel çalışma sayfasından tüm resim bilgilerini alır.

**Önkoşullar**  
Bu uç noktayı çağırmadan önce şunlardan emin olun:

- Geçerli bir Aspose Cloud JWT erişim belirteci.  
- Hedef Excel dosyasının seçilen depoya yüklenmiş olması.  
- Doğru depo adı (özel bir depo kullanıyorsanız).  
- Resimleri içeren çalışma sayfası adı.

## GetWorksheetPictures API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**Not:** API’yi çağırırken HTTPS (TLS 1.2 veya üzeri) kullanın ve `Authorization` başlığına geçerli bir JWT belirteci ekleyin.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür     | Konum | Açıklama                                            |
| ------------- | ------- | ----- | --------------------------------------------------- |
| name          | string  | path  | Excel dosyasının adı.                               |
| sheetName     | string  | path  | Resimleri içeren çalışma sayfasının adı.            |
| folder        | string  | query | Dosyanın bulunduğu klasör yolu.                     |
| storageName   | string  | query | Depolama hizmetinin adı.                            |

### Hata Yanıtları

| HTTP Kodu | Açıklama                                                                   |
| --------- | -------------------------------------------------------------------------- |
| 401       | Yetkisiz – eksik veya geçersiz belirteç.                                   |
| 404       | Bulunamadı – belirtilen dosya, çalışma sayfası veya sayfa kırma dizini yok. |
| 400       | Hatalı İstek – hatalı istek sözdizimi veya geçersiz parametreler.         |
| 500       | Sunucu İç Hatası – beklenmeyen bir durumla karşılaşıldı.                   |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
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

**Başarılı Yanıt** – Başarılı bir çağrı, HTTP 200 ile birlikte `Pictures` nesnesini içeren bir JSON yükü döndürür; bu nesne her bir resmin kaynak bağlantısını listeler.

## Bulut SDK Geliştirme Seti Ailesi

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yöneterek proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine çeşitli SDK’lar aracılığıyla nasıl istek yapıldığını göstermektedir:

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

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

SDK’ları, ilgili paket yöneticilerinden doğrudan indirebilirsiniz (örneğin, .NET için NuGet, Java için Maven Central, PHP için Composer, Node.js için npm, Python için PyPI, Perl için CPAN ve Go için Go modülleri).  

*Ayrıca bakın:* Bir resim ekleme, Bir resim silme, Resim özellikleri güncelleme.
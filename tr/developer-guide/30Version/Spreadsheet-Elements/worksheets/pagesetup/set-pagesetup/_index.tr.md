---
title: "Bir çalışma sayfası için sayfa ayarını ayarla"
second_title: "Belge"
linktitle: "Sayfa ayarını ayarla"
type: docs
url: /set-page-setup/
keywords: "Aspose.Cells, Excel, sayfa ayarı, REST API, çalışma sayfası, bulut SDK'sı"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfası için sayfa ayarını nasıl ayarlayacağınızı öğrenin. İstek detaylarını, güvenli HTTPS cURL örneğini, yanıt durum kodlarını ve birden fazla programlama dili için SDK kod parçacıklarını içerir."
weight: 20
ArticleTitle: "Bir çalışma sayfası için sayfa ayarını ayarla – Aspose.Cells Cloud API Kılavuzu"
---

Önkoşullar: Bu API'yi çağırmak için geçerli bir JWT (OAuth) jetonuna ve çalışma kitabının, okuma/yazma izinlerine sahip olduğunuz bir Aspose Cloud depolama konumunda bulunmasına ihtiyacınız vardır. Jetonun **Authorization** başlığında yer almasına ve hesabınızın gerekli API kotasına sahip olduğundan emin olun.

Bu REST API, bir Excel çalışma sayfası için sayfa ayarını ayarlar.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür    | Konum | Açıklama                |
| ------------- | ------ | ----- | ----------------------- |
| name          | string | path  | Belge adı.              |
| sheetName     | string | path  | Çalışma sayfası adı.    |
| pageSetup     | object | body  | Sayfa ayarı açıklaması. |
| folder        | string | query | Belge klasörü.          |
| storageName   | string | query | Depo adı.               |

**`pageSetup` nesnesi için örnek JSON yükü**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

<a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>, herkese açık erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

API, işlemin sonucunu gösteren bir JSON nesnesi döndürür:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Mümkün yanıt durum kodları**

| Kod | Anlamı                      | Durum                                                     |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK                          | Başarılı sayfa ayarı güncelleme                           |
| 400 | Bad Request (Geçersiz İstek)| Geçersiz JSON yükü veya eksik gerekli alanlar             |
| 401 | Unauthorized (Yetkisiz)     | Eksik veya geçersiz JWT jetonu                            |
| 404 | Not Found (Bulunamadı)      | Çalışma kitabının veya çalışma sayfasının adı yok         |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası                          |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en hızlı şekilde artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine istek nasıl yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
title: "Bir Excel çalışma sayfasındaki tüm resimleri silin"
second_title: "Belge"
linktitle: "Temizle"
type: docs
url: /tr/pictures/clear/
aliases: [  /tr/delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, tüm resimleri sil, çalışma sayfası, REST API, resimleri temizle"
description: "Aspose.Cells Cloud REST API ile bir Excel çalışma sayfasından tüm resimleri nasıl sileceğinizi cURL ve SDK örnekleriyle öğrenin."
weight: 60
ArticleTitle: "Aspose.Cells Cloud ile Bir Excel Çalışma Sayfasındaki Tüm Resimleri Nasıl Silirsiniz?"
---

Bu REST API, bir çalışma sayfasındaki **tüm** resimleri siler.

**Önkoşullar**  
- Geçerli bir OAuth 2.0 erişim belirteci ile aktif bir Aspose.Cells Cloud hesabı.  
- API sürümü 3.0 (veya daha üstü) gereklidir; önceki sürümler kullanım dışıdır.  
- Hedef Excel dosyası, desteklenen bir depolama konumunda (öntanımlı veya özel) saklanmalıdır.

**Sürüm Uyumluluğu**  
Uç nokta, Cells Cloud 3.0 API仕様ına uyar. İstemci kütüphanelerinizin ve istek URL’lerinizin `api.aspose.cloud/v3.0` adresini hedeflediğinden emin olun.

## DeleteWorksheetPictures API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür   | Konum | Açıklama                                     |
| -------------- | ------ | -------- | ------------------------------------------ |
| name           | string | Yol     | Excel dosyasının adı.                    |
| sheetName      | string | Yol     | Resimleri içeren çalışma sayfasının adı. |
| folder         | string | Sorgu   | Dosyanın bulunduğu klasör.           |
| storageName    | string | Sorgu   | Depolama hizmetinin adı.               |

### Hata Yanıtları

| HTTP Kodu | Açıklama                                                                    |
| --------- | ------------------------------------------------------------------------------ |
| 401       | Yetkisiz – eksik veya geçersiz belirteç.                                       |
| 404       | Bulunamadı – belirtilen dosya, çalışma sayfası veya sayfa kırma dizini mevcut değil. |
| 400       | Geçersiz İstek – hatalı istek sözdizimi veya geçersiz parametreler.                  |
| 500       | İç Sunucu Hatası – beklenmeyen bir durumla karşılaşıldı.               |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Grubu

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye detayları yöneterek iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Notlar:** DELETE işlemi sayfalamayi desteklemez ve standart Aspose.Cells Cloud API hız sınırlarına (öntanımlı 100 istek/dakika) tabidir. İstemci mantığınızı buna göre ayarlayın.

**Ayrıca bakınız**:  
- [/pictures/delete/](../delete/) – Bir çalışma sayfasından belirli bir resmi silin.  
- [/pictures/add/](../add/) – Bir çalışma sayfasına resim ekleyin.  
---
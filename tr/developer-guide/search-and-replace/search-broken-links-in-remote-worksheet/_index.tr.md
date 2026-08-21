---
title: "Aspose.Cells Cloud – Excel Bozuk Bağlantı Algılama API’si – Uzaktan Çalışma Sayfalarındaki Tablo Bağlantılarını Taranın ve Doğrulayın"
secondtitle: "Belge"
ArticleTitle: "Uzaktan Excel Çalışma Sayfasında Bozuk Bağlantıları Bulun ve Düzeltin – Bulut Tablo Bağlantı Denetleyicisi"
linktitle: "Uzaktan Çalışma Sayfasındaki Bozuk Bağlantıları Arayın"
type: docs
url: /search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, bozuk bağlantılar, Excel API, bulut tablo, bağlantı doğrulama"
description: "Bulut depolama alanında depolanan Excel çalışma sayfalarındaki harici bozuk bağlantıları algılayın ve düzeltin. Aspose.Cells Cloud API’sini kullanarak aralıkları tarayın, bağlantı ayrıntılarını alın ve kalite kontrolünü otomatikleştirin."
weight: 100
---

## **Uzaktan Çalışma Sayfasındaki Bozuk Bağlantıları Arama API’si**

Bulut depolama alanında depolanan bir Excel çalışma sayfasındaki bozuk bağlantıları otomatik olarak algılayın. API, belirtilen aralıkları tarayarak bozuk harici başvuruları, geçersiz formülleri ve eksik veri kaynaklarını tespit eder. Bulut depolama sağlayıcılarıyla entegrasyonu destekler, uzaktan tablo denetimi ve otomatik kalite kontrolü sağlar. Kurumsal iş akışı otomasyonu için RESTful API.

### **Web API’si**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı   | Tür      | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                                                                                                                                                                     |
| :-------------- | :------- | :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name            | String   | Yol                         | **Zorunlu.** Bozuk bağlantıların aranacağı Excel çalışma kitabının dosya adı (uzantısıyla birlikte) (örn. `Annual_Report.xlsx`).                                                                                           |
| worksheet       | String   | Yol                         | **Zorunlu.** Bağlantı taramasının yapılacağı çalışma sayfasının tam adı (örn. `DataSheet1`).                                                                                                                                 |
| folder          | String   | Sorgu                       | **İsteğe bağlı.** Hedef çalışma kitabının bulunduğu bulut depolama alanındaki dizin yolu. Belirtilmezse kök klasör kullanılır.                                                                                                |
| storageName     | String   | Sorgu                       | **İsteğe bağlı.** Özelleştirilmiş yapılandırılmış bulut depolama alanınızın tanımlayıcısı. Belirtilmezse, API hesabın varsayılan depolama alanını kullanır.                                                                   |
| region          | String   | Sorgu                       | **İsteğe bağlı.** Tarama sırasında uygulanacak yerel ayar (örn. `fr-FR`). Bu ayar, belirli formüllerin veya bölgesel veri formatlarının yorumlanmasını etkileyebilir. _Desteklenen yerel kodlar şunları içerir: `en-US`, `fr-FR`, `de-DE`, `es-ES`, vb._ |
| password        | String   | Sorgu                       | **İsteğe bağlı.** Şifreli bir tablo için şifre çözme şifresi. Dosya şifrelenmemişse boş bırakın.                                                                                                                              |

**Örnek cURL isteği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Annual_Report.xlsx/worksheets/DataSheet1/search/broken-links?folder=Reports&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Yanıt**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "Kaynak dosya bulunamadı"
    }
  ]
}
```

Yanıt nesnesi **BrokenLinksResponse** türündedir ve şunları içerir:

- **BrokenLinks** – `BrokenLink` nesnelerinden oluşan bir koleksiyon; her biri sorunlu başvuruyu (adres, hata kodu ve mesajı) açıklar.
- **Code** – Hizmet tarafından döndürülen sayısal durum kodu.
- **Status** – Sonucun metinsel açıklaması.

**Notlar**: API, sonuçları sayfalama yapmaz. Bir istekte en fazla 10.000 bozuk bağlantı döndürülebilir. Hesap başına rate limit (rate limiting) 100 istek/dakikadır.

### Hata Kodları

- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI’si.
- **401 Unauthorized** – Geçersiz veya eksik erişim belirteci.
- **404 Not Found** – Tablo dosyasına erişilemiyor.
- **500 Server Error** – Hesaplama verileri alınırken bir sorun oluştu.

## Excel Tablosunun Çalışma Sayfasındaki Bozuk Bağlantıları Arama API’si nerede kullanılmalıdır?

- **Büyük Finansal Modellerin Düzenli Denetimi**: Aylık veya çeyrek raporlar yayınlanmadan önce, büyük miktarda harici veri referansı içeren (örn. `Dashboard!B5:K50`) temel hesaplama alanlarını tarayarak tüm bağlantıların geçerli kaynak dosyalara işaret ettiğinden emin olun.
- **Birleşmeler ve İstihkaklar İçin Veri Entegrasyonu**: İşletme birimlerini temsil eden birden fazla tablo dosyası birleştirildikten sonra "Overview" (Genel Bakış) çalışma sayfasını tarayarak, kaynak dosya yollarındaki değişiklikler veya izin sorunları nedeniyle geçersiz hale gelen bağlantıları belirleyin.
- **Yatırımcı Veri Paketlerinin Hazırlanması**: Dış veritabanlarına veya pazar veri kaynaklarına bağlı grafikler ve tablolar içeren sunum materyalleri nihai hale getirilmeden önce tüm bağlantıların geçerliliğini kontrol edin.

## Neden Excel Tablosunun Çalışma Sayfasındaki Bozuk Bağlantıları Arama API’si kullanılmalıdır?

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar; hızlı geliştirme sağlar ve kapsamlı belgelerle birlikte gelir. Özelleştirilmiş grafik oluşturma çözümleri oluşturmakla karşılaştırıldığında, geliştirme iş yükünü büyük ölçüde azaltır.
- **İşgücü Maliyetlerini Azaltır**: Elle belge birleştirme ve bağlantı doğrulama görevleri için çalışan personel ihtiyacını ortadan kaldırır.
- **Öde-ve-Kullan**: Ön ödeme gerekmez; yalnızca kullandığınız API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım Maliyeti**: Bakımı yapılacak sunucu yok, yazılım güncellemesi yok, uyumluluk sorunu yok.
- **Karmaşık Excel Biçimlendirmesini Evrensel Erişimli PDF Formatında Korur.**

## Excel Tablosunun Çalışma Sayfasındaki Bozuk Bağlantıları Arama API’sini SDK’larla Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, alttaki detayları yöneterek Excel tablolarının çalışma sayfalarındaki bozuk bağlantıları aramayı minimum kodla uygulamanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---
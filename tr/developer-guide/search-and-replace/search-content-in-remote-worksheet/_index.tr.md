---
title: "Aspose.Cells Cloud Excel Metin Arama Web API’si – Uzak Çalışma Kitabında Metin Bulma"
second_title: "Doküman"
ArticleTitle: "Uzak Excel Çalışma Kitabı Çalışma Sayfasında Metin Arama – Belirli Verileri Bulma"
linktype: "İçerik Arama"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Aspose Cells, Excel API, metin arama, uzak çalışma sayfası"
description: "Aspose.Cells Cloud API kullanarak uzak bir Excel çalışma sayfasında metin, sayı veya formülleri arayın. Büyük/küçük harf duyarsız ve parolayla korumalı dosyaları destekler."
weight: 100
---

## **Uzak Çalışma Sayfasında İçerik Arama**

Aspose.Cells Cloud API kullanarak herhangi bir Excel çalışma sayfasında belirli bir metni programatik olarak arayın. Hizmet, bulut depolama alanında saklanan uzak dosyalarda metin, sayı veya formülleri bulabilir; böylece otomatik veri keşfi, içerik analizi ve elektronik tablo denetimi iş akışlarını sağlar.

### **Web API’si**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri**

| Parametre Adı | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                       |
| -------------- | ------- | --------------------------- | ------------------------------------------------------------------------------------------------- |
| name           | String  | Yol                         | **Zorunlu.** Hedef çalışma kitabının dosya adı (örneğin, `yillik_rapor.xlsx`).                   |
| worksheet      | String  | Yol                         | **Zorunlu.** Aramanın yapılacağı çalışma kitabındaki çalışma sayfası.                            |
| searchText     | String  | Sorgu                       | **Zorunlu.** Bulunacak tam metin dizesi veya sayı.                                              |
| ignoreCase     | Boolean | Sorgu                       | **İsteğe bağlı.** `true` olarak ayarlandığında arama büyük/küçük harf duyarlılığı yapmaz. Varsayılan değer `false`'tir. |
| folder         | String  | Sorgu                       | **İsteğe bağlı.** Çalışma kitabının bulunduğu klasörün yolu. Atlanırsa kök klasör kullanılır.    |
| storageName    | String  | Sorgu                       | **İsteğe bağlı.** Özelleştirilmiş yapılandırılmış bulut depolama adı. Atlanırsa varsayılan depo kullanılır. |
| region         | String  | Sorgu                       | **İsteğe bağlı.** Metin karşılaştırmasını etkileyebilecek yerel ayar (örneğin, `ja-JP`).          |
| password       | String  | Sorgu                       | **İsteğe bağlı.** Korumalı bir çalışma kitabının parolası. Dosya şifreli değilse atlayın.        |

### **Yanıt**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Toplam",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Toplam",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** – Eşleşmelerin dizisi. Her bir öğe, hücre adresini (`cellName`), eşleşen dizeyi (`text`) ve o hücrede kaç kez tekrar ettiğini (`occurrences`) içerir.
- **code** – Hizmetin döndürdüğü HTTP durum kodu.
- **status** – Sonucun metinsel açıklaması.

### **Hata Kodları**

- **400 Bad Request (Bad Request)** – Geçersiz API URI’si veya hatalı parametreler.
- **401 Unauthorized (Yetkisiz)** – Eksik veya geçersiz OAuth 2.0 belirteci.
- **404 Not Found (Bulunamadı)** – Çalışma kitabına veya çalışma sayfasına ulaşılamıyor.
- **500 Server Error (Sunucu Hatası)** – İstek işlenirken beklenmedik bir durum oluştu.

## Elektronik Tablo API’sinin Çalışma Sayfası İçerik Araması Nerede Kullanılmalı?

- **Çalışma kitabı uyumluluk denetimi:** “Gizli” gibi hassas terimleri dosyanın tamamında hızlıca bulun.
- **Çoklu sayfa veri ilişkilendirme:** Birden fazla sayfada geçen bir proje numarası veya müşteri adı bulun.
- **Şablon doğrulama:** Rapor oluşturulduktan sonra `{{Tarih}}` gibi yer tutucuların değiştirildiğini doğrulayın.
- **Tarihsel veri madenciliği:** Geçmiş iş mantığını anlamak için eski elektronik tablolarda belirli olay kodlarını arayın.

## Elektronik Tablo API’sinin Çalışma Sayfası İçerik Araması Neden Kullanılmalı?

- **Geliştirici dostu:** Birçok dil için SDK’lar, hızlı geliştirme sağlar ve tam olarak belgelenmiştir.
- **Düşük iş gücü maliyeti:** Elle veri birleştirme göreviyle uğraşan personel ihtiyacını azaltır.
- **Kullanım bedeli ödemeli:** Sadece gerçek olarak yaptığınız API çağrıları için ödeme yaparsınız.
- **Sıfır bakım:** Yönetilecek sunucu yoktur, yazılım güncellemesi gerekmez ve uyumluluk sorunları yoktur.
- **Sonuçları PDF veya diğer formatlara aktarırken karmaşık Excel formatlarını korur.**

## Elektronik Tablo API’sinin Çalışma Sayfası İçerik Araması SDK’ları ile Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, temel alınan ayrıntıları işler; böylece elektronik tabloların çalışma sayfasında içerik arama işlemini en az kodla uygulamanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.
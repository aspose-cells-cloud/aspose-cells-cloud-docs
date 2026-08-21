---
title: "Tablo Bağlantılarını Kontrol Et: Kırık Bağlantıları Bul ve Düzelt – Aspose.Cells Cloud API"
second_title: "Belge"
ArticleTitle: "Excel’de Kırık Bağlantıları Bul ve Düzelt – Bulut Tablo Bağlantı Denetleyicisi"
linktitle: "Tablo Kırık Bağlantılarını Ara"
type: docs
url: /tr/search-spreadsheet-broken-links/
keywords: "Aspose Cells, kırık bağlantılar, tablo denetimi, Excel API, bulut tablo, bağlantı denetleyicisi"
description: "Aspose.Cells Cloud API ile Excel çalışma kitaplarında kırık bağlantıları algıla ve düzelt. Aralıkları tarayın, ayrıntılı JSON sonuçları alın ve herhangi bir dil SDK’siyle entegre edin."
weight: 100
---

## **Tablo Kırık Bağlantılarını Ara API’si**

Excel dosyalarındaki kırık bağlantıları otomatik olarak algılayın. API, belirlenmiş aralıkları tarayarak kırık harici referansları, geçersiz formülleri ve eksik veri kaynaklarını tespit eder. Uzaktan tablo denetimi, otomatik kalite kontrolleri ve bulut depolama sağlayıcılarıyla entegrasyonu destekler. Kurumsal iş akışı otomasyonu için RESTful API.

**Özet:** Bu uç noktayı kullanarak çalışma kitaplarındaki geçersiz bağlantıları hızlıca belirleyin ve düzeltin; finansal modeller, BİT (birleşme ve satın alma) veri kümeleri ve yatırımcılar için hazır paketler gibi durumlarda veri bütünlüğünü sağlayın.

### **Web API’si**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sayfa1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@örnek.xlsx"
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### İstek Parametreleri

| Parametre Adı | Tür   | Konum             | Açıklama                                                                                                           |
|---------------|-------|-------------------|---------------------------------------------------------------------------------------------------------------------|
| Spreadsheet   | Dosya | FormData (multipart) | **Gerekli.** Analiz edilecek Excel çalışma kitap dosyası (`.xlsx`, `.xls`, vb.).                                         |
| worksheet     | Metin | Sorgu             | **İsteğe bağlı.** Analiz edilecek çalışma sayfasının adı. Atlanırsa ilk çalışma sayfası kullanılır.                          |
| cellArea      | Metin | Sorgu             | **İsteğe bağlı.** A1 gösterimiyle hedef hücre aralığı (örn. `B2:D10`). Belirtilmezse kullanılan tüm aralık analiz edilir. |
| region        | Metin | Sorgu             | **İsteğe bağlı.** Tarih, sayı veya para birimi yorumlamasını etkileyebilecek yerel ayar (örn. `tr-TR`).                |
| password      | Metin | Sorgu             | **İsteğe bağlı.** Şifrelenmiş çalışma kitapları için parola. Dosya korunmuyorsa boş bırakın.                             |

### Yanıt

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Veri\\kaynak.xlsx",
      "ErrorMessage": "Dosya bulunamadı",
      "Status": "Kırık"
    },
    {
      "CellName": "C12",
      "Link": "http://ornek.com/data.csv",
      "ErrorMessage": "404 Bulunamadı",
      "Status": "Kırık"
    }
  ],
  "Code": 200,
  "Status": "Tamam"
}
```

### Hata Kodları

| Kod | Açıklama |
|-----|----------|
| **400 Bad Request** | Geçersiz Aspose.Cells Cloud API URI’si. |
| **401 Unauthorized** | Geçersiz erişim belirteci, istemci kimliği veya istemci gizli anahtarı. |
| **404 Not Found** | Tablo dosyasına erişilemiyor. |
| **429 Too Many Requests** | Oran sınırlaması aşıldı (dakikada 60 çağrı). |
| **500 Server Error** | Hesaplama verileri alınırken tabloda bir anomali oluştu. |


## Tablo Kırık Bağlantılarını Ara API’si nerede kullanılmalıdır?

- **Büyük Finansal Modellerin Düzenli Denetimi**: Aylık veya üç aylık raporlar yayınlanmadan önce, harici veri kaynaklarına çok sayıda referans içeren önemli hesaplama alanlarını (örn. `Dashboard!B5:K50`) otomatik olarak tarayarak tüm bağlantıların geçerli kaynak dosyalara işaret ettiğinden emin olun.  
- **Birleşmeler ve Satın Alımlar için Veri Entegrasyonu**: İş birliklerini temsil eden birden fazla tablo dosyası birleştirildikten sonra “Genel Bakış” çalışma sayfasını tarayarak, dosya yollarının değişmesi veya izin sorunları nedeniyle geçersiz hale gelen bağlantıları tespit edin.  
- **Yatırımcı Veri Paketlerinin Hazırlanması**: Dış veritabanlarına veya piyasa veri kaynaklarına bağlantılı grafikler ve tablolar içeren sunum materyalleri sonlandırılmadan önce tüm bağlantıların geçerliliğini kontrol edin.

## Tablo Kırık Bağlantılarını Ara API’si neden kullanılmalıdır?

- **Geliştirici Dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kitaplıkları sunar; hızlı geliştirme ve kapsamlı belgeler sağlar. Özel çözümler oluşturmakla karşılaştırıldığında geliştirme yükünü önemli ölçüde azaltır.  
- **Düşük İş Gücü Maliyeti** – Belgelerdeki bağlantıları manuel olarak doğrulamak için ayrı personel gereksinimini ortadan kaldırır.  
- **Ödeme-İkramiye Modeli** – Ön ödemeye gerek yoktur; sadece kullandığınız API çağrıları için ücret ödersiniz.  
- **Sıfır Bakım Maliyeti** – Bakımlı sunucu yoktur, yazılım güncellemesi yoktur ve uyumluluk sorunları yoktur.  
- **Karmaşık Excel Biçimlendirmesini Korur** – Sonuçlar, orijinal çalışma kitabının düzenini koruyarak evrensel olarak erişilebilir bir JSON formatında döndürülür.

## Tablo Kırık Bağlantılarını Ara API’si’ni SDK’larla Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"}, web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenize olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, temel detayları kendisi yönetir; böylece minimum kodla sadece “kırık bağlantıları ara” işlevselliğini uygulamanız gerekir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerine nasıl çağrı yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}


---
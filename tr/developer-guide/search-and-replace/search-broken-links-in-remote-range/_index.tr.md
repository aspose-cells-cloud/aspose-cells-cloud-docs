---
title: "Aspose.Cells Cloud – Excel Aralığında Bozuk Bağlantıları Tespit Etme (API)"
secondtitle: "Belge"
articletitle: "Uzaktaki Excel Aralığında Bozuk Bağlantıları Bul ve Düzelt – Bulut Tabanlı Elektronik Tablo Bağlantı Denetleyicisi"
linktitle: "Uzak Aralıktaki Bozuk Bağlantıları Ara"
type: docs
url: /search-broken-links-in-remote-range/
keywords: "Aspose, Cells, bozuk bağlantılar, API, Excel aralığı, doğrulama, bulut, elektronik tablo, dış referans, denetleyici"
description: "Aspose.Cells Cloud API’sini kullanarak belirli bir Excel aralığında bozuk dış bağlantıları, geçersiz formülleri veya eksik veri kaynaklarını tarayın. Güvenli, hızlı ve bulut tabanlı."
weight: 100
---

## **Uzak Aralıktaki Bozuk Bağlantıları Arama API’si**

Bulut depolama alanına kaydedilmiş Excel dosyalarının aralıktaki verilerinde otomatik olarak bozuk bağlantıları tespit edin. API, belirtilen aralıkları tarayarak bozuk dış referansları, geçersiz formülleri ve eksik veri kaynaklarını bulur. Bulut tabanlı elektronik tablo denetimi, otomatik kalite kontrolleri ve bulut depolama sağlayıcılarıyla entegrasyonu destekler. Kurumsal iş akışı otomasyonu için RESTful API.

### **Web API’si**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### İstek Parametreleri

| Parametre Adı | Tür    | Konum  | Açıklama                                                                                                                                                               |
|---------------|--------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name          | String | Yol    | **Gerekli.** Bozuk bağlantıları taranacak olan bulut depolama alanında bulunan Excel çalışma kitabının adı (örn. `mali_rapor.xlsx`).                                     |
| worksheet     | String | Yol    | **Gerekli.** Bozuk bağlantıların aranacağı çalışma kitabındaki belirli bir çalışma sayfasının adı (örn. `Sayfa1`, `Q4_Veriler`).                                        |
| cellArea      | String | Yol    | **Gerekli.** Belirtilen çalışma sayfası içinde dış referansları, formülleri veya bağlantıları aramak için hedeflenen hücre aralığı adresi (örn. `A1:F100`).             |
| folder        | String | Sorgu  | **İsteğe bağlı.** Hedef çalışma kitabının bulunduğu bulut depolama alanındaki dizin yolu. Atlanırsa kök dizin varsayılır.                                                 |
| storageName   | String | Sorgu  | **İsteğe bağlı.** Yapılandırılmış bulut depolama hizmetinizin adı (örn. `DropboxBusiness`, `S3Bucket`). Belirtilmezse API, hesabın varsayılan depolamasını kullanır.    |
| region        | String | Sorgu  | **İsteğe bağlı.** Tarama sırasında bölgesel veri yorumlaması için uygulanacak yerel ayar (örn. `tr-TR`, `de-DE`).                                                       |
| password      | String | Sorgu  | **İsteğe bağlı.** Şifreli bir çalışma kitabına erişmek için gereken şifre çözme şifresi. Dosya şifreli değilse boş bırakın.                                               |

**Örnek İstek Gövdesi**

```json
{
  "name": "mali_rapor.xlsx",
  "worksheet": "Sayfa1",
  "cellArea": "A1:F100",
  "folder": "raporlar/2024",
  "storageName": "MyDropbox",
  "region": "tr-TR",
  "password": ""
}
```

### Yanıt

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

`BrokenLinks` koleksiyonu, **BrokenLink** türündeki nesneleri içerir. Her bir nesne aşağıdaki özellikleri sağlar:

- **CellName** – Bozuk referansı içeren hücrenin adresi (örn. `B12`).
- **LinkType** – Bozuk olan bağlantının türü (örn. `ExternalReference`, `Formula`).
- **ErrorMessage** – Bağlantının neden bozuk olarak değerlendirildiğine dair açıklama.

**Not**: API, hız sınırlarına tabidir. Ayrıntılar için [Fiyatlandırma ve Hız Sınırları](https://www.aspose.cloud/pricing) sayfasına bakın.

### Hata Kodları

- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI’si.
- **401 Unauthorized** – Geçersiz erişim belirteci, istemci kimliği veya istemci gizli anahtarı.
- **404 Not Found** – Elektronik tablo dosyasına erişilemiyor.
- **500 Server Error** – Elektronik tablo, hesaplama verilerini alırken bir sorunla karşılaştı.

## Elektronik Tablo API’sinin aralığında bozuk bağlantıları aramayı nerede kullanmalıyız?

- **Büyük miktarda veri içeren mali modellerin düzenli denetimi** – Aylık veya üç aylık raporlar yayınlanmadan önce, çok sayıda dış veri kaynağına referans içeren ana hesaplama alanlarını (örn. `Dashboard!B5:K50`) tarayarak tüm bağlantıların geçerli kaynak dosyalara işaret ettiğinden emin olun.
- **Birleşmeler ve İstihkaklar için veri entegrasyonu** – İş birimlerini temsil eden birden fazla elektronik tablo dosyasını birleştirirken, entegrasyondan sonra “Genel Bakış” çalışma sayfasını tarayarak dosya yollarındaki veya izinlerdeki değişiklikler nedeniyle geçersiz hale gelen bağlantıları belirleyin.
- **Yatırımcı veri paketlerinin hazırlanması** – Harici veritabanlarına veya pazar veri kaynaklarına bağlı grafik ve tablolar içeren sunum materyalleri sona erdirilmeden önce tüm bağlantıların geçerliliğini doğrulayın.

## Elektronik Tablo API’sinin aralığında bozuk bağlantıları aramayı neden kullanmalıyım?

- **Geliştirici dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kitaplıkları sunar ve kapsamlı belgelerle hızlı geliştirme sağlar. Özel bir çözüm oluşturmaya kıyasla, geliştirme çabasını önemli ölçüde azaltır.
- **Düşük iş gücü maliyeti** – Belgeleri manuel olarak birleştirmek için özel personel gereksinimini ortadan kaldırır.
- **Kullanım başına ödeme** – Ön ödeme gerektirmez; yalnızca gerçekleştirdiğiniz API çağrıları için ödeme yaparsınız.
- **Sıfır bakım maliyeti** – Bakımı yapılacak sunucu yoktur, yazılım güncellemeleri gerekmez ve uyumluluk sorunları yoktur.
- **Karmaşık Excel formatını korur** – Sonuçlar, stillerini kaybetmeden evrensel olarak erişilebilir PDF formatına aktarılabilir.

## Elektronik Tablo API’sinin aralığında bozuk bağlantıları SDK’larla nasıl arayacağım?

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, gelişimi hızlandırmanın en iyi yoludur. SDK, altta yatan ayrıntıları yönetir ve “aralıkta bozuk bağlantıları ara” işlemini minimum kodla uygulamanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapılabileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
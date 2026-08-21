---
title: "Aspose.Cells Cloud – Excel Bozuk Bağlantı Algılama API’si – Uzaktan Çalışma Kitaplarında Elektronik Tablo Bağlantılarını Tarama ve Doğrulama"
secondtitle: "Belge"
articletitle: "Uzaktan Excel Dosyalarındaki Bozuk Bağlantıları Bulun ve Düzeltin – Bulut Elektronik Tablo Bağlantı Denetleyicisi"
linktitle: "Uzaktan Elektronik Tablolardaki Bozuk Bağlantıları Arayın"
type: docs
url: /tr/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, bozuk bağlantılar, API, bulut, elektronik tablo, doğrulama, Aspose.Cells"
description: "Aspose.Cells Cloud API’sini kullanarak uzaktan Excel çalışma kitaplarında bozuk harici bağlantıları, geçersiz formülleri ve eksik veri kaynaklarını tarama yapın."
weight: 100
---

## **Uzaktan Elektronik Tabloda Bozuk Bağlantıları Arama API’si**

Bulut depolama alanına kaydedilmiş Excel dosyalarındaki bozuk bağlantıları otomatik olarak algılayın. API’niz belirtilen aralıkları tarayarak bozuk harici referansları, geçersiz formülleri ve eksik veri kaynaklarını bulur. Bulut depolama sağlayıcılarıyla entegrasyonu destekleyen uzaktan elektronik tablo denetimi, otomatik kalite kontrolü ve entegrasyon yeteneğine sahiptir. Kurumsal düzeyde iş akışlarınızı otomatikleştirmek için RESTful API’yi kullanın.

### **Web API’si**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvendedir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı   | Tür      | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                              |
| :-------------- | :------- | :--------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| name            | String   | Yol                          | **Gerekli.** Bozuk bağlantılar için taranacak Excel çalışma kitap dosyasının adı (örneğin `Quarterly_Report.xlsx`).                                  |
| worksheet       | String   | Sorgu                        | **Gerekli.** Arama işlemisinin yapılacağı çalışma sayfasının adı. Çalışma kitabında görünen şekilde tam sayfa adını belirtin.                          |
| cellArea        | String   | Sorgu                        | **Gerekli.** Bozuk bağlantılar için analiz edilecek hücre aralığı, A1 gösteriminde ifade edilir (örneğin `C5:J50`). API yalnızca bu alanda arama yapar.|
| folder          | String   | Sorgu                        | **İsteğe bağlı.** Çalışma kitabının bulunduğu dizinin yolu. Atlanırsa kök dizin varsayılan alınır.                                                   |
| storageName     | String   | Sorgu                        | **İsteğe bağlı.** Özel bulut depolama yapılandırmanızın adı. Atlanırsa sistem varsayılan depolama alanını kullanır.                                 |
| region          | String   | Sorgu                        | **İsteğe bağlı.** İşlem sırasında uygulanacak yerel ayar (örneğin `tr-TR`). Bölgeye özel formül sözdizimi veya referansların yorumlanmasını etkileyebilir.|
| password        | String   | Sorgu                        | **İsteğe bağlı.** Şifrelenmiş bir elektronik tabloyu açmak için gereken şifre. Dosya şifre korumalı değilse atlayın.                                  |

**Örnek cURL isteği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Yanıt**

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

**Örnek JSON yanıtı**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "Dosya bulunamadı"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "Bulut modunda harici referans desteklenmiyor"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Hata Kodları

- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI’si.  
- **401 Unauthorized** – Geçersiz erişim belirteci, istemci kimliği veya istemci gizli anahtarı.  
- **404 Not Found** – Elektronik tablo dosyasına erişilemiyor.  
- **500 Server Error** – Hesaplama verileri alınırken beklenmedik bir hata oluştu.

## Uzaktan Elektronik Tabloda Bozuk Bağlantıları Arama API’si nerede kullanılmalıdır?

- **Büyük finansal modellerin düzenli denetimi** – Aylık veya çeyrek raporları yayınlamadan önce, birçok harici veri kaynağı referansı içeren ana hesaplama alanlarını (örneğin `Dashboard!B5:K50`) otomatik olarak tarayarak tüm bağlantıların geçerli kaynak dosyalara işaret ettiğinden emin olun.  
- **Birleşmeler ve satın almalar için veri entegrasyonu** – İş birimlerini temsil eden birden fazla elektronik tabloyu birleştirirken, entegrasyon sonrası “Overview” sayfasını tarayarak dosya yollarında veya izin sorunlarında oluşan geçersiz bağlantıları belirleyin.  
- **Yatırımcı veri paketlerinin hazırlanması** – Harici veritabanlarına veya piyasa veri kaynaklarına bağlantılı grafik ve tablolar içeren sunum materyallerini nihai hale getirmeden önce tüm bağlantıların geçerliliğini doğrulayın.

## Neden Uzaktan Elektronik Tabloda Bozuk Bağlantıları Arama API’sini kullanmalısınız?

- **Geliştirici dostu** – Aspose.Cells Cloud, çok sayıda dilde SDK kütüphaneleri sunar ve kapsamlı belgelerle hızlı geliştirme sağlar. Özel bir çözüm geliştirmeye kıyasla geliştirme çabasını ciddi oranda azaltır.  
- **Düşük iş gücü maliyeti** – Bağlantı doğrulamayı otomatikleştirerek belgeleri manuel olarak birleştirmek için özel personel gerektirmesini ortadan kaldırır.  
- **Kullanıma göre ödeme** – Ön ödemeye gerek yoktur; yalnızca kullandığınız API çağrıları için ödeme yaparsınız.  
- **Sıfır bakım maliyeti** – Bakımı yapılacak sunucu yoktur, yazılım güncellemeleri gerekmez ve uyumluluk sorunları yoktur.

## Uzaktan Elektronik Tabloda Bozuk Bağlantıları Arama API’sini SDK’larla Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirmeyi hızlandırmanın en etkili yoludur. SDK, temel HTTP ayrıntılarını soyutlayarak minimum kodla bozuk bağlantı algılama özelliğini uygulamanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetleriyle nasıl etkileşime girileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}
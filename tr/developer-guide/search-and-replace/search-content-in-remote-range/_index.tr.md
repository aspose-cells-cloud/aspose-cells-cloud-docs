---
title: "Aspose Cells Cloud Excel Metin Arama API’sı – Uzaktan Elektronik Tablo Aralıklarında Metin Bulma"
second_title: "Belge"
ArticleTitle: "Uzaktan Excel Elektronik Tablolarda Metin Arama – Belirli Aralıklarda Veri Bulma"
linktitle: "Uzak Aralık İçeriğini Arama"
type: docs
url: /tr/search-content-in-remote-range/
keywords: "Aspose.Cells, Excel API, metin arama, uzak aralık, bulut elektronik tablo, REST API, veri keşfi"
description: "Aspose Cloud’da depolanan bir Excel çalışma kitabının belirli bir aralığında metin, sayı veya formül arayın."
weight: 100
---

## **Uzak Aralığın İçeriğini Arama**

Aspose.Cells Cloud API’si ile elektronik tablo aralıklarında belirli metinleri programatik olarak arayın. Bulut depolama alanınızda depolanan uzak dosyalarda metin, sayı veya formülleri bulun. Otomatik veri keşfi, içerik analizi ve elektronik tablo denetim iş akışları için REST tabanlı API.

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```


**cURL Örneği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### İstek Parametreleri

| Parametre Adı | Tür    | Yol/Sorgu/Dize/HTTPBody | Açıklama                                                                                                                                         |
| :------------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Yol                       | **Gerekli**. Arama yapılacak Excel çalışma kitabının dosya adı (uzantı dahil), örneğin `customer_data.xlsx`.                                       |
| worksheet      | String  | Yol                       | **Gerekli**. Aramanın yapılacağı çalışma kitabındaki çalışma sayfasının tam adı, örneğin `Orders_2024`.                                                |
| cellArea       | String  | Yol                       | **Gerekli**. Aramanın yapılacağı hedef hücre aralığı, A1 gösterimiyle belirtilir (örneğin `B2:H100`). Arama bu alana kısıtlıdır.                |
| searchText     | String  | Sorgu                     | **Gerekli**. Tanımlanan hücre aralığında bulunacak belirli metin dizesi, sayı veya kısmi içerik.                                            |
| ignoreCase     | Boolean | Sorgu                     | **İsteğe bağlı**. `true` olarak ayarlandığında, arama büyük/küçük harf farklılıklarını görmezden gelir (örneğin “Report”, “report” ile eşleşir). Varsayılan değer `false` (büyük/küçük harfe duyarlıdır).       |
| folder         | String  | Sorgu                     | **İsteğe bağlı**. Çalışma kitabının bulunduğu bulut depolama alanındaki dizin yolu. Atlanırsa kök dizin kullanılır.                       |
| storageName    | String  | Sorgu                     | **İsteğe bağlı**. Özel bir bulut depolama yapılandırmasının tanımlayıcısı. Belirtilmezse, hesabın varsayılan depolama alanı kullanılır.               |
| region         | String  | Sorgu                     | **İsteğe bağlı**. Arama sırasında bölgesel karakter veya formatların yorumlanmasını etkileyebilecek kültür/bölge ayarı (örneğin `en‑AU`). |
| password       | String  | Sorgu                     | **İsteğe bağlı**. Şifreli bir elektronik tablo dosyasının şifresini çözmek ve erişmek için gerekli şifre. Dosya şifreli değilse atlayın.                          |

### Yanıt

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

### Hata Kodları

- **400 Bad Request (Kötü İstek)** – Geçersiz Aspose.Cells Cloud API URI’si.  
- **401 Unauthorized (Yetkisiz)** – Geçersiz erişim belirteci, istemci kimliği veya istemci gizli anahtarı.  
- **404 Not Found (Bulunamadı)** – Elektronik tablo dosyasına erişilemiyor.  
- **500 Server Error (Sunucu Hatası)** – Sunucunun isteği yerine getirmesini engelleyen beklenmeyen bir durum oluştu.

## Elektronik Tablonun Aralığında İçerik Arama API’si Nerede Kullanılmalı?

- **Büyük Ölçekli Veri Kalitesi Kontrolü** – Veri ambarı ETL süreçlerinin kabul aşamasında, eksik alan açıklamalarını, tanımlanmamış kısaltmaları veya yer tutucu metni (örneğin, `"TBD"` veya `"NULL"`) veri eşleme tablosunda (`DataDictionary!B2:F1000`) arayarak eksik veri tanımlarını belirleyin.  
- **Dinamik Raporlama ve İçerik Çıkarma** – Otomatik raporlama sistemlerinde, karışık veriler içeren şablon çalışma sayfalarından (`Monthly_Metrics!C10:G50`) belirli tanımlayıcılarla (örneğin `"[KPI]"`) işaretlenmiş mevcut dönem veri bloklarını akıllıca arayın ve çıkararak nihai raporu oluşturun.  
- **Sözleşme ve Yasal Belge Analizi** – Birçok madde içeren elektronik tablo ekleri incelenirken, tanımlı bir aralıkta (`Contract_Terms!A:A`) belirli yasal terimleri (örneğin `"liability limit"`), taraf adlarını veya tarihleri verimli bir şekilde bulun ve inceleme sürecini hızlandırın.

## Elektronik Tablonun Aralığında İçerik Arama API’si Neden Kullanılmalı?

- **Geliştirici dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar; bu da özel çözümler oluşturmak yerine hızlı geliştirme ve kapsamlı belgeler sağlayarak geliştirme yükünü önemli ölçüde azaltır.  
- **Düşük iş gücü maliyeti** – Belge birleştirme işini yürütmek için özel personel gereksinimini ortadan kaldırır.  
- **Kullanım başına ödeme** – Önceden yatırım gerektirmez; yalnızca kullanılan API çağrıları için ödeme yaparsınız.  
- **Sıfır bakım maliyeti** – Bakımı yapılacak sunucu yoktur, yazılım güncellemesi gerekmez ve uyumluluk sorunları yoktur.

## Elektronik Tablonun Aralığında İçerik Arama API’sini SDK’lar ile Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanımı, geliştirme hızını en çok artıran yöntemdir. SDK, temel detayları yönetir; böylece elektronik tablo hücreleri için aralık içinde içerik arama işlemlerini en az kodla uygulayabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---
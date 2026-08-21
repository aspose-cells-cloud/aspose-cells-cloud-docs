---
title: "Uzak Excel Çalışma Kitaplarında Metin Arama – Aspose.Cells Cloud API"
second_title: "Belge"
ArticleTitle: "Uzak Excel Çalışma Kitaplarında Metin Arama – Belirli Verileri Bulma"
linktype: "Search Remote Spreadsheet Content"
type: docs
url: /tr/search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, Excel arama API'si, bulut çalışma kitapları, metin arama, REST"
description: "Aspose.Cells Cloud kullanarak bulut depolama alanında saklanan Excel dosyalarında metin, sayı veya formül arayın. Büyük/küçük harf duyarsız sorguları, klasör seçimi ve şifreli çalışma kitaplarını destekler."
weight: 100
---

### **Uzak Çalışma Kitabında İçerik Arama API’si**

Aspose.Cells Cloud API’sini kullanarak herhangi bir Excel çalışma kitabında programlı olarak belirli metinleri arayın. Bulut depolama alanında saklanan dosyalarda metin, sayı veya formülleri bulun. Bu RESTful API, otomatik veri keşfi, içerik analizi ve çalışma kitabları denetim süreçlerini mümkün kılar.

### **Web API’si**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı   | Tür       | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                      |
| :-------------- | :-------- | :--------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name            | String    | Yol                          | **Zorunlu**. Metin aramasının yapılacağı Excel çalışma kitabının dosya adı (uzantısı dahil), örneğin `sales_data.xlsx`.                                      |
| searchText      | String    | Sorgu                        | **Zorunlu**. Çalışma kitabının tamamında veya çalışma sayfasında(sayfalarında) bulunacak olan tam dize, sayı veya kısmi içerik.                                |
| ignoringCase    | Boolean   | Sorgu                        | **İsteğe bağlı**. Büyük/küçük harf duyarlılığını belirler. Büyük/küçük harf duyarsız eşleştirme için `true` olarak ayarlayın (örneğin “Rapor”, “RAPOR” ile eşleşir); varsayılan değer `false`'dır. |
| folder          | String    | Sorgu                        | **İsteğe bağlı**. Hedef çalışma kitabını içeren bulut depolama alanındaki dizin yolu. Atlanırsa kök klasör varsayılır.                                        |
| storageName     | String    | Sorgu                        | **İsteğe bağlı**. Özelleştirilmiş yapılandırılmış bir bulut depolama hizmeti için ad tanımlayıcısı. Belirtilmezse API, hesapla ilişkili varsayılan depoyu kullanır. |
| region          | String    | Sorgu                        | **İsteğe bağlı**. Arama sırasında uygulanacak yerel ayar (örneğin `tr-TR`); bu ayar metin normalleştirme veya karşılaştırma kurallarını etkileyebilir.         |
| password        | String    | Sorgu                        | **İsteğe bağlı**. Şifreli bir Excel dosyasına erişmek için gereken şifre çözme şifresi. Dosya şifrelenmemişse bu parametreyi atlayın.                         |

**Sözlük**

- **searchText** – Bulunacak tam dize; kısmi eşleşme de olabilir.
- **ignoringCase** – `true` aramayı büyük/küçük harf duyarsız yapar; `false` büyük/küçük harf duyarlılığını zorunlu kılar.
- **folder** – Çalışma kitabını içeren dizinin yolu.
- **storageName** – Özelleştirilmiş depo yapılandırmasının tanımlayıcısı.
- **region** – Metin karşılaştırma kurallarını etkileyen yerel kod.
- **password** – Korumalı çalışma kitapları için şifre çözme şifresi.

### **Yanıt**

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

Yanıt, aranan metnin bulunduğu hücrelerin listesini (`CellName`) ve çalışma sayfası adını ile eşleşen metni içerir. Eşleşme bulunamazsa `TextItems` dizisi boş döner ancak istek yine de HTTP 200 OK döndürülür.

### Hata Kodları

- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI’si.  
  ```json
  {"code":400,"message":"Invalid request URI"}
  ```
- **401 Unauthorized** – Geçersiz erişim belirteci, istemci kimliği veya istemci gizli anahtarı.  
  ```json
  {"code":401,"message":"Invalid access token"}
  ```
- **404 Not Found** – Çalışma kitab dosyasına ulaşılamıyor.  
  ```json
  {"code":404,"message":"File not found"}
  ```
- **500 Server Error** – API'nin isteği tamamlamasını engelleyen beklenmeyen bir durum oluştu.  
  ```json
  {"code":500,"message":"Internal server error"}
  ```

## Çalışma Kitabında İçerik Arama API’si Nerede Kullanılmalı?

- **Kapsamlı çalışma kitabı uygunluk denetimi** – Kurumsal veri güvenliği ve uygunluk kontrolü için tüm Excel dosyasını hızlıca tarayın ve tüm hassas terimleri (örneğin “Gizli Madde”, “İç Veri”) bulun.
- **Çoklu sayfa verisi ilişkilendirme sorgusu** – Proje bilgileri birden fazla çalışma sayfasına dağıtılmışsa, belirli bir proje numarasını veya müşteri adını arayın ve ilgili tüm verileri anında bulun.
- **Toplu şablon içerik doğrulama** – Otomatik rapor oluşturma işleminden sonra, tüm önceden tanımlı yer tutucuların (`{{Date}}` gibi) doğru şekilde değiştirildiğini doğrulamak için birden fazla Excel dosyasını toplu olarak tarayın; böylece raporların eksiksiz ve doğru olmasını sağlayın.
- **Tarihsel veri arşivleme ve madencilik** – Eski dosyaları analiz edin, belirli olay kodlarını veya iş terimlerini arayın ve veri arkeolojisi amacıyla tarihsel iş mantığını hızlıca anlayın.

## Çalışma Kitabında İçerik Arama API’si Neden Kullanılmalı?

- **Geliştirici dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar ve kapsamlı belgelerle hızlı geliştirme sağlar. Özel çözümler geliştirmeye kıyasla geliştirme çabasını büyük ölçüde azaltır.
- **Düşük iş gücü maliyeti** – Tekrarlayan arama görevlerini otomatikleştirir, geliştiricileri manuel veri çıkarma işlerinden serbest bırakır.
- **Kullanım başına ödeme** – Önceden ödeme gerektirmez; sadece kullandığınız API çağrıları için ödeme yaparsınız.
- **Bakım gerektirmez** – Aspose sunucuları, güncellemeleri ve uyumluluğu yönetir; böylece uygulama mantığına odaklanabilirsiniz.
- **Karmaşık Excel formatlarını korur** – Sonuçlar orijinal stillendirme korunarak evrensel olarak erişilebilir PDF formatına aktarılabilir.

## Çalışma Kitabında Bozuk Bağlantıları Arama Nasıl Yapılır? – SDK’larla

### OpenAPI Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme hızını en çok artıracak yoldur. SDK, arka plandaki ayrıntıları yöneterek, hücrelerdeki çalışma kitaplarında içerik arama işlevselliğini en az kodla uygulamanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub Deposu</a>'na bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---
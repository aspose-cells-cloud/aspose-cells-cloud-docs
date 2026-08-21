---
title: "Aspose.Cells – Kelime Büyük/Küçük Harf Güncelleme API'si"
second_title: "Belge"
linktype: "docs"
url: /tr/post-update-word-case/
keywords: "Aspose.Cells, Kelime Büyük/Küçük Harf Güncelleme API'si, metin büyük/küçük harf dönüştürme, Excel, CSV, Google Sheets, REST API"
description: "Aspose.Cells Cloud’un Kelime Büyük/Küçük Harf Güncelleme API’si ile Excel, CSV veya Google Sheets dosyalarındaki metin büyük/küçük harflerini dönüştürün. Büyük/küçük harf, başlık büyük harf ve ilk harf büyük harf formatlarını destekler."
weight: 100
ArticleTitle: "Aspose.Cells – Kelime Büyük/Küçük Harf Güncelleme API'si Belgesi"
---

**API sürümü:** 3.0

Yaygın olarak büyük/küçük harf tutarsızlığı içeren elektronik tablolarda (Excel, Google Sheets, CSV) çalışmak can sıkıcı olabilir, özellikle büyük veri setleriyle çalışırken. **PostUpdateWordCase web API’si**, metin büyük/küçük harf dönüşümlerini otomatikleştirerek minimum çaba ile temiz ve standartlaştırılmış veriler elde etmenizi sağlar.


## **Excel Web API’si – Kelime Büyük/Küçük Harf Güncelleme API'si**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İşlev Açıklaması**

PostUpdateWordCase web API’si, elektronik tablolarda yaygın olarak görülen metin büyük/küçük harf tutarsızlığı sorununa çözüm sunar; bu durum, veri analizini ve işlemeyi ciddi şekilde etkileyebilir. Bu API, büyük/küçük harf dönüşümlerini otomatikleştirerek verilerinizin temiz, standartlaştırılmış ve ileriye dönük manipülasyon veya analiz için hazır olmasını sağlar.

- **Otomatik Metin Büyük/Küçük Harf Dönüşümü**
  - **Büyük Harften Küçük Harfe** – Tüm büyük harfleri küçük harfe dönüştürür.
  - **Küçük Harften Büyük Harfe** – Tüm küçük harfleri büyük harfe dönüştürür.
  - **İlk Harfi Büyük Yap** – Her kelimenin ilk harfini büyük harfe çevirir.
  - **Başlık Büyük Harfi** – Her ana kelimenin ilk harfini büyük harf yaparak metni başlık büyük harfi formatına dönüştürür.

- **Birden Fazla Format Desteği** – API, Excel, OpenOffice, JSON, CSV ve diğerleri dahil olmak üzere geniş bir elektronik tablo formatı yelpazesini destekler. Bu esneklik, çeşitli veri işleme ihtiyaçları için uygundur.

### **İstek Parametreleri**

| Parametre Adı       | Tür     | Konum           | Açıklama                                                                                                                 |
| ------------------- | ------- | --------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions`   | nesne   | İstek gövdesi   | Kaynak aralık, hedef büyük/küçük harf türü ve diğer ek ayarlar gibi istenen büyük/küçük harf dönüşümünü tanımlayan seçenekler. |

**`wordCaseOptions` şeması**

```json
{
  "Range": "A1:B10", // İşlenecek Excel tarzı aralık (zorunludur)
  "CaseType": "Upper", // Numaralandırma: Upper, Lower, Capitalize, Title (zorunludur)
  "IgnoreBlank": true // Boole, isteğe bağlı – true ise boş hücreler değişmeden bırakılır
}
```

**Örnek istek gövdesi**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – Büyük/küçük harf dönüşümünün uygulanacağı hücre aralığı (örneğin, `A1:C5`).
- **CaseType** – Uygulanacak büyük/küçük harf dönüşümü türü. İzin verilen değerler: `Upper`, `Lower`, `Capitalize`, ve `Title`.
- **IgnoreBlank** – `true` ise boş hücreler yoksayılır; varsayılan değer `false`’tır.

### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[birleştirilmiş dosya adı]",
    "Filesize" : [dosya boyutu],
    "FileContent" : "[Base64Dizisi]"
}
```

- **Filename** – İşlenmiş dosyanın adı.
- **FileSize** – Dosyanın bayt cinsinden boyutu.
- **FileContent** – Dönüştürülmüş dosyanın Base64 ile kodlanmış içeriği.

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | İstek Gövdesi Çok Büyük     | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası. |

## PostUpdateWordCase API’yi SDK’lar ile Nasıl Kullanılır?

### PostUpdateWordCase API Belirtimi

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">OpenAPI Belirtimi</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye ayrıntıları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub Deposu</a>na göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---
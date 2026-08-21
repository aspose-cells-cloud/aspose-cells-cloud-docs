---
title: "Aspose.Cells Cloud Pozisyona Göre Karakter Silme Web API’si – Excel’de Belirli Konumlardan Metin Silme"
second_title: "Belge"
ArticleTitle: "Excel Pozisyon Tabanlı Karakter Silici – Belirli Konumlardan Metin Silme – Çevrimiçi Kısa Kod"
linktitle: "Pozisyona Göre Karakterleri Sil"
type: docs
url: /tr/remove-characters-by-position/
keywords: "Aspose.Cells Cloud, pozisyona göre karakter silme, Excel metin temizleme, ilk N karakteri silme, son N karakteri silme, belirleyici metinden önceki metni silme, belirleyici metinden sonraki metni silme, aradaki değerlerin silinmesi"
description: "Aspose.Cells Cloud Web API’sini kullanarak Excel hücrelerinden pozisyona göre karakterler silin—ilk/son N karakteri veya belirli belirleyicilerden önceki/sonraki metni yüksek doğrulukla silin."
weight: 100
---

Pozisyona göre Excel hücrelerinden karakterleri silin: ilk/son N karakteri silin veya belirtilen belirleyicilerden önceki/sonraki metni silin. Aspose.Cells Cloud Web API’si ile hassas metin temizleme.

## **Giriş**: Pozisyona Göre İstenmeyen Karakterleri Silme

**Konum modları**

- `theFirstNCharacters` – metnin başından itibaren N karakteri siler
- `theLastNCharacters` – metnin sonundan itibaren N karakteri siler
- `allCharactersBeforeText` – belirtilen alt metnin ilk oluşumundan önceki tüm karakterleri siler
- `allCharactersAfterText` – belirtilen alt metnin ilk oluşumundan sonraki tüm karakterleri siler
- `BetweenValues` – iki kullanıcı tanımlı değer arasındaki alt metni (ve isteğe bağlı olarak sınırlayıcı karakterleri kendilerini) kaldırır

**Seçenekler**

- `caseSensitive` – `BeforeText`, `AfterText` ve `BetweenValues` için aramaların büyük/küçük harf duyarlı olup olmadığını belirler

## **RemoveCharactersByPosition API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **RemoveCharactersByPosition** API’sinin istek parametreleri şunlardır:

| Parametre Adı         | Tür      | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                           |
| --------------------- | -------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet           | Dosya    | FormData                      | İşlenecek hesap tablosu dosyası. Desteklenen formatlar arasında XLSX, XLS, ODS, CSV vb. bulunmaktadır.                                                            |
| Authorization         | Metin    | Header                        | Kimlik doğrulama için Bearer belirteci (zorunludur).                                                                                                               |
| theFirstNCharacters   | Tamsayı  | Sorgu                         | Seçilen her hücredeki metnin başından itibaren silinecek karakter sayısı (örneğin `3`, ilk 3 karakteri siler).                                                    |
| theLastNCharacters    | Tamsayı  | Sorgu                         | Seçilen her hücredeki metnin sonundan itibaren silinecek karakter sayısı (örneğin `2`, son 2 karakteri siler).                                                    |
| allCharactersBeforeText | Metin  | Sorgu                         | Her hücrede belirtilen metin dizisinden önce gelen tüm karakterleri siler. Metin birden fazla kez geçiyorsa, silme işlemi ilk oluşuma göre yapılır.                |
| allCharactersAfterText  | Metin  | Sorgu                         | Her hücrede belirtilen metin dizisinden sonra gelen tüm karakterleri siler. Metin birden fazla kez geçiyorsa, silme işlemi ilk oluşuma göre yapılır.             |
| worksheet             | Metin    | Sorgu                         | _(İsteğe bağlı)_ Karakter silme işleminin uygulanacağı çalışma sayfasının adı. Atlanırsa, işlem ilk çalışma sayfasına uygulanır.                                   |
| range                 | Metin    | Sorgu                         | _(İsteğe bağlı)_ Karakter silme işleminin uygulanacağı hücre aralığı (örneğin `"A1:C10"`). Atlanırsa, işlem belirtilen çalışma sayfasındaki tüm kullanılan hücrelere uygulanır. |
| outPath               | Metin    | Sorgu                         | _(İsteğe bağlı)_ İşlenmiş çalışma kitabının kaydedileceği bulut depolama klasör yolu. Atlanırsa, dosya kaynak klasörde kaydedilir.                               |
| outStorageName        | Metin    | Sorgu                         | Çıktı dosyasının depolanacağı bulut depolamanın adı.                                                                                                               |
| region                | Metin    | Sorgu                         | _(İsteğe bağlı)_ Metin işleme için yerel ayarı belirler; özellikle dil özgü karakter konumları ve kodlamalar için önemlidir (örneğin `"en-US"`, `"zh-CN"`).         |
| password              | Metin    | Sorgu                         | _(İsteğe bağlı)_ Yüklenen hesap tablosu parola korumalıysa, dosyayı açmak ve işlemek için parolayı sağlayın.                                                       |

### **Yanıt**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Hata Kodları

- **200 OK** – İstek başarılı oldu ve işlenmiş dosya döndürüldü.
- **400 Bad Request**: Geçersiz Aspose.Cells Cloud API URI’si.
- **401 Unauthorized**: Geçersiz erişim belirteci veya geçersiz istemci kimliği ve gizli anahtarı.
- **404 Not Found**: Hesap tablosu dosyasına erişilemiyor.
- **500 Server Error**: Hesap tablosu, hesaplama verilerini alırken bir anomaliyle karşılaştı.

## Remove Characters by Position API’si nerede kullanılmalı?

- **Veri Standartlaştırma**: Ürün kodlarını temizleme (önek sıfırları veya sonekleri silme), telefon numaralarını temizleme (ülke kodlarını silme)
- **Metin Çıkarma**: Günlük dosyalarından önemli bilgileri çıkarma (zaman damgalarını veya önekleri silme)
- **Dosya İşleme**: Dosya adlarını düzenleme (tek tip önekleri veya tarih soneklerini silme)
- **Veri Ayrıştırma**: Yapılandırılmış metin işleme (parantezler veya belirli belirleyiciler arasında içerik çıkarma)
- **Veritabanı Yönetimi**: İçe aktarılan verileri temizleme (sabit formatlı başlık/sonuç karakterlerini silme)

## Remove Characters by Position API’si neden kullanılmalı?

- **Hassas ve Verimli**: Doğrudan pozisyon tabanlı silme, karmaşık normal ifadelerin kullanımını ortadan kaldırır.
- **Esnek Yapılandırma**: Beş konum modu ve büyük/küçük harf duyarlılık seçeneği, çeşitli senaryoları kapsar.
- **Toplu İşleme**: Tek bir çağrıyla tüm sütunları temizleyerek verimliliği en fazla 10 kat artırır.
- **Akıllı Ayrıştırma**: İki sınırlayıcı arasında kalan içeriği çıkarmayı kolayca yönetir.
- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dil için SDK’lar sağlar; bu da geliştirme hızını artırır ve kapsamlı belgeler sunar. Özel metin işleme mantığı oluşturmakla karşılaştırıldığında, bu işlem geliştirme yükünü büyük ölçüde azaltır.
- **Maliyet Etkin**: Çalışma kitabını önceden yüklemeksizin karakterler silinebilir; bu da depolama alanından tasarruf sağlayarak maliyetleri düşürür.

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, altta yatan ayrıntıları işler ve hücrelerde karakterleri pozisyona göre silme işlemini minimum kodla uygulamanızı sağlar.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl istekte bulunulacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---
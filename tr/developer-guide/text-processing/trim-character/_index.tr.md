---
title: "Aspose.Cells Cloud Metin Kırpma Web API'si - Ekstra Boşlukları ve Satır Sonlarını Kaldırın"
secondtitle: "Belge"
articletitle: "Excel Veri Temizleyici - Karakterleri, Boşlukları ve Satır Sonlarını Otomatik Kırpın – Çevrimiçi, Kısa Kod"
linktitle: "Karakter Kırp"
type: docs
url: /trim-character/
keywords: "Excel, metin kırpma, boşlukları kaldır, satır sonları, Aspose.Cells, veri temizleme, elektronik tablo, hücre formatını normalize et"
description: "Aspose.Cells Cloud API ile Excel hücrelerinden ekstra boşlukları, satır sonlarını ve gereksiz karakterleri kırpin. Temiz ve tutarlı elektronik tablo verileri sağlayın."
weight: 100
---

Aspose.Cells Trim Character API’sini kullanarak Excel hücrelerindeki gereksiz karakterleri, fazla boşlukları ve satır sonlarını otomatik olarak kırpin. Veri girişlerini temizleyin ve elektronik tablolarınızda tutarlı bir formatlama koruyun.

## **Genel Bakış**

- **İlk ve son boşlukları kırpin**
  - Metnin başındaki ve sonundaki fazla boşlukları kaldırın
  - Verilerin görünümünü daha düzenli ve okunabilir hale getirin
- **Kelimeler arasındaki fazla boşlukların işlenmesi**
  - Kelimeler arasındaki fazla boşlukları ortadan kaldırın
  - Çoklu kaynaklı verilerin neden olduğu format kafa karışıklığını çözün

- **Özel boşluklar kaldırılır**
  - Özel olarak, kesinlikle kırılmayan boşlukları (non-breaking spaces) temizleyin
  - Veri doğruluğunu ve tutarlılığını sağlayın

- **Satır sonu yönetimi**
  - Fazla veya tüm satır sonlarını kaldırın
  - Hücre içeriğini düzenli ve profesyonel görünümde tutun

## **TrimCharacter API'si**

API'yi çağırmadan önce geçerli bir Aspose Cloud hesabınızın, bir `client_id`/`client_secret` ve **Cells** kapsamlı bir erişim belirtecinizin olduğundan emin olun.

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **TrimCharacter** API'sinin istek parametreleri

| Parametre Adı          | Tür     | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                                                                                                         |
| :---------------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Elektronik Tablo        | Dosya   | FormData                   | İşlenecek elektronik tablo dosyası. Desteklenen formatlar arasında XLSX, XLS, ODS, CSV vb. yer alır.                                                                           |
| trimContent             | Dize    | Sorgu                      | Hücre içeriğinden kırılmasını belirttiğiniz karakterleri veya dizeleri belirtir. Tek bir karakter, çoklu karakterler veya özel bir desen olabilir.                  |
| trimLeading             | Boolean | Sorgu                      | `true` olduğunda, hücre içeriğinin başına belirtilen karakterleri kaldırır.                                                                            |
| trimTrailing            | Boolean | Sorgu                      | `true` olduğunda, hücre içeriğinin sonundan belirtilen karakterleri kaldırır.                                                                                  |
| trimSpaceBetweenWordTo1 | Boolean | Sorgu                      | `true` olduğunda, her hücredeki kelimeler arasındaki birden fazla ardışık boşluğu tek bir boşluğa düşürür.                                                                  |
| trimNonBreakingSpaces   | Boolean | Sorgu                      | `true` olduğunda, hücre içeriğinden kesinlikle kırılmayan boşluk karakterlerini (Unicode U+00A0) kaldırır.                                                                          |
| removeExtraLineBreaks   | Boolean | Sorgu                      | `true` olduğunda, her hücredeki birden fazla ardışık satır sonunu tek bir satır sonuna düşürür.                                                                      |
| removeAllLineBreaks     | Boolean | Sorgu                      | `true` olduğunda, hücre içeriğinden tüm satır sonu karakterlerini kaldırır.                                                                                               |
| worksheet               | Dize    | Sorgu                      | _(İsteğe bağlı)_ Metin kırpmasının uygulanacağı çalışma sayfasının adı. Atlanırsa işlem ilk çalışma sayfasına uygulanır.                               |
| range                   | Dize    | Sorgu                      | _(İsteğe bağlı)_ Metin kırpmasının uygulanacağı hücre aralığı (örneğin `"A1:C10"`). Atlanırsa işlem belirtilen çalışma sayfasındaki tüm kullanılmış hücrelere uygulanır. |
| outPath                 | Dize    | Sorgu                      | _(İsteğe bağlı)_ İşlenmiş çalışma kitabının kaydedileceği bulut depolama klasör yolu. Atlanırsa dosya kaynak klasörde kaydedilir.                          |
| outStorageName          | Dize    | Sorgu                      | Çıktı dosyasının depolanacağı bulut depolamanın adı.                                                                                                 |
| region                  | Dize    | Sorgu                      | _(İsteğe bağlı)_ Metin işleme için yerel ayarı ayarlar; bu, belirli diller için boşluk ve satır sonu işleme davranışını etkileyebilir (örneğin `"en-US"`, `"ar-SA"`).               |
| password                | Dize    | Sorgu                      | _(İsteğe bağlı)_ Yüklenen elektronik tablo şifreliyse, dosyayı açıp işlemek için şifreyi sağlayın.                                                  |

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

**Başarı örneği (HTTP 200):** API, kırpmış olduğunuz çalışma kitabını içeren bir dosya akışı döndürür.

### Hata Kodları

- **400 Bad Request**: Geçersiz Aspose.Cells Cloud API URI'si.
- **401 Unauthorized**: Geçersiz erişim belirteci. Veya geçersiz client id ve secret.
- **404 Not Found**: Elektronik tablo dosyasına erişilemiyor.
- **500 Server Error**: Elektronik tablo, hesaplama verilerini alırken bir anomaliyle karşılaştı.

## Trim Character API nerede kullanılmalı?

- **Kullanıcı Girdisi Normalizasyonu**: Elle girilmiş kullanıcı veri tablolarını temizleyin, fazla boşlukları ve satır sonlarını kaldırın.
- **Müşteri Veritabanı Bakımı**: Müşteri adlarında, adreslerinde ve iletişim bilgilerindeki gereksiz boşlukları ve formatlama sorunlarını temizleyin.
- **Otomatik Rapor Temizleme**: Otomatik rapor oluşturma öncesinde veri kaynağı formatını temizleyin.
- **Veri Taşıma Hazırlığı**: Veri yeni sisteme taşınmadan önce formatlama sorunlarını temizleyin.

## Trim Character API neden kullanılmalı?

- **Düşürülmüş İşgücü Maliyeti**: Veri temizleme için zaman alıcı manuel çabaları ortadan kaldırın
- **Hata Maliyetinin Azalması**: Formatlama sorunlarından kaynaklanan analiz hatalarını önleyin
- **Kullanım Ücretli**: Sabit ücret yoktur; sadece gerçek kullanım miktarına göre faturalandırılır
- **Sıfır Altyapı Yatırımı**: Sunucu veya yazılım bakımına gerek yoktur
- **Çoklu Format Desteği**: XLSX, XLS, CSV, ODS vb. gibi çoklu format işlemeyi destekler
- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar; hızlı geliştirme yapmanıza olanak tanır ve kapsamlı belgelerle birlikte gelir. Özel grafik oluşturma çözümleri oluşturmakla karşılaştırıldığında geliştirme iş yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Çalışma kitabını önceden yüklemeye gerek kalmadan tekrarlayan karakterleri kaldırabilirsiniz; bu, depolama alanını tasarruf eder ve maliyetleri düşürür.

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, alt seviye detayları yöneterek, hücrelerdeki metni kırpmak için minimum kod ile sadece Trim Character işlemini uygulamanızı sağlar.
Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapıldığını göstermektedir:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---
title: "Aspose.Cells Cloud – Kelime Büyük/Küçük Harf Değiştirme (Büyük, Küçük, Baş Harf Büyük, Cümle Büyük Harf)"
ArticleTitle: "Excel Büyük/Küçük Harf Dönüştürücüsü – Büyük Harf, Küçük Harf, Baş Harf Büyük Harf ve Cümle Büyük Harf"
linktitle: "Kelime Büyük/Küçük Harf"
type: docs
url: /tr/change-word-case/
keywords: "kelime büyük/küçük harf değiştirme API'si, Aspose.Cells, Excel büyük/küçük harf dönüştürme, büyük harf, küçük harf, baş harf büyük harf, cümle büyük harf, metin formatlama"
description: "Aspose.Cells Cloud API'sini kullanarak Excel dosyalarındaki metin büyük/küçük harfini kolayca dönüştürün. Büyük Harf, Küçük Harf, Baş Harf Büyük Harf ve Cümle Büyük Harf formatlarını destekler. C#, Java, Python ve diğerleri için kod örneklerini edinin."
weight: 100
---

## **Kelime Büyük/Küçük Harfini Değiştirme**

Aspose.Cells Cloud Web API'sini kullanarak elektronik tablonuzdaki metin büyük/küçük harfini anında dönüştürün—seçili bir aralıkta büyük harf, küçük harf, baş harf büyük harf (her kelimenin ilk harfini büyük harf yapma) veya cümle büyük harf (her cümlenin ilk harfini büyük harf yapma) arasında geçiş yapın. Yalnızca metin hücreleri etkilenir; sayılar, mantıksal değerler, hatalar ve boş hücreler yok sayılır. Formüller, formatlama ve veri doğrulama değiştirilmez.

- **UpperCase** – Her karakter büyük harfe çevrilir.
- **LowerCase** – Her karakter küçük harfe çevrilir.
- **ProperCase** – Her kelimenin ilk harfi büyük, geri kalanları küçük harfe çevrilir.
- **SentenceCase** – Her cümlenin ilk harfi büyük, geri kalanları küçük harfe çevrilir.

<img src="images/result.png" alt="Önce/sonra büyük/küçük harf dönüştürme ekran görüntüsü" width="800" height="450" />

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```
### **UpdateWordCase** API'si İçin İstek Parametreleri

| Parametre Adı | Tür   | Konum     | Açıklama                                                                                                                                                               |
| :------------- | :----- | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet    | Dosya  | FormData | İşlenecek elektronik tablo dosyası. Desteklenen formatlar arasında XLSX, XLS, ODS, CSV vb. yer alır.                                                                    |
| wordCaseType   | Dize   | Sorgu    | Metin büyük/küçük harf dönüştürme türünü belirtir: `UpperCase`, `LowerCase`, `ProperCase` veya `SentenceCase`.                                                         |
| worksheet      | Dize   | Sorgu    | _(İsteğe bağlı)_ Büyük/küçük harf dönüştürmenin uygulanacağı çalışma sayfasının adı. Atlanırsa, işlem çalışma kitabının ilk çalışma sayfasına uygulanır.                 |
| range          | Dize   | Sorgu    | _(İsteğe bağlı)_ Büyük/küçük harf dönüştürmenin uygulanacağı hücre aralığı (örneğin, `"A1:C10"`). Atlanırsa, işlem belirtilen çalışma sayfasındaki tüm kullanılan hücrelere uygulanır. |
| outPath        | Dize   | Sorgu    | _(İsteğe bağlı)_ İşlenmiş çalışma kitabının kaydedileceği bulut depolama klasör yolu. Atlanırsa, dosya kaynak klasörde kaydedilir.                                      |
| outStorageName | Dize   | Sorgu    | Çıktı dosyasının depolanacağı bulut depolamanın adı.                                                                                                                    |
| region         | Dize   | Sorgu    | _(İsteğe bağlı)_ Metin büyük/küçük harf kuralları için yerel ayarı ayarlar; özellikle dil özgüne büyük harf kuralları için önemlidir (örneğin, `"en-US"`, `"tr-TR"`).    |
| password       | Dize   | Sorgu    | _(İsteğe bağlı)_ Yüklenen elektronik tablo parola korumalıysa, dosyayı açmak ve işlemek için parolayı sağlayın.                                                         |

### Yanıt

Başarılı durumda hizmet, işlenmiş çalışma kitabının ikili akışını içeren JSON yüküyle birlikte **200 OK** (veya **202 Accepted**) döndürür.

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

- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI'si.
- **401 Unauthorized** – Geçersiz erişim belirteci veya yanlış istemci kimlik bilgileri.
- **404 Not Found** – Elektronik tablo dosyasına erişilemiyor.
- **500 Server Error** – Elektronik tabloda iç işlem hatası oluştu.

## Kelime büyük/küçük harf değiştirme API'si nerede kullanılmalıdır?

### Veri Temizleme ve Standartlaştırma

- **Müşteri Verisi Yönetimi** – Müşteri adları ve adres bilgilerinin büyük/küçük harfini standartlaştırın (örneğin, `john doe` → `John Doe`).
- **Ürün Kataloğu İşleme** – Ürün başlıkları ve açıklama metinlerini standartlaştırın (örneğin, `IPHONE 15 PRO` → `iPhone 15 Pro`).
- **Finansal Rapor Oluşturma** – Finansal tablolardaki ürün adları ve açıklama alanlarını normale getirin.

### Çoklu Kaynaklı Veri Entegrasyonu

- **Veri Ambarı ETL** – Farklı sistemlerden veri yüklerken metin formatını standartlaştırın.
- **API Verisi Alma** – Harici API’lerden dönen tutarsız büyük/küçük harfe sahip verileri işleyin.
- **Bölüm Arası Veri Birleştirme** – Farklı bölümlerin Excel raporlarındaki metin formatını standartlaştırın.

### İçerik Yönetim Sistemi

- **Otomatik Haber Basın duyuruları** – Haber başlıklarını ve içeriğini otomatik olarak biçimlendirin (başlık büyük/küçük harf kuralları).
- **Ürün Dokümantasyonu Oluşturma** – Teknik dokümantasyon terimlerinin formatlamasında tutarlılık sağlayın.
- **Bilgi Tabanı Bakımı** – SSS ve yardım belgelerinin metin formatını standartlaştırın.

### Kurumsal Uygulama Entegrasyonu

- **CRM Sistemi Entegrasyonu** – Müşteri verilerinin içe/dışa aktarımı sırasında adları ve şirket bilgilerini otomatik olarak biçimlendirin.
- **ERP Veri İşleme** – Malzeme açıklamaları ve tedarikçi adları gibi anahtar alanları standartlaştırın.
- **HR Yönetim Sistemi** – Çalışan bilgilerini ve iş pozisyonlarını standartlaştırın.

### Toplu Belge İşleme

- **Hukuki Belge Hazırlama** – Sözleşmeler ve anlaşmaların madde formatlarını toplu olarak işleyin.
- **Pazarlama Materyalleri Oluşturma** – Reklam metinlerinin ve e-posta şablonlarının metin formatlarını standartlaştırın.
- **Akademik Makale Formatlama** – Referans ve başlıklar için format gereksinimlerini standartlaştırın.

### Gerçek Zamanlı Veri İşleme

- **Kullanıcı Girdisi Doğrulama** – Kullanıcıların gönderdiği form verilerinin formatını gerçek zamanlı olarak ayarlayın.
- **Sohbet Botu Yanıtları** – Otomatik oluşturulan yanıtların metin formatını standartlaştırın.
- **Anlık Rapor Oluşturma** – Tek bir formatta iş raporlarını dinamik olarak oluşturun.

### Ulusallaştırma ve Yerelleştirme

- **Çok Dilli Veri İşleme** – Farklı dillerdeki metinler için büyük/küçük harf kurallarındaki farklılıkları işleyin.
- **Yerelleştirme İçeriği Hazırlama** – Farklı bölgeler için formatlanmış yerel içerik hazırlayın.
- **Çeviri Projesi Yönetimi** – Çeviri öncesi ve sonrası metin format tutarlılığını sağlayın.

## Kelime büyük/küçük harf değiştirme API'sini neden kullanmalısınız?

- **Geliştirici Dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kitaplıkları sunar; böylece hızlı geliştirme ve kapsamlı belgeler sağlar. Özel çözümler oluşturmak yerine bu, geliştirme iş yükünü önemli ölçüde azaltır.
- **Maliyet Etkin** – Çalışma kitabını önce yüklemeden kelime büyük/küçük harfini değiştirebilirsiniz; bu da depolama alanından tasarruf sağlar ve maliyetleri düşürür.

## OpenAPI Specification

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, alttaki ayrıntıları yönetir; böylece **UpdateWordCase**’i hücreler için minimal kodla uygulamanız yeterli olur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---
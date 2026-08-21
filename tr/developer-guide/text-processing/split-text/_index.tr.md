---
title: "Metin Bölme API’si – Excel Hücrelerini Sütunlara Ayırın | Aspose.Cells Cloud"
second_title: "Belge"
ArticleTitle: "Excel Metin Bölücü – Hücre İçeriğini Çoklu Sütunlara Ayırın | Aspose.Cells Cloud"
linktitle: "Metni Böl"
type: docs
url: /tr/split-text/
keywords: "Aspose, Cells, Metin Bölme API’si, Excel, ayıraç, metin segmentasyonu, bulut API’si"
description: "Aspose.Cells Cloud ile Excel hücre metnini kolayca ayrı sütunlara veya satırlara ayırın. Özel ayıraçları, maskelemeleri, satır sonlarını destekler ve ayıraçların korunmasını sağlar. Dakikalar içinde curl veya SDK’lar ile başlayın."
weight: 100
---

Özel segmentasyon kurallarını kullanarak Excel hücre metnini çoklu sütunlara ayırın. Aspose.Cells Cloud metin bölme Web API’si ile içeriği ayıraça göre ayırın ve belirtilen aralıklara çıktı verin.

## **Giriş**: Metni Bölme

Metin Segmentasyonu API’si, hücre içeriğini belirtilen ayıraçlara, kalıplara veya satır sonlarına göre birden fazla hücreye böler ve sonuçları hedef aralığa yazar. Esnek bölme yöntemlerini, yön belirleme çıktısını (sütun veya satır) ve ayıraçların korunmasını sağlar—birleştirilmiş verilerin, CSV tarzı içeriklerin veya çok satırlı metinlerin yapılandırılmış formatlara ayrıştırılması için idealdir.

- **Hücreyi belirli bir karaktere göre bölme** – hücre içeriğini herhangi bir karakteri (virgül, boşluk, noktalı virgül vb.) ayıraç olarak seçerek birden fazla hücreye bölün.
- **Hücreleri dizeye göre bölme** – belirttiğiniz karakter kombinasyonuna göre hücreleri ayırın.
- **Maskeye göre metni bölme** – belirli bir kalıba göre metni bölmek için joker karakterleri kullanın; bu, metin bölme konusunda daha esnek ve güçlü bir yöntem sunar.
- **Satır sonuna göre hücre içeriğini bölme** – satır sonlarına göre bölerek daha düzenli bir sunum oluşturun.
- **Hücreleri sütunlara veya satırlara bölme** – bölme sonuçlarının ardışık sütunlara mı yoksa satırlara mı yazılacağını seçin.
- **Ayıraçları kaldırma veya koruma** – ayıraçların sonuç hücrelerinin başında veya sonunda kaldırılıp kaldırılmayacağını veya konumlarını belirleyin.

## **SplitText API’si**

**Önkoşullar**: Bu API’yi kullanmak için geçerli bir Aspose Cloud erişim belirteci ve işlenecek çalışma kitabının Aspose Cloud deposuna yüklenmiş olması veya doğrudan isteğe dahil edilmiş olması gerekir. API, XLSX, XLS, ODS ve CSV gibi yaygın elektronik tablo formatlarını destekler.

### Web API’si

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **splitText** API’sinin istek parametreleri

| Parametre Adı                  | Tür      | Konum     | Gerekli mi? | Varsayılan     | Açıklama                                                                                                                                             |
| ------------------------------ | -------- | ---------- | ----------- | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | Dosya    | FormData   | Evet        | —              | İşlenecek elektronik tablo dosyası. Desteklenen formatlar: XLSX, XLS, ODS, CSV vb.                                                                   |
| delimiters                     | Dize     | Sorgu      | Hayır       | —              | Hücre içindeki metni bölmek için kullanılacak bir veya daha fazla ayıraç karakteri (örn., `","`, `";"`, `Boşluk`, `SatırSonu`, `Sekme`, `Pipe`, `Özel`). |
| keepDelimitersInResultingCells | Boole    | Sorgu      | Hayır       | false          | `true` ise, ayıraç karakterleri bölünmüş hücrelerde korunur.                                                                                         |
| keepDelimitersPosition         | Dize     | Sorgu      | Hayır       | None           | `keepDelimitersInResultingCells` `true` ise ayıraçların nerede tutulacağını belirtir. Seçenekler: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`. |
| howToSplit                     | Dize     | Sorgu      | Hayır       | SplitToColumns | Metin segmentasyonu yöntemi. Seçenekler: `None`, `SplitToColumns`, `SplitToRows`.                                                                   |
| outPositionRange               | Dize     | Sorgu      | Evet        | —              | Bölünen sonuçların yazılacağı hedef aralık (örn., `"D1:F10"`).                                                                                       |
| worksheet                      | Dize     | Sorgu      | Hayır       | —              | Metin bölme işleminin uygulanacağı çalışma sayfasının adı. Atlanırsa ilk sayfa kullanılır.                                                           |
| range                          | Dize     | Sorgu      | Hayır       | —              | Bölme işleminin uygulanacağı kaynak hücre aralığı (örn., `"A1:A10"`). Atlanırsa sayfadaki tüm kullanılmış hücreler işlenir.                          |
| outPath                        | Dize     | Sorgu      | Hayır       | —              | İşlenmiş çalışma kitabının kaydedileceği bulut depo klasör yolu. Atlanırsa dosya kaynak klasörde kaydedilir.                                         |
| outStorageName                 | Dize     | Sorgu      | Hayır       | —              | Çıktı dosyasının saklanacağı bulut depo adı.                                                                                                        |
| region                         | Dize     | Sorgu      | Hayır       | —              | Metin segmentasyonu için yerel ayar; bu, ayıraç yorumlamasını ve karakter kodlamasını etkileyebilir (örn., `"en-US"`, `"ja-JP"`).                       |
| password                       | Dize     | Sorgu      | Hayır       | —              | Şifreli bir elektronik tabloyu açmak için şifre.                                                                                                    |

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

- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI’si veya hatalı parametreler.
- **401 Unauthorized** – Eksik veya geçersiz erişim belirteci (veya client-id/secret).
- **404 Not Found** – Belirtilen elektronik tablo dosyasına ulaşılamadı.
- **500 Server Error** – Elektronik tablo içinde işlem hatası oluştu.

## Metin Bölme API’si nerede kullanılmalı?

### **CSV ve Metin Dosyası İçe Aktarma Temizleme**

Harici sistemlerden veri içe aktarırken alanlar sıklıkla tek bir hücreye birleştirilir:

- **ERP/CRM Veri İçe Aktarmaları** – `"John Doe;johndoe@email.com;555-1234"` ifadesini ayrı ad, e-posta ve telefon sütunlarına ayırın.
- **Veritabanı Dışa Aktarmaları** – `"ORD-2024-001|Premium|Express"` gibi birleştirilmiş anahtarları sipariş kimliği, seviye ve gönderim yöntemi olarak ayrıştırın.
- **Günlük Dosyası Analizi** – `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` gibi yarı-yapılandırılmış günlükleri filtreleme için bölün.

### **Eski Sistem Geçişleri**

- Eski sistemler çok-değerli alanları tek hücreye döker; bunları yeni veritabanı şemalarına göre bölün.
- Düz dosya dışa aktarmalarını Power BI veya Tableau için hazırleştirilmiş normalleştirilmiş Excel tablolarına dönüştürün.

### **Veri Temizleme ve Standartlaştırma**

- **Ayıraç Standardizasyonu** – `"A,B;C|D"` gibi karışık ayıraçları çoklu-ayıraç bölme ile tek bir formata dönüştürün.
- **Boşluk Temizleme** – Kelimeler arası fazla boşlukları belirlemek ve kaldırmak için boşluğa göre bölün.
- **Finansal Veriler** – `"DEP-CHK-3847"` gibi birleştirilmiş işlem kodlarını işlem türü, kaynağı ve referansı olarak ayırın.
- **Tıbbi Kayıtlar** – `"Smith,Jane_F_1985"` gibi hasta verilerini soyadı, adı, cinsiyeti ve doğum yılını olacak şekilde ayrıştırın.

## Metin Bölme API’si neden kullanılmalı?

- **Belirli Karakterler** – Virgül, noktalı virgül, sekme, boşluk gibi herhangi tek bir karaktere göre bölün.
- **Dize Kombinasyonları** – `||`, `->` veya özel ayıraçlar gibi çok karakterli ayıraçları kullanın.
- **Satır Sonları** – Çok satırlı hücreleri (adresler, yorumlar, açıklamalar) anında ayrı satırlara ayrıştırın.
- **Özel Ayıraçlar** – Ticari veri formatları için herhangi bir karakter kombinasyonunu ayıraç olarak tanımlayın.
- **Geliştirici Dostu** – Aspose.Cells Cloud, farklı dillerde SDK kitaplıkları sunar; hızlı geliştirme sağlar ve kapsamlı belgelerle birlikte gelir. Özel çözümler oluşturmaya göre geliştirme yükünü ciddi oranda azaltır.
- **Maliyet Etkin** – Çalışma kitabını önce yüklemeden tekrarlayan karakterleri kaldırabilirsiniz; bu, depolama alanını tasarruf ettirir ve maliyetleri düşürür.

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, gelişimi hızlandırmanın en iyi yoludur. SDK, alttaki detayları yönetir ve hücrelere metin bölme işlemini minimum kodla uygulamanıza izin verir. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}
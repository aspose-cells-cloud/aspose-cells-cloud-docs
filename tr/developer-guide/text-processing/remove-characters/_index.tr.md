---
title: "Aspose.Cells Cloud Remove Characters Web API – Excel Dosyalarından Özel Karakterleri ve Alt Dizeleri Silme (Çevrimiçi Kısa Kod)"
second_title: "Belge"
ArticleTitle: "Excel Metin Temizleyici – Seçilen Aralık Üzerinden Karakterleri ve Alt Dizeleri Silme"
linktitle: "Karakterleri Sil"
type: docs
url: /remove-characters/
keywords: "Aspose.Cells, karakterleri sil, Excel API, metin temizleme, elektronik tablo"
description: "Seçilen bir aralık içinde Excel hücrelerinden özel karakterleri, karakter kümelerini ve alt dizeleri silin. Aspose.Cells API’sini kullanarak belirli konumlardaki metni doğrulukla silin."
weight: 100
---

Seçilen hücre aralığından özel karakterleri, karakter kümelerini veya alt dizeleri silerek Excel verilerinizi temizleyin. Aspose.Cells API’si ile belirli konumlardaki metni doğru şekilde temizleyerek veri formatlamasını sağlayın.

## Giriş

Belirli istenmeyen karakterleri silerek Excel verilerinizi kolayca temizleyip standart hale getirin. Eklentimiz, hücrelerinizi temizlemek için birden fazla hedefli yöntemi sunar:

- **Özel Karakterleri Sil**  
  Tanımladığınız herhangi bir sembolü silin. Her karakteri alanın içine girin, eklenti seçili hücrelerdeki tüm örnekleri anında silecektir. Benzersiz ayıraçları, yazım hatalarını veya özel işaretleri ortadan kaldırmak için idealdir.

- **Karakter Kümelerini Sil (Toplu Temizleme)**
  - **Yazdırılmayan Karakterler** – Analizi ve formatlamayı bozan görünmez karakterleri verilerinizden temizleyin (satır sonları, satır başı, sekmeler ve diğer kontrol karakterleri; örneğin ASCII 0‑31, 127, 129, 141, 143, 144, 157).
  - **Metin Karakterleri (Tüm Harfler)** – Seçilen aralıktan her harfi (A‑Z, a‑z) kaldırarak sayıları ve sembolleri ayırt edin.
  - **Sayısal Karakterler (Tüm Rakamlar)** – Ürün adları veya metinsel açıklamaları temizlemek için ideal olan, tüm rakamları (0‑9) silerek saf metne ulaşın.
  - **Semboller** – Matematiksel (örn. ±, √), geometrik (örn. ∆, °), teknik, para birimi (örn. £, ¢) ve harf benzeri (örn. ™, ®, ©) semboller dahil olmak üzere geniş bir sembol karışıklığını silin.
  - **Noktalama İşaretleri** – Noktalar, virgüller, tırnak işaretleri ve tireler gibi tüm noktalama işaretlerini silerek temiz, noktalama işaretsiz metin elde edin.

- **Belirli Bir Alt Dizeyi Sil**  
  Tek karakterlerin ötesine geçerek tam kelimeleri veya belirli karakter dizilerini silin. Veri setlerinizden yaygın önekleri, sonekleri veya gereksiz metin ifadelerini kolayca kaldırın.

**Sürüm 4.0 – Güncellendi: 2024‑11‑15**

## RemoveCharacters API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### İstek Parametreleri

| Parametre Adı     | Tür     | Konum                   | Açıklama                                                                                                                                                                                                                      |
| ----------------- | ------- | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet       | Dosya   | FormData                 | İşlenecek elektronik tablo dosyası. Desteklenen formatlar: XLSX, XLS, ODS, CSV vb.                                                                                                                                           |
| removeTextMethod  | Metin   | Sorgu                    | Metin silme yöntemini belirtir. Seçenekler: `None`, `RemoveCustomCharacter`, `RemoveCharacterSets`, `RemoveSubString`. Varsayılan: `None`.                                                                                 |
| characterSets     | Metin   | Sorgu                    | `RemoveCharacterSets` seçildiğinde silinecek önceden tanımlanmış karakter kümesi(ler)i. Seçenekler: `NonPrintingCharacters`, `TextCharacters`, `NumericCharacters`, `Symbols`, `PunctuationMarks`. Birden fazla küme virgülle birleştirilebilir. |
| removeCustomValue | Metin   | Sorgu                    | `RemoveCustomCharacter` veya `RemoveSubString` kullanılırken silinecek özel karakter(ler) veya alt dize(ler).                                                                                                               |
| worksheet         | Metin   | Sorgu _(isteğe bağlı)_   | Metin silme işlemi uygulanacak çalışma sayfasının adı. **Atlandığında, API çalışma kitabının ilk çalışma sayfasını işler.**                                                                                                   |
| range             | Metin   | Sorgu _(isteğe bağlı)_   | Metin silme işlemi uygulanacak hücre aralığı (örn. `"A1:C10"`). **Atlandığında, işlem belirtilen çalışma sayfasındaki tüm kullanılan hücrelere uygulanır.**                                                                   |
| outPath           | Metin   | Sorgu _(isteğe bağlı)_   | İşlenmiş çalışma kitabının kaydedileceği bulut depolama klasör yolu. Atlanırsa dosya kaynak klasörde kaydedilir.                                                                                                              |
| outStorageName    | Metin   | Sorgu _(isteğe bağlı)_   | Çıktı dosyasının depolanacağı bulut depolamanın adı.                                                                                                                                                                          |
| region            | Metin   | Sorgu _(isteğe bağlı)_   | Karakter kümesi tanımları için yerel ayarı ayarlar (örn. `"en-US"`, `"ja-JP"`).                                                                                                                                               |
| password          | Metin   | Sorgu _(isteğe bağlı)_   | Gerekliyse korumalı bir çalışma kitabının şifresi.                                                                                                                                                                            |

### Yanıt

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

- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI’si.
- **401 Unauthorized** – Geçersiz erişim belirteci ya da yanlış istemci kimliği ve gizli anahtarı.
- **404 Not Found** – Elektronik tablo dosyasına erişilemiyor.
- **500 Server Error** – Elektronik tablo, hesaplama verileri alınırken bir sorunla karşılaştı.

## Remove Characters API Nerede Kullanılmalı?

- **Veri İçe/Dışa Aktarma** – Görünmez karakterleri ve formatlama hatalarını silerek içe aktarılan CSV/verileri temizleyin.
- **Veritabanı Yönetimi** – İstenmeyen semboller veya noktalama işaretlerini silerek ürün kodlarını, kimliklerini ve adlarını standart hale getirin.
- **Finansal Analiz** – Para birimi sembollerini ve metin karakterlerini kaldırarak saf sayısal verileri çıkarın.
- **Metin İşleme** – Temiz metin analizi ve raporlama için satır sonlarını ve sekmeleri silin.
- **Envanter Yönetimi** – Gereksiz önekler veya sonekleri kaldırarak ürün adlarını temizleyin.

## Remove Characters API Neden Kullanılmalı?

- **Zaman Tasarrufu** – Manuel temizlemeye kıyasla birden fazla karakter türünü anında toplu olarak silin.
- **Doğruluğu Sağlayın** – Analiz hatalarına ve formatlama sorunlarına neden olan gizli karakterleri ortadan kaldırın.
- **Verileri Standart Hale Getirin** – Veri setleri ve sistemler arasında tutarlı formatlama elde edin.
- **Analizi İyileştirin** – Sayıları veya metni gerektiği şekilde ayırt ederek temiz, analiz için hazır veriler elde edin.
- **İçe Aktarma Hatalarını Düzeltin** – Veritabanlarını ve formüllerini bozan sorunlu karakterleri silin.
- **Geliştirici Dostu** – Aspose.Cells Cloud, çok sayıda dilde SDK kitaplıkları sunar ve kapsamlı belgelerle hızlı geliştirme sağlar. Özel çözümler geliştirmeye kıyasla, geliştirme yükünü önemli ölçüde azaltır.
- **Maliyet Etkin** – Çalışma kitabını önceden yüklemek zorunda kalmadan karakterleri silin, depolama alanından tasarruf edin ve maliyetleri düşürün.

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, alttaki ayrıntıları yönetir ve **Karakterleri Sil** işlevini en az kodla hücrelere uygulamanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}
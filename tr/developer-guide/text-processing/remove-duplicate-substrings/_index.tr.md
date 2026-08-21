---
title: "Aspose.Cells Cloud Yinelenen Alt Dizeleri Kaldırma Web API’si – Excel’de Tekrar Eden Metni Temizle"
second_title: "Belge"
ArticleTitle: "Excel Yinelenen Alt Dizeleri Kaldırıcı – Hücrelerde Tekrar Eden Metni Temizleyin"
linktitle: "Yinelenen Alt Dizeleri Kaldır"
type: docs
url: /tr/remove-duplicate-substrings/
keywords: "Aspose.Cells, yinelenen alt dizeler, Excel API’si, metin temizleme, bulut"
description: "Aspose.Cells Cloud API’si ile Excel hücrelerinden yinelenen alt dizeleri kaldırırken formatlamayı ve doğrulamayı koruyun."
weight: 100
---

Excel hücrelerinden yinelenen alt dizeleri akıllı algılama ile kaldırın. Aspose.Cells temizleme API’si ile gereksiz metni kaldırırken orijinal formatlamayı koruyun.

## **Tanıtım**: İstenmeyen Karakterleri Kesinlikle Kaldırın

Yinelenen Alt Dize Temizleyici API’si, bir Excel aralığındaki hücrelerdeki yinelenen alt dizeleri kaldırırken hücre formatlamasını, veri doğrulamasını ve diğer çalışma kitaplığı yapılarını korur. Her hücreyi bağımsız olarak işler ve her yinelenen alt dizenin ilk oluşumunu korur.

### **Veri Kaynağı Seçenekleri**

| Alan          | Tür   | Gerekli | Açıklama                                             |
| ------------- | ----- | ------- | ---------------------------------------------------- |
| `workbook`    | dosya | Evet    | Excel çalışma kitaplığı dosyası (.xlsx, .xlsm)      |
| `range`       | string | Evet    | İşlenecek hedef aralık (örn. "A1:D100", "Sheet1!A:D") |

### **Ayırıcı Seçenekleri**

| Alan                               | Tür     | Varsayılan | Açıklama                                                                                                                                              |
| ---------------------------------- | ------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                       | string  | `"preset"` | Seçenekler: `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break` veya özel ayırıcı dizesi (birden fazla karakter birleşik olarak işlenir) |
| `treatConsecutiveDelimitersAsOne` | boolean | `false`    | Bitişik ayırıcıları tek bir ayırıcı olarak birleştirir                                                                                               |
| `caseSensitive`                    | boolean | `false`    | Karşılaştırmanın büyük/küçük harfe duyarlı olup olmadığını belirler. `false` olduğunda, yineleme algılama sırasında büyük/küçük harf dikkate alınmaz.   |

## **RemoveDuplicateSubstrings API’si**

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **RemoveDuplicateSubstrings** API’sinin İstek Parametreleri

| Parametre Adı                  | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                                         |
| :----------------------------- | :------ | :--------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                    | Dosya   | FormData                     | İşlenecek elektronik tablo dosyası. Desteklenen formatlar: XLSX, XLS, ODS, CSV vb.                                                                                              |
| delimiters                     | String  | Sorgu                        | Hücre içeriğini alt dizelere ayırmak için kullanılan bir veya daha fazla ayırıcı karakteri belirtir. Birden fazla ayırıcı belirtilebilir (örn. `",;"`).                         |
| treatConsecutiveDelimitersAsOne | Boolean | Sorgu                        | `true` ayarlandığında ardışık ayırıcı karakterler tek bir ayırıcı olarak kabul edilir. `false` olduğunda her ayırıcı ayrı ayrı işlenir.                                         |
| caseSensitive                  | Boolean | Sorgu                        | `true` olduğunda yinelenen alt dize algılama büyük/küçük harf duyarlıdır (örn. "Text" ≠ "text"). `false` olduğunda büyük/küçük harf yineleme karşılaştırmasında dikkate alınmaz.    |
| worksheet                      | String  | Sorgu                        | _(İsteğe bağlı)_ Yinelenen alt dize kaldırma işleminin uygulanacağı çalışma sayfasının adı. Belirtilmezse işlem ilk çalışma sayfasına uygulanır.                                   |
| range                          | String  | Sorgu                        | _(İsteğe bağlı)_ Yinelenen alt dize kaldırma işleminin uygulanacağı hücre aralığı (örn. `"A1:C10"`). Belirtilmezse işlem belirtilen çalışma sayfasındaki tüm kullanılan hücrelere uygulanır. |
| outPath                        | String  | Sorgu                        | _(İsteğe bağlı)_ İşlenmiş çalışma kitabının kaydedileceği bulut depolama klasör yoludur. Belirtilmezse dosya kaynak klasörde kaydedilir.                                        |
| outStorageName                 | String  | Sorgu                        | Çıktı dosyasının saklanacağı bulut depolamanın adı.                                                                                                                               |
| region                         | String  | Sorgu                        | _(İsteğe bağlı)_ Metin işleme için yerel ayarı ayarlar; bu, belirli diller için ayırıcı yorumlamasını ve büyük/küçük harf duyarlılık kurallarını etkileyebilir (örn. `"en-US"`, `"tr-TR"`). |
| password                       | String  | Sorgu                        | _(İsteğe bağlı)_ Yüklenen elektronik tablo parola korumalı ise, dosyayı açmak ve işlemek için parolayı belirtin.                                                                  |

**Örnek istek (cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
```

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

### **Durum Kodu**

| Kod | Anlam                                   | Açıklama                                                                                      |
|-----|-----------------------------------------|-----------------------------------------------------------------------------------------------|
| 200 | Tamam                                   | İstek başarıyla tamamlandı ve işlenmiş çalışma kitabı döndürüldü.                             |
| 202 | Kabul Edildi                            | İstek asenkron işlem için kabul edildi.                                                       |
| 400 | Geçersiz İstek                          | İstek hatalı biçimlendirilmiş veya geçersiz parametreler içeriyor.                           |
| 401 | Yetkisiz                                | Kimlik doğrulama başarısız oldu veya belirteç eksik/geçersiz.                                 |
| 404 | Bulunamadı                              | Belirtilen çalışma kitaplığı veya kaynak bulunamadı.                                         |
| 500 | Sunucu İç Hatası                        | Sunucu tarafında beklenmeyen bir hata oluştu.                                                 |

## Yinelenen Alt Dizeleri Kaldır API’si nerede kullanılmalı?

- **Veri Temizleme ve Standardizasyon Senaryoları**: Etiketleri temizleyin; örneğin `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.
- **Teknik ve İşletmsel Veriler**: Tekrar eden hata kodları içeren günlük girdilerini temizleyin, tekrar eden bin/rakam tanımlayıcılarını kaldırın vb.
- **İçerik ve Medya Yönetimi**: Yetenek etiketlerini temizleyin, gereksiz sertifika girişlerini kaldırın.

## Yinelenen Alt Dizeleri Kaldır API’si neden kullanılmalı?

- **El ile İşlemleri Otomatikleştirin**: Can sıkıcı düzenlemeleri ortadan kaldırın ve insan hatasını azaltın.
- **Veri Bütünlüğünü Koruyun**: Hücre renkleri, yazı tipleri, kenarlıklar ve koşullu formatlama değişmeden kalır; açılır listeler ve doğrulama kuralları korunur.
- **Esnek İşleme**: Ayırıcıdan bağımsız, isteğe bağlı büyük/küçük harf duyarlılığı kontrolü ve başlık koruması.
- **Geliştirici Dostu**: Aspose.Cells Cloud, çoklu dillerde SDK kitaplıkları sunar ve kapsamlı belgelerle hızlı geliştirme sağlar.
- **Maliyet Etkin**: İşlem bulutta gerçekleştirilir; ara dosyaların yerel olarak depolanmasına gerek kalmaz.

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, temel alınan ayrıntıları yönetir; bu sayede hücrelerdeki yinelenen alt dize kaldırma işlemini en az kodla uygulayabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:

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
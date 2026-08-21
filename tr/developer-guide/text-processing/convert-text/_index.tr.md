---
title: "Aspose.Cells Cloud Web API - Excel'de Metni Sayıya Dönüştürme ve Özel Karakterleri Temizleme"
secondtitle: "Belge"
articletitle: "Excel Veri Temizleyici - Metni Sayıya Dönüştürme ve İstenmeyen Karakterleri Kaldırma"
linktitle: "Metni Dönüştür"
type: docs
url: /tr/convert-text/
keywords: "Aspose.Cells metin dönüştürme, Excel'de metni sayiya çevirme, özel karakterleri Excel'den kaldırma, satır sonlarını Excel'de değiştirme, aksanlı karakterleri normalleştirme, Excel veri temizleme API'si"
description: "Aspose.Cells Cloud API kullanarak Excel dosyalarında metin biçimli sayıları sayısal değerlere dönüştürme, istenmeyen karakterleri ve satır sonlarını değiştirme ve aksanlı karakterleri standart harflere normalleştirme."
weight: 100
---

Aspose.Cells API ile Excel verilerini temizleyin: metin biçimindeki sayıları sayısal değerlere dönüştürün, istenmeyen karakterleri ve satır sonlarını değiştirin ve aksanlı karakterleri standart harflere normalleştirin.

## Genel Bakış

**Sayılar olarak saklanan metinleri dönüştürün, gereksizleri temizleyin, aksanları değiştirin — tek bir çağrı, sıfır formül.**

- **Metin olarak saklanan sayıları sayıya dönüştürün**: Metin olarak saklanan sayısal verileri gerçek sayılara dönüştürerek doğru hesaplamalar ve uygun veri gösterimi sağlayın.
- **Belirli karakterleri değiştirin**: Seçili hücrelerde belirtilen karakterlerin tüm örneklerini tek seferde değiştirerek verilerinizi standart hale getirin.
- **Satır sonlarını boşluk, virgül veya noktalı virgül ile değiştirin**: Okunabilirliği artırmak için satır sonlarını boşluk, virgül veya noktalı virgül ile değiştirerek daha düzenli ve görsel olarak çekici bir sunum oluşturun.
- **Aksanlı karakterleri değiştirin**: Verileriniz farklı dillerdeyse “é” veya “ü” gibi aksanlı karakterleri aksansız karşılıklarıyla değiştirerek tutarlılık ve netliği artırabilirsiniz.

## **ConvertText API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **convertText** API'sinin istek parametreleri şunlardır:

| Parametre Adı   | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                            |
| ---------------- | ------ | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Dosya  | FormData                      | İşlenecek elektronik tablo dosyası. Desteklenen formatlar şunları içerir: XLSX, XLS, ODS, CSV vb.                                                                   |
| convertTextType  | Dize   | Sorgu                         | Uygulanacak metin dönüştürme türünü belirtir; örneğin metin biçimindeki sayıları sayısal değerlere dönüştürme veya aksanlı karakterleri düz karşılıklarıyla değiştirme. |
| sourceCharacters | Dize   | Sorgu                         | Metinden değiştirilecek veya kaldırılacak karakterleri, dizileri veya desenleri belirtir (örn. `"é,è,ê"`, `"#N/A"`, `"\\n"` satır sonları için).                |
| targetCharacters | Dize   | Sorgu                         | Kaynak karakterleri değiştirecek değiştirme karakterlerini veya dizilerini belirtir (örn. aksanlı harfler için `"e"`, kaldırma için `""`, satır sonları için `" "`). |
| worksheet        | Dize   | Sorgu                         | _(İsteğe bağlı)_ Metin dönüştürmenin uygulanacağı çalışma sayfasının adı. Atlanırsa işlem ilk çalışma sayfasına uygulanır.                                          |
| range            | Dize   | Sorgu                         | _(İsteğe bağlı)_ Metin dönüştürmenin uygulanacağı hücre aralığı (örn. `"A1:C10"`). Atlanırsa işlem belirtilen çalışma sayfasındaki tüm kullanılan hücrelere uygulanır. |
| outPath          | Dize   | Sorgu                         | _(İsteğe bağlı)_ İşlenmiş çalışma kitabının kaydedileceği bulut depolama klasör yolu. Atlanırsa dosya kaynak klasörde kaydedilir.                                  |
| outStorageName   | Dize   | Sorgu                         | Çıktı dosyasının depolanacağı bulut depolamanın adı.                                                                                                                |
| region           | Dize   | Sorgu                         | _(İsteğe bağlı)_ Metin dönüştürme kuralları için yerel ayarı ayarlar; özellikle dil-özel karakter işleme için önemlidir (örn. `"en-US"`, `"fr-FR"`).               |
| password         | Dize   | Sorgu                         | _(İsteğe bağlı)_ Yüklenen elektronik tablo parola korumalıysa, dosyayı açmak ve işlemek için parolayı belirtin.                                                     |

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

- **400 Bad Request (Hatalı İstek)**: Geçersiz Aspose.Cells Cloud API URI'si.
- **401 Unauthorized (Yetkisiz)**: Geçersiz erişim belirteci veya geçersiz istemci kimliği ve gizli anahtarı.
- **404 Not Found (Bulunamadı)**: Elektronik tablo dosyasına erişilemiyor.
- **500 Server Error (Sunucu Hatası)**: Elektronik tablo hesaplama verilerini alırken bir sorunla karşılaştı.

## Convert Text API'si nerede kullanılmalı?

- **Sayı Biçimi Düzeltme**: Metin olarak saklanan sayıları (örn. “123.45”) hesaplamalar için uygun sayısal forma dönüştürün.
- **Özel Karakter Temizleme**: Verilerden gereksiz özel simgeleri, fazla boşlukları veya görünmez karakterleri kaldırın.
- **Satır Sonu Yönetimi**: Hücrelerdeki satır sonlarını boşluk veya diğer ayıraçlarla değiştirin.
- **Aksan Karakter Normalleştirme**: Aksanlı harfleri (örn. “é”, “ñ”) standart harflere (“e”, “n”) dönüştürün.
- **CSV Dosyası Ön İşleme**: CSV dosyalarını Excel'e içe aktarmadan önce metin formatını standartlaştırın.

## Convert Text API'si neden kullanılmalı?

- **Otomatik Biçim Dönüştürme**: Tek bir istekle metin biçimindeki sayıları toplu olarak hesaplanabilir değerlere dönüştürün.
- **Karakter Standartlaştırma**: Özel karakterleri, aksan işaretlerini ve kodlama sorunlarını tek bir şekilde ele alın.
- **Veri Tutarlılığı**: Tüm veri kümesinde metin formatının tamamen tutarlı olduğundan emin olun.
- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kitaplıkları sunar, hızlı geliştirme sağlar ve kapsamlı belgeler sağlar. Özel metin işleme çözümleri oluşturmaya kıyasla geliştirme iş yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Çalışma kitabını önce yüklemek zorunda kalmadan metin dönüştürebilirsiniz; bu, depolama alanını tasarruf eder ve maliyetleri düşürür.

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK'larını Kullanın

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, altta yatan ayrıntıları işler, böylece metin dönüştürmeyi hücrelerde minimum kodla uygulayabilirsiniz.  
Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
---
---
title: Aspose.Cells Cloud Web API - Parola ile E-Tablonun Korumasını Kaldır
second_title: Documen
ArticleTitle: Unprotect the Spreadsheet with passwor
linktitle: E-Tablonun Korumasını Kaldır
type: docs
url: /tr/unprotect-spreadsheet/
keywords: Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Managemen
description: Excel elektronik tablolarından çift katmanlı parola korumasını etkili bir şekilde kaldırır ve gelişmiş şifreleme teknikleriyle hem açık hem de değiştirilmiş parolaları destekler
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir
---
Excel numaralı elektronik tabloların şifreli olarak korunmasını sağlar, hem açma hem de değiştirme şifrelerini destekler.

## **E-Tablo Korumasını Kaldır API**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|Korumasız olmak için elektronik tablo dosyasını yükleyin.|
|şifre|Sicim|Sorgu|E-tablo dosyasının şifreleme parolası.|
|Şifreyi değiştir|Sicim|Sorgu|Korunan dosyayı değiştirmek için gereken şifre.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Korunmasız çalışma kitabının saklanacağı klasör yolu. Varsayılanı null'dır.|
|outStorageName|Sicim|Sorgu|Çıkış dosyasının depolama adını belirtir.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarlarını tanımlar.|

### **Cevap**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## Delete Spreadsheet Blank Columns API komutunu nerede kullanmalıyız?

Verilerinizi dönüştürmeniz gerektiğinde API'i kullanabilirsiniz.

## E-Tablodaki Boş Sütunları Sil API'i neden kullanmalısınız?

- Excel elektronik tablosundan herhangi bir veri veya başka nesne içermeyen tüm boş sütunları hızlıca silin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Delete Spreadsheet Blank Columns API Nasıl Kullanılır

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenizi sağlayan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, minimum kodla elektronik tablolardaki hücreler için boş sütunları silmenize olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

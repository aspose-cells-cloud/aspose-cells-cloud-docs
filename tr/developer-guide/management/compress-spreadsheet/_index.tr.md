---
title: Aspose.Cells Cloud Web API - Elektronik Tablonun boyutunu sıkıştırın
second_title: Documen
ArticleTitle: Compress the size of the Spreadshee
linktitle: Elektronik Tabloyu Sıkıştır
type: docs
url: /tr/compress-spreadsheet/
keywords: Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web AP
description: Sıkıştırılmış Elektronik Tablo API, kullanıcıların belirtilen sıkıştırma seviyelerini uygulayarak, depolama alanını optimize ederek ve performansı artırarak elektronik tabloların dosya boyutunu verimli bir şekilde azaltmalarına olanak tanır
weight: 100
kwords: Excel, Office Bulut, REST, Elektronik Tablo Sıkıştırma, Dosya Boyutu Optimizasyonu, PDF, CSV, Json, Markdow
---
E-tablonun boyutunu sıkıştırın.

## **Elektronik Tabloyu Sıkıştır API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|Sıkıştırılacak elektronik tablo dosyasını yükleyin.|
|seviye|Tam sayı|Sorgu|Uygulanacak sıkıştırma düzeyini belirtir; 0 (sıkıştırma yok) ile 9 (maksimum sıkıştırma) arasında değişir.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Sıkıştırılmış çalışma kitabının saklanacağı klasör yolu. Varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyası depolama adı.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarı.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için gereken şifre.|

### **Cevap**

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

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## API Sıkıştırılmış Elektronik Tablosunu nerede kullanmalıyız?

Elektronik tablolarınızın boyutunu küçültmeniz gerektiğinde API numarasını kullanabilirsiniz.

## Neden API Sıkıştırılmış Elektronik Tablosunu kullanmalısınız?

- E-tablo çok büyük ve dosya boyutunun küçültülmesi gerekiyor.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## API Sıkıştırılmış Elektronik Tablosunun SDK'larla Nasıl Kullanılacağı

### Sıkıştırılmış Elektronik Tablo API Spesifikasyonu

 The[Sıkıştırılmış Elektronik Tablo API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) REST etkileşimleri için herkese açık bir arayüz sağlar ve web tarayıcısından doğrudan API çağrılarına izin verir.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, kısa kodla elektronik tablo boyutunu sıkıştırmanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

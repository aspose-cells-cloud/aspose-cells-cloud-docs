---
title: Aspose.Cells Cloud Web API - Elektronik Tablo Verilerini PDF Dosyasına Dönüştürme
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Pdf file
linktitle: Tabloyu PD'ye Dönüştür
type: docs
url: /tr/convert-table-to-pdf/
keywords: Table to PDF conversion, Excel to PDF, REST API, Spreadsheet conversion, Aspose.Cells Cloud Web AP
description: Yerel sürücünüzdeki bir elektronik tablodan bir tabloyu verimli API'imizi kullanarak PDF dosyasına dönüştürün
weight: 100
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel tablo dönüştürme, Cloud PDF servisi
---
Yerel bir elektronik tablo/Excel tablosundaki verileri pdf dosyasına dönüştürün.

## **Tabloyu PDF API'e dönüştür**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|Dönüştürülecek elektronik tablo dosyasını yükleyin.|
|çalışma sayfası|Sicim|Sorgu|Spreadsheet/Excel çalışma sayfasının adı|
|tabloAdı|Sicim|Sorgu|Dönüştürülecek tablonun adı.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Dönüştürülen PDF'in saklanacağı klasör yolu. Varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyası depolamasının adını belirtin.|
|yazı tipleriKonum|Sicim|Sorgu|PDF için özel yazı tiplerini kullanın.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarını tanımlayın.|
|şifre|Sicim|Sorgu|E-tablo dosyasına erişim için şifre.|

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

## Neden Tabloyu Pdf'e Dönüştür API'i kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Convert Table to Pdf API Nasıl Kullanılır?

### Tabloyu PDF'e Dönüştür API Şartnamesi

 The[Tabloyu PDF'e Dönüştür API Şartnamesi](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToPdf) REST etkileşimlerini doğrudan bir web tarayıcısından yürütmek için herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablo tablosundaki verileri kısa kodla bir PDF dosyasına dönüştürmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}

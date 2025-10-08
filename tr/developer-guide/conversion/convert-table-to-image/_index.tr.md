---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Tablosu Verisini Bir Görüntüye Dönüştürme
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to an Imag
linktitle: Tabloyu Imag'a Dönüştür
type: docs
url: /tr/convert-table-to-image/
keywords: table to image, Aspose.Cells Cloud Web API, cloud conversion, spreadsheet to image, image format
description: Aspose.Cells Cloud Web API'i kullanarak yerel bir elektronik tablo tablosunu verimli bir şekilde bir görüntü dosyasına dönüştürün
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, tabloyu görüntüye dönüştürme, bulut dönüştürme, görüntü dosya biçimleri, elektronik tablo dönüştürme
---
 Yerel bir elektronik tablo/Excel tablosu verilerini görüntüye dönüştürün. Desteklenir**GÖRÜNTÜ FORMATLARI:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Tabloyu Görüntüye Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|E-tablo dosyasını yükleyin.|
|çalışma sayfası|Sicim|Sorgu|Spreadsheet/Excel çalışma sayfasının adı|
|tabloAdı|Sicim|Sorgu|Dönüştürülecek tablonun adı.|
|biçim|Sicim|Sorgu|İstenilen resim dosya biçimi (örneğin, png, svg).|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Dönüştürülen görüntünün saklanacağı klasör yolu. Varsayılanı null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyasının depolama adını belirtin.|
|yazı tipleriKonum|Sicim|Sorgu|Gerekirse özel yazı tipleri kullanın.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarlarını tanımlar.|
|şifre|Sicim|Sorgu|E-tablo dosyasına erişmek için şifre gerekiyor.|

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

## Neden Tabloyu Görüntüye Dönüştür API'i kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Tabloyu Görüntüye Dönüştürme API Nasıl Kullanılır?

### Tabloyu Görüntüye Dönüştür API Spesifikasyonu

 The[Tabloyu Görüntüye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToImage) REST etkileşimlerini doğrudan bir web tarayıcısından yürütmek için herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablonun verilerini kısa kodla bir görüntüye dönüştürmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{< /tab >}}
{{< /tabs >}}

---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Aralığı Verisini Görüntüye Dönüştürme
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to an Imag
linktitle: Aralığı Görüntüye Dönüştür
type: docs
url: /tr/convert-range-to-image/
keywords: Aspose.Cells Cloud Web API, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Format
description: Yerel bir elektronik tablo/Excel dosyasındaki bir aralık verisini bir görüntü dosyasına dönüştürün
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, Görüntü Dönüştürme, PNG, SVG, TIFF, JSON, Markdown
---
Yerel bir elektronik tablo/Excel dosyasındaki bir aralık verisini bir görüntü dosyasına dönüştürün. Desteklenir**GÖRÜNTÜ FORMATLARI:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Aralığı Görüntüye Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|Dönüştürme için elektronik tablo dosyasını yükleyin.|
|çalışma sayfası|Sicim|Sorgu|Spreadsheet/Excel çalışma sayfasının adı|
|menzil|Sicim|Sorgu|Dönüştürülecek hücre alanını tanımlayın (örneğin, A1:C10).|
|biçim|Sicim|Sorgu|Çıktı dosya biçimini belirtin (örneğin, png, svg, tiff).|
|Başlıkları yazdır|Boolean|Sorgu|Satır ve sütun başlıklarının yazdırılıp yazdırılmayacağını belirtin.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu; varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyasının depolama adı.|
|yazı tipleriKonum|Sicim|Sorgu|Dönüştürme için kullanılacak özel yazı tipleri.|
|yeniden gitmek|Sicim|Sorgu|E-tablo bölge ayarını tanımlayın.|
|şifre|Sicim|Sorgu|Korumalıysa elektronik tablo dosyasını açmak için şifre.|

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

## Neden Görüntüye Dönüştürme Aralığını API kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API Görüntüsüne Dönüştürme Aralığı Nasıl Kullanılır?

### Aralığı Görüntüye Dönüştürme API Spesifikasyonu

 The[Aralığı Görüntüye Dönüştürme API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToImage) web tarayıcınızdan doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir aralık verisini kısa kodla bir görüntüye dönüştürmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}

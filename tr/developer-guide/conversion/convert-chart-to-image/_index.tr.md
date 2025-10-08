---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Grafiğini Görüntüye Dönüştürme
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: Grafiği Görüntüye Dönüştür
type: docs
url: /tr/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: Aspose.Cells Cloud Web API ile yerel bir elektronik tablo/Excel dosyasındaki bir grafiği bir görüntü dosyasına dönüştürün
weight: 100
kwords: Excel grafiğini görüntüye, png'ye, svg'ye, tiff'e, jpg'ye, bmp'ye, Spreadshee'ye dönüştürün
---
Bir grafiği yerel bir elektronik tablo/Excel dosyasından bir görüntü biçimi dosyasına dönüştürün. Desteklenir**GÖRÜNTÜ FORMATLARI:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Tabloyu Resme Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|Tabloyu içeren elektronik tablo dosyasını yükleyin.|
|çalışma sayfası|Sicim|Sorgu|Uygunsa çalışma sayfasının adını belirtin.|
|grafikIndeksi|Tam sayı|Sorgu|Dönüştürülecek grafiğin indeksi.|
|biçim|Sicim|Sorgu|(Gerekli) İstenilen resim türü (örneğin, svg, png, jpg).|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu; varsayılan olarak null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyasının depolama alanı adı.|
|yazı tipleriKonum|Sicim|Sorgu|Gerekirse özel yazı tiplerini belirtin.|
|bölge|Sicim|Sorgu|E-tablo bölgesini ayarlayın.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için şifre.|

## **Cevap**

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

## API Görsele Dönüştürme Tablosunu nerede kullanmalısınız?

- Tabloları elektronik tabloda resim olarak dışa aktarın.

## Neden API Görseline Dönüştürme Tablosunu kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API Görseline Dönüştürme Tablosu Nasıl Kullanılır?

### Tabloyu Görüntüye Dönüştürme API Teknik Özellikleri

 The[Tabloyu Görüntüye Dönüştürme API Teknik Özellikleri](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, kısa kodla bir grafiği görüntüye dönüştürmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}

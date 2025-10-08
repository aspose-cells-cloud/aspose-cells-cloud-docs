---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Çalışma Sayfasını Görüntüye Dönüştürme
second_title: Documen
ArticleTitle: Convert a Spreadsheet Worksheet to an Imag
linktitle: Çalışma Sayfasını Imag'a Dönüştür
type: docs
url: /tr/convert-worksheet-to-image/
keywords: Aspose.Cells Cloud Web API, Convert Worksheet to Image, Cloud Conversion, Image Format Conversion, Excel to Image, RES
description: Aspose.Cells API kullanarak yerel bir sürücüdeki bir elektronik tablo çalışma sayfasını çeşitli görüntü biçimlerine verimli bir şekilde dönüştürün
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, Görüntü Dönüştürme, SVG, PNG, TIFF, Bulut Hizmetleri, Yerelden Buluta Dönüştürme, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir
---
Yerel bir elektronik tabloyu/Excel çalışma sayfasını görüntüye dönüştürün.

## **Çalışma Sayfasını Görüntüye Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| Elektronik tablo| Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| çalışma sayfası| Sicim| Sorgu| Elektronik tabloda çalışma sayfasının adı.|
| biçim| Sicim| Sorgu| İstenilen resim formatı: svg, png, tiff, vb.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyasının depolama adı.|
| yazı tipleriKonum| Sicim| Sorgu| Özel yazı tipleri kullanın.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

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

 The[Tabloyu Görüntüye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToImage) herkesin erişebileceği bir programlama arayüzü tanımlar ve doğrudan bir web tarayıcısından REST etkileşimlerine olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablonun verilerini kısa kodla bir görüntüye dönüştürmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{< /tab >}}
{{< /tabs >}}

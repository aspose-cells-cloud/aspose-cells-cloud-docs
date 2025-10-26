---
title: Aspose.Cells Cloud Web API - Elektronik Tablo Aralığını HTML'ye Dönüştürme
second_title: Documen
ArticleTitle: Converting Spreadsheet Range to Htm
linktitle: Aralığı HTM'ye Dönüştür
type: docs
url: /tr/convert-range-to-html/
keywords: Convert a spreadsheet range data to a html file, Spreadsheet Conversion, Excel Conversio
description: Yerel bir elektronik tablo/Excel dosyasındaki bir aralığı Aspose.Cells Cloud Web API ile bir HTML dosyasına dönüştürün
weight: 100
kwords: Aralığı HTML, E-Tablo ve Excel'e dönüştürün
---
Yerel bir elektronik tablo/Excel dosyasındaki bir aralık verisini html dosyasına dönüştürün.

## **Aralığı HTML'ye Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/html
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|------------|--|------------------------|-------------------------------------------------|
| Elektronik tablo|Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| çalışma sayfası| Sicim| Sorgu| Elektronik tablodaki çalışma sayfasının adı.|
| menzil| Sicim| Sorgu| Dönüştürülecek hücre alanı, örneğin A1:C10.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
| outStorageName| Sicim| Sorgu| Çıktı dosyasının depolama adı.|
| yazı tipleriKonum| Sicim| Sorgu| Kullanılacak özel yazı tiplerini belirtin.|
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

## Neden Convert Range to Html API'i kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla HTML'e Dönüştürme Aralığı API Nasıl Kullanılır?

### Aralığı HTML'ye Dönüştürme API Spesifikasyonu

 The[Aralığı HTML'ye Dönüştürme API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToHtml) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenizi sağlayan, herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak bir aralık verisini kısa kodlu bir HTML dosyasına dönüştürmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen ziyaret edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının kapsamlı listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}

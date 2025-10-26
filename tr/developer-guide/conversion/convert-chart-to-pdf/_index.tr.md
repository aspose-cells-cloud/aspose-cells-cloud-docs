---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Grafiğini PDF Dosyasına Dönüştürme
second_title: Documen
ArticleTitle: Converting a Spreadsheet Chart to a Pdf file
linktitle: Grafiği PD'ye Dönüştür
type: docs
url: /tr/convert-chart-to-pdf/
keywords: convert an Excel chart to pdf, convert spreadsheet to pdf, Aspose Cloud Web  API, cloud conversion, Excel to PD
description: Bu API, yerel bir sürücüde bulunan elektronik tablolardaki grafikleri PDF dosyasına sorunsuz bir şekilde dönüştürür
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo Dönüştürme, PDF, CSV, JSON, Markdown, Grafiği PDF'e Dönüştürme, Bulut Dönüştürme
---
 Bir grafiği yerel bir elektronik tablo/Excel dosyasından bir tabloya dönüştürün[PDF](https://docs.fileformat.com/pdf/) dosya.

## **Tabloyu PDF'e Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|-------------- ||--------------------- |--------------------------------------------------- |
| Elektronik tablo|Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| çalışma sayfası| Sicim| Sorgu| Tabloyu içeren çalışma sayfasının adı.|
| grafikIndeksi|Tam sayı| Sorgu| Dönüştürülecek grafiğin indeksi.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Dönüştürülen dosyanın saklandığı klasör yolu. Varsayılan değer null'dır.|
| outStorageName| Sicim| Sorgu| Çıktı dosyası depolama adı.|
| yazı tipleriKonum| Sicim| Sorgu| Gerekirse özel yazı tipleri kullanın.|
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

## API Pdf'e Dönüştürme Tablosunu Nerede Kullanmalısınız?

- Tablodaki grafikleri Pdf olarak dışarı aktarın.

## Neden API PDF'e Dönüştürme Tablosunu kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla PDF'e Dönüştürme Tablosu API Nasıl Kullanılır?

### Tabloyu PDF'e Dönüştür API Şartnamesi

 The[Tabloyu PDF'e Dönüştür API Şartnamesi](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

## Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak bir grafiği kısa kodla bir PDF dosyasına dönüştürmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}

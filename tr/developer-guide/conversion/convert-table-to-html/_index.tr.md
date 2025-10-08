---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Tablosu Verisini Html Dosyasına Dönüştürme
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Html fil
linktitle: Tabloyu HTM'ye Dönüştür
type: docs
url: /tr/convert-table-to-html/
keywords: Excel Table to HTML, Spreadsheet Conversion, Aspose.Cells Cloud Web API, REST, Convert Excel to HTML, Table to HTML, Document Conversion, Cloud Service
description: Bulut tabanlı API'imizi kullanarak yerel elektronik tablo dosyalarındaki tabloları kolayca HTML biçimine dönüştürün
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, HTML, PDF, CSV, JSON, Markdown, Excel'de boş hücreleri eşleştir
---
Yerel bir elektronik tablo/Excel tablosundaki verileri html dosyasına dönüştürün.

## **Tabloyu HTML'ye Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
| Elektronik tablo| Dosya| FormVerileri| Dönüştürülecek elektronik tablo dosyasını yükleyin.|
| çalışma sayfası| Sicim| Sorgu| Spreadsheet/Excel çalışma sayfasının adı|
| tabloAdı| Sicim| Sorgu| Dönüştürülecek tablonun adı.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Dönüştürülen dosyanın saklanacağı klasör yolu. Varsayılan değer null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyası için belirlenmiş depolama adı.|
| yazı tipleriKonum| Sicim| Sorgu| Dönüştürme için özel yazı tiplerini belirtin.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarlarını tanımlayın.|
| şifre| Sicim| Sorgu| E-tablo dosyasına erişmek için gereken şifre.|

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

## Neden Convert Table to Html API kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Convert Table to Html API Nasıl Kullanılır?

### Tabloyu HTML'ye Dönüştürme API Spesifikasyonu

 The[Tabloyu HTML'ye Dönüştürme API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToHtml) web tarayıcınızdan doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan, herkese açık bir programlama arayüzü sunar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablodaki verileri kısa kodlu bir HTML dosyasına dönüştürmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}

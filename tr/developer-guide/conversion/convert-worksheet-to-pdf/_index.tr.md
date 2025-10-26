---
title: Aspose.Cells Cloud Web API - Elektronik Tablo Çalışma Sayfasını Pd'ye Dönüştür
second_title: Documen
ArticleTitle: Convert Spreadsheet Worksheet to Pd
linktitle: Çalışma Sayfasını Pd'ye Dönüştür
type: docs
url: /tr/convert-worksheet-to-pdf/
keywords: worksheet to pdf, Excel PDF conversion, REST API, cloud-based conversion, spreadsheet to PD
description: Bulut tabanlı API uygulamamızı kullanarak yerel sürücünüzdeki bir elektronik tablodan bir çalışma sayfasını PDF dosyasına dönüştürün
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, çalışma sayfasını PDF'e dönüştür, bulut dönüştürme, yerel dosya dönüştürme
---
Excel Cloud Web API ile yerel bir elektronik tabloyu/Excel çalışma sayfasını pdf dosyasına dönüştürün.

## **Çalışma Sayfasını PDF'ye Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|-----------------|-|-----------------------|------------------------------------|
| Elektronik tablo| Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| çalışma sayfası|Sicim| Sorgu|Elektronik tabloda çalışma sayfasının adı.|
| çıkış yolu|Sicim| Sorgu|(İsteğe bağlı) Çalışma kitabını depolamak için klasör yolu; varsayılan değer null'dır.|
| outStorageName|Sicim| Sorgu| Çıktı dosyasının depolama adı.|
| yazı tipleriKonum|Sicim| Sorgu| Özel yazı tiplerini belirtin.|
| bölge|Sicim| Sorgu| E-tablo bölge ayarını tanımlayın.|
|şifre|Sicim| Sorgu|E-tablo dosyasını açmak için gereken şifre.|

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

## Neden Tabloyu Pdf'e Dönüştür API'i kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Convert Table to Pdf API Nasıl Kullanılır?

### Tabloyu PDF'e Dönüştür API Şartnamesi

 The[Tabloyu PDF'e Dönüştür API Şartnamesi](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToPdf) herkesin erişebileceği bir programlama arayüzü sağlar ve doğrudan bir web tarayıcısından REST etkileşimlerine olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablo tablosundaki verileri kısa kodla bir PDF dosyasına dönüştürmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}

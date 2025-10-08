---
title: Aspose.Cells Cloud Web API - Elektronik Tablo Verilerini CSV Dosyasına Dönüştürme
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Csv file
linktitle: Tabloyu CS'ye Dönüştür
type: docs
url: /tr/convert-table-to-csv/
keywords: convert table to csv, convert spreadsheet to csv, Excel to CSV conversion, cloud conversio
description: API'i kullanarak yerel sürücünüzdeki bir elektronik tablodan bir tabloyu CSV dosyasına verimli bir şekilde dönüştürür
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Tablodan CSV'ye, Yerelden Buluta Dönüştürme
---
Yerel bir elektronik tabloyu/Excel tablosunu csv dosyasına dönüştürün.

## **Tabloyu CSV'ye Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|-------------|-|------------------------|-------------------------------------------|
| Elektronik tablo| Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| çalışma sayfası|Sicim| Sorgu| Elektronik tabloda çalışma sayfasının adı.|
| tabloAdı|Sicim| Sorgu|Dönüştürülecek tablonun adı.|
| çıkış yolu|Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu; varsayılanı null'dır.|
| outStorageName|Sicim| Sorgu| Çıktı dosyasının depolama adı.|
| yazı tipleriKonum|Sicim| Sorgu| Özel yazı tiplerini kullanma yolu.|
| bölge|Sicim| Sorgu| E-tablo bölge ayarını tanımlar.|
| şifre|Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

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

## Neden Tabloyu CSV'ye Dönüştür API'i kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Convert Table to CSV API Nasıl Kullanılır?

### Tabloyu CSV'ye Dönüştür API Spesifikasyonu

 The[Tabloyu CSV'ye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToCsv) web tarayıcısından doğrudan REST etkileşimlerine izin veren, herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablo tablosundaki verileri kısa kodlu bir csv dosyasına dönüştürmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}

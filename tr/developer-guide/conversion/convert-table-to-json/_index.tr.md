---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Tablosu Verisini Json Dosyasına Dönüştürme
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Json file
linktitle: Tabloyu JSO'ya Dönüştür
type: docs
url: /tr/convert-table-to-json/
keywords: Excel API, JSON conversion, spreadsheet to JSON, cloud file conversion, REST API, Aspose.Cell
description: Excel API kullanarak yerel bir elektronik tabloyu JSON formatına verimli bir şekilde dönüştürün. Bu yöntem, bulut depolamaya ihtiyaç duymadan sorunsuz dosya işlemeyi mümkün kılar.
weight: 100
kwords: Excel API, JSON dönüştürme, bulut dosyası dönüştürme, elektronik tablo, REST API, Aspose.Cells, yerel sürücü işleme, dosya biçimi dönüştürme
---
Yerel bir elektronik tabloyu/Excel tablosunu Aspose.Cells Cloud Web API ile bir json dosyasına dönüştürün.

## **Tabloyu Json'a Dönüştür API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|-------------|-|-----------------------|----------------------------------------------|
| Elektronik tablo| Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| çalışma sayfası|Sicim| Sorgu| Elektronik tablonun çalışma sayfası adını belirtin.|
| tabloAdı|Sicim| Sorgu| Dönüştürülecek tablonun adını belirtin.|
| çıkış yolu|Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu; varsayılan olarak null'dır.|
| outStorageName|Sicim| Sorgu| Çıktı dosyasının depolama adını belirtin.|
| yazı tipleriKonum|Sicim| Sorgu| Dönüştürme için özel yazı tiplerini kullanın.|
| bölge|Sicim| Sorgu|E-tablo için bölge ayarlarını tanımlayın.|
| şifre|Sicim| Sorgu| E-tablo dosyasını açmak için gereken şifre.|

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

## Neden Convert Table to Json API'i kullanmalısınız?

- Bulut depolamaya gerek kalmaz, bulut kaynakları üzerindeki yük azalır.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Json API Tablosunu Nasıl Kullanabilirim?

### Tabloyu Json'a Dönüştürme API Spesifikasyonu

 The[Tabloyu Json'a Dönüştürme API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToJson) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablo tablosundaki verileri kısa kodla bir json dosyasına dönüştürmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}
{{< /tab >}}
{{< /tabs >}}

---
title: Aspose.Cells Cloud Web API - Bir E-Tablodaki Bozuk Bağlantıları Ara
second_title: Documen
ArticleTitle: Search Spreadsheet Broken Links in a Spreadshee
linktitle: E-Tabloda Arama Bozuk Bağlantı
type: docs
url: /tr/search-spreadsheet-broken-links/
keywords: search broken links, spreadsheet API, Excel broken links, REST API, Office Cloud integratio
description: Excel API'i kullanarak yerel elektronik tablolarda bozuk bağlantıları etkili bir şekilde arayın
weight: 100
kwords: Excel API, bozuk bağlantıları ara, Office Bulut, REST API, Elektronik tablo yönetimi, PDF, CSV, JSON, Markdown, bozuk bağlantıları belirle, köprü metnini onar
---
Yerel elektronik tablolar içindeki bozuk bağlantıları arayın.

## **E-Tabloda Kırık Bağlantıları Ara API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/broken-links
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|Analiz edilecek elektronik tablo dosyasını yükleyin.|
|çalışma sayfası|Sicim|Sorgu|Sınav için çalışma kağıdını belirtin.|
|hücreAlanı|Sicim|Sorgu|Analiz için hücre alanını tanımlayın.|
|bölge|Sicim|Sorgu|E-tablo bölgesi yapılandırmasını ayarlayın.|
|şifre|Sicim|Sorgu|E-tablo dosyasına erişim için şifreyi girin.|

### **Cevap**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## API E-Tablosu içerisinde Kırık Bağlantıları Ara özelliğini nerede kullanmalıyız?

E-tablo içerisinde kırık bağlantıları aramanız gerektiğinde API numarasını kullanabilirsiniz.

## API E-Tablosunda Kırık Bağlantıları Ara özelliğini neden kullanmalısınız?

- API ile uzaktan bir elektronik tabloda bozuk bağlantıları zahmetsizce arayın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API E-Tablosunda Bozuk Bağlantıları Arama Özelliğinin Nasıl Kullanılacağı

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, elektronik tablolardaki hücrelerdeki bozuk bağlantıları minimum kodla kolayca aramanıza olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{< /tab >}}
{{< /tabs >}}

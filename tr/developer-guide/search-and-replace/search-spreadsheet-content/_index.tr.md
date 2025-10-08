---
title: Aspose.Cells Cloud Web API - E-Tablo İçeriğini Ara
second_title: Documen
ArticleTitle: Search Spreadsheet Conten
linktitle: E-Tablo İçeriğini Ara
type: docs
url: /tr/search-spreadsheet-content/
keywords: Excel, Office Cloud, REST API, Spreadsheet Search, PDF Export, CSV Handling, JSON Formatting, Markdown Integration, Match Empty Cells in Exce
description: API numaralı telefonumuzla yerel elektronik tablo dosyalarında metni verimli bir şekilde arayın
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo Arama, PDF Dışa Aktarma, CSV İşleme, JSON Biçimlendirme, Markdown Entegrasyonu, Excel'de Cells Boşluğunu Eşleştirme
---
API'i kullanarak yerel elektronik tablo dosyalarında metin arayın.

## **E-Tablo İçeriğini Ara API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/content
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|Arama yapmak için elektronik tablo dosyasını yükleyin.|
|aramaMetni|Sicim|Sorgu|E-tabloda aranacak metin.|
|ignoringCase|Boolean|Sorgu|Aramada büyük/küçük harf ayrımının dikkate alınıp alınmayacağını belirtin.|
|çalışma sayfası|Sicim|Sorgu|İçinde arama yapılacak çalışma sayfasını belirtin.|
|hücreAlanı|Sicim|Sorgu|Aranacak hücre alanını belirtin.|
|bölge|Sicim|Sorgu|E-tablo için bölge ayarı.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için gereken şifre.|

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

## API E-Tablosu içerisinde Arama içeriğini nerede kullanmalıyız?

E-Tablo içerisinde içerik araması yapmanız gerektiğinde API numarasını kullanabilirsiniz.

## API E-Tablosu içindeki Arama içeriğini neden kullanmalısınız?

- API ile elektronik tabloda içerikleri zahmetsizce arayın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API E-Tablosunda Bozuk Bağlantıları Arama Özelliğinin Nasıl Kullanılacağı

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, hücreler için elektronik tablolarda minimum kodla içerik araması yapmanıza olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}

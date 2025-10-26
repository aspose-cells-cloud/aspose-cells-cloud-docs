---
title: Aspose.Cells Bulut Web API - Uzak Elektronik Tabloda İçerik Ara
second_title: Documen
ArticleTitle: Search Content in a Remote Spreadshee
linktitle: Uzaktan E-Tablo İçeriğini Ara
type: docs
url: /tr/search-content-in-remote-spreadsheet/
keywords: remote spreadsheet search, Excel API, search text in spreadsheet, cloud storage search, Aspose.Cells AP
description: Aspose.Cells API'i kullanarak uzak bir elektronik tabloda metni verimli bir şekilde arayın
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir, uzak elektronik tablo araması, bulut depolama araması
---
Uzak bir elektronik tabloda belirtilen metni arayın.

### **Uzaktan Elektronik Tabloda İçerik Ara API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|Aranacak çalışma kitabı dosyasının adı.|
|aramaMetni|Sicim|Sorgu|E-tabloda aranacak metin.|
|ignoringCase|Boolean|Sorgu|Aramada büyük/küçük harf ayrımının dikkate alınıp alınmayacağını belirtir.|
|dosya|Sicim|Sorgu|Çalışma kitabının saklandığı klasör yolu.|
|depolamaAdı|Sicim|Sorgu|(İsteğe bağlı) Özel bulut depolama alanının adı. Belirtilmezse varsayılan depolama alanı kullanılır.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarı.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için şifre.|

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

- API ile uzaktan bir elektronik tabloda zahmetsizce içerik arayın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'lar ile API E-Tablo aralığındaki bozuk bağlantıları arama özelliğinin nasıl kullanılacağı

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteSpreadsheet) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, hücreler için elektronik tablolarda minimum kodla içerik araması yapmanıza olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

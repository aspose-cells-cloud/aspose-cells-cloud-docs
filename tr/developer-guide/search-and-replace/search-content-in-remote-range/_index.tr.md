---
title: Aspose.Cells Bulut Web API - Uzak E-Tablolarda Arama Aralığı İçeriği
second_title: Documen
ArticleTitle: Search Range Content in Remote Spreadshee
linktitle: Uzak Aralık İçeriğini Ara
type: docs
url: /tr/search-content-in-remote-range/
keywords: Excel API, Remote Spreadsheet Search, Cloud Storage, Data Retrieval, Spreadsheet Search, Text Search AP
description: Excel API'i kullanarak bulut depolama alanında saklanan uzak bir elektronik tablonun belirtilen aralığındaki metni verimli bir şekilde arayın
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, Metin Arama, JSON, CSV, PDF, Markdown, Excel'de Boş Cells'i Eşleştir
---
Uzak bir elektronik tablonun belirli bir aralığında belirtilen metni arayın.

## **Uzak Mesafede İçerik Ara API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|E-tablo dosyasının adı.|
|çalışma sayfası|Sicim|Yol|Çalışma sayfasının adı.|
|hücreAlanı|Sicim|Yol|Aranacak hücre aralığı.|
|aramaMetni|Sicim|Sorgu|Aranacak metin.|
|ignoringCase|Boolean|Sorgu|Aramanın büyük/küçük harf duyarlılığını göz ardı edip etmeyeceğini belirtin.|
|dosya|Sicim|Sorgu|Dosyanın saklandığı klasör.|
|depolamaAdı|Sicim|Sorgu|(İsteğe bağlı) Özel bulut depolama alanı kullanılıyorsa depolama alanının adı. Belirtilmezse varsayılan depolama alanını kullanın.|
|yeniden gitmek|Sicim|Sorgu|E-tablo bölge ayarı.|
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

## API E-Tablo aralığında Arama içeriğini nerede kullanmalıyız?

E-Tablo aralığında içerik araması yapmanız gerektiğinde API numarasını kullanabilirsiniz.

## API E-Tablo aralığındaki Arama içeriğini neden kullanmalısınız?

- API ile uzak bir elektronik tablo aralığındaki içeriği zahmetsizce arayın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'lar ile API E-Tablo aralığındaki bozuk bağlantıları arama özelliğinin nasıl kullanılacağı

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteRange) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, elektronik tablolar aralığındaki hücreler için minimum kodla arama içeriği uygulamanıza olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}

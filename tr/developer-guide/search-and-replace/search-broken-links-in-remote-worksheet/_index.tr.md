---
title: Aspose.Cells Cloud Web API - Uzak Elektronik Tablodaki Çalışma Sayfasının Bozuk Bağlantılarını Ara
second_title: Documen
ArticleTitle: Search Broken Links of Worksheet in Remote Spreadshee
linktitle: Uzaktan Çalışma Sayfası Bozuk Bağlantısını Ara
type: docs
url: /tr/search-broken-links-in-remote-worksheet/
keywords: broken links, Excel API, cloud spreadsheet, REST API, hyperlink validation, remote workshee
description: Excel API'i kullanarak uzak bir elektronik tablo çalışma sayfasındaki bozuk bağlantıları zahmetsizce arayın
weight: 100
kwords: Excel API, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, bozuk bağlantılar, geçersiz URL'ler, köprü metni doğrulaması
---
Uzak bir elektronik tablo çalışma sayfasındaki bozuk bağlantıları arayın.

## **Uzaktan Çalışma Sayfasındaki Bozuk Bağlantıları Ara API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|Aranacak çalışma kitabı dosyasının adı.|
|çalışma sayfası|Sicim|Yol|Arama için çalışma sayfasını belirtin.|
|dosya|Sicim|Sorgu|Çalışma kitabının saklandığı klasör yolu.|
|depolamaAdı|Sicim|Sorgu|(İsteğe bağlı) Özel bulut depolama alanı kullanılıyorsa depolama alanının adı. Belirtilmezse varsayılan depolama alanını kullanın.|
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

## API nolu E-Tablonun çalışma sayfasında Kırık Bağlantıları Ara özelliğini nerede kullanmalıyız?

Elektronik Tablo çalışma sayfasında bozuk bağlantıları aramanız gerektiğinde API numarasını kullanabilirsiniz.

## API numaralı E-Tablonun çalışma sayfasındaki Bozuk Bağlantıları Ara özelliğini neden kullanmalısınız?

- API ile uzaktan bir elektronik tablo çalışma sayfasındaki bozuk bağlantıları zahmetsizce arayın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'lar ile API E-Tablosunun Çalışma Sayfasında Bozuk Bağlantıları Arama Özelliğinin Nasıl Kullanılacağı

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/SearchBrokenLinksInRemoteWorksheet) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, minimum kodla hücreler için çalışma sayfaları veya elektronik tablolar içinde parçalı arama yapmanızı sağlar.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

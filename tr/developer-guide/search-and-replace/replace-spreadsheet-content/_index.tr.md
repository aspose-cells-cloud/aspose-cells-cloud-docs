---
title: Aspose.Cells Cloud Web API - Elektronik Tablo İçeriğini Değiştir
second_title: Documen
ArticleTitle: Replace Spreadsheet Conten
linktitle: E-Tablo İçeriğini Değiştir
type: docs
url: /tr/replace-spreadsheet-content/
keywords: Excel API, Spreadsheet manipulation, Replace text, Office Cloud integration, REST AP
description: Aspose.Cells API'i kullanarak yerel elektronik tablo dosyalarındaki metni verimli bir şekilde değiştirin
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel'deki metni değiştir, Excel çalışma sayfasındaki boş hücreleri eşleştir
---
Yerel elektronik tablo dosyalarında belirtilen metni etkili bir şekilde değiştirin.

## **Elektronik Tablo İçeriğini Değiştir API**

```
PUT http://api.aspose.cloud/v4.0/cells/replace/content
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| Elektronik tablo| Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| aramaMetni| Sicim| Sorgu|Aranacak metin.|
| Metni değiştir| Sicim| Sorgu| Değiştirilecek metin.|
| çalışma sayfası| Sicim| Sorgu| Değiştirme için çalışma sayfasını belirtin.|
| hücreAlanı| Sicim| Sorgu| Değiştirme için hücre alanını belirtin.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

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

## API E-Tablosunda İçeriği Değiştir seçeneğini nerede kullanmalıyız?

E-tablodaki içeriği şifreyle değiştirmeniz gerektiğinde API'i kullanabilirsiniz.

## API E-Tablosundaki İçeriği Değiştir özelliğini neden kullanmalısınız?

- Elektronik tablolardaki içeriği hızla parolayla değiştirin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## API E-Tablosundaki İçeriği SDK'larla Değiştirme Nasıl Kullanılır

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceSpreadsheetContent) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, hücrelerdeki içerikleri elektronik tablolarda minimum kodla kolayca değiştirmenize olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}

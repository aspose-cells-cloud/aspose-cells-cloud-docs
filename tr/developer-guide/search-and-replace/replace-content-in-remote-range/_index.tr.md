---
title: Aspose.Cells Cloud Web API - Uzak E-Tablodaki Aralık İçeriğini Değiştir
second_title: Documen
ArticleTitle: Replace Range Content in Remote a Spreadshee
linktitle: Uzaktan Aralık İçeriğini Değiştir
type: docs
url: /tr/replace-content-in-remote-range/
keywords: API, Excel API, Replace Content, Remote Spreadsheet, Cloud Storage, Text Replacement, REST AP
description: Aspose.Cells Bulut API'i kullanarak uzak elektronik tabloların belirtilen aralıklarındaki metni verimli bir şekilde değiştirin
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir, uzak metin değiştirme, bulut depolama entegrasyonu
---
Uzak bir elektronik tablo dosyasının belirli bir aralığında belirtilen metni verimli bir şekilde değiştirin.

## **Uzak Aralıktaki İçeriği Değiştir API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
| isim| Sicim| Yol| Değiştirilecek çalışma kitabı dosyasının adı.|
| aramaMetni| Sicim| Sorgu| E-tabloda aranacak metin.|
| Metni değiştir| Sicim| Sorgu| Aranan metnin yerine konulacak metin.|
| çalışma sayfası| Sicim| Yol| Değiştirmenin gerçekleşeceği çalışma sayfasının adı.|
| hücreAlanı| Sicim| Yol| Değiştirme için belirli hücre alanı.|
| dosya| Sicim| Sorgu| Çalışma kitabının saklandığı klasör yolu.|
| depolamaAdı| Sicim| Sorgu|(İsteğe bağlı) Özel bulut depolama alanı kullanılıyorsa depolama alanının adı. Belirtilmezse varsayılan depolama alanını kullanın.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

### **Cevap**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
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

## Uzaktan Hesap Tablosu API'de Aralığın İçeriğini Değiştir seçeneğini nerede kullanmalıyız?

Uzaktaki bir elektronik tabloda Range içeriğini değiştirmeniz gerektiğinde API'i kullanabilirsiniz.

## Uzaktan Hesap Tablosu API'de Aralığın İçeriğini Değiştir seçeneğini neden kullanmalısınız?

- Uzaktaki elektronik tablolarda Range içeriğini hızla değiştirin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## Uzak E-Tablo API'de SDK'larla Aralığın İçeriğini Değiştir Nasıl Kullanılır

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteRange) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, hücrelerdeki içerikleri elektronik tablolarda minimum kodla kolayca değiştirmenize olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}

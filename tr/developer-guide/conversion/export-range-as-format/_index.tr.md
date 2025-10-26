---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Aralığı verisini Biçim dosyası olarak dışa aktarın
second_title: Documen
ArticleTitle: Export a Spreadsheet Range data as a Format file
linktitle: İhracat Aralığı Forma Olarak
type: docs
url: /tr/export-range-as-format/
keywords: Aspose.Cells Cloud Web API, Export range, Spreadsheet conversion, REST API, PDF, CSV, JSON, Markdown, Excel workshee
description: Bulut depolama alanındaki bir elektronik tablonun belirtilen aralığını dosyayı indirmeden PDF, CSV veya resim biçimleri gibi çeşitli biçimlere dönüştürün
weight: 100
kwords: E-tablo dönüştürme, REST API, PDF, CSV, JSON, Markdown, Excel çalışma sayfası
---
Bir bulut elektronik tablosunu/Excel aralığını bir biçim dosyasına aktarın. Biçim dosyası buluta kaydedilebilir veya yerel depolama alanına aktarılabilir.

## **Aralık Formatını API Olarak Dışa Aktar**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|(Gerekli) Alınacak çalışma kitabı dosyasının adı.|
|çalışma sayfası|Sicim|Yol|Çalışma sayfası adı Spreadsheet/Excel|
|menzil|Sicim|Yol|Dönüştürülecek aralık (örneğin, A1:C12).|
|biçim|Sicim|Sorgu|(Gerekli) İstenilen çıktı biçimi (örneğin, "png", "pdf", "svg").|
|dosya|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılanı null'dır.|
|depolamaAdı|Sicim|Sorgu|(İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolamanın adı. Belirtilmezse varsayılan depolamaya döner.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çıktı dosyasının klasör yolu. Varsayılanı null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyasının depolandığı yerin adı.|
|yazı tipleriKonum|Sicim|Sorgu|Özel yazı tipleri konumu.|
|bölge|Sicim|Sorgu|E-tablonun bölge ayarı.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için gereken şifre.|

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

## Neden API Formatı Olarak Export Elektronik Tablo Aralığını Kullanmalısınız?

- Bulut dosyalarınızı istediğiniz zaman, istediğiniz yerde farklı formatlara dönüştürebilirsiniz.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Format API Olarak Dışa Aktarım E-Tablo Aralığı Nasıl Kullanılır?

### API Formatı Olarak İhracat Aralığı

 The[API Formatı Olarak İhracat Aralığı](https://reference.aspose.cloud/cells/#/ConversionController/ExportRangeAsFormat) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablo aralığı verisini kısa kodlu bir biçim dosyasına aktarmanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}

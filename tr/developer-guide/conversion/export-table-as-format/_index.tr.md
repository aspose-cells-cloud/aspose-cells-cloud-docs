---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Tablosu verisini bir Biçim dosyasına aktarın
second_title: Documen
ArticleTitle: Export a Spreadsheet Table data as a Format file
linktitle: Tabloyu Belirtilen Forma Aktar
type: docs
url: /tr/export-table-as-format/
keywords: Spreadsheet Conversion, Aspose.Cells Cloud Web API, Export Table, RESTI, PDF, CSV, Excel, JSON, Markdow
description: Bulut depolama alanındaki elektronik tablolardaki tabloları çeşitli belirtilen biçimlere verimli bir şekilde dönüştürür
weight: 100
kwords: E-Tablo Dönüştürme, PDF, CSV, Excel, JSON, Markdown, Dışa Aktarma Tablosu
---
Bulut elektronik tablosunu/Excel tablosunu başka bir format dosyasına aktarın.

## **Tabloyu API Formatında Dışa Aktar**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|(Gerekli) Alınacak çalışma kitabı dosyasının adı.|
|çalışma sayfası|Sicim|Yol|Çalışma sayfasının adı.|
|tabloAdı|Sicim|Yol|Tablonun adı.|
|biçim|Sicim|Sorgu|(Gerekli) İstenilen format (örneğin, "png", "pdf", "svg").|
|dosya|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|depolamaAdı|Sicim|Sorgu|(İsteğe bağlı) Özel bulut depolama alanı kullanılıyorsa depolama alanının adı. Belirtilmezse varsayılan depolama alanını kullanın.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çıktı depolaması için klasör yolu. Varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyasının depolama adı.|
|yazı tipleriKonum|Sicim|Sorgu|Özel yazı tipleri için konum.|
|bölge|Sicim|Sorgu|E-tablo bölgesi için ayar.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için şifre.|

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

## Neden Export Spreadsheet Table Format API'i kullanmalısınız?

- Bulut dosyalarınızı istediğiniz zaman, istediğiniz yerde farklı formatlara dönüştürebilirsiniz.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Format API Olarak Export Elektronik Tablo Tablosu Nasıl Kullanılır?

### Tabloyu API Formatında Dışa Aktar

 The[Tabloyu API Formatında Dışa Aktar](https://reference.aspose.cloud/cells/#/ConversionController/ExportTableAsFormat) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, elektronik tablo verilerini kısa kodlu bir biçim dosyasına aktarmanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{< /tab >}}
{{< tab tabtabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}

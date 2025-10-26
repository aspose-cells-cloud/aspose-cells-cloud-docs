---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Çalışma Sayfasını Biçim dosyası olarak dışa aktarın
second_title: Documen
ArticleTitle: Export a Spreadsheet Worksheet as a Format fil
linktitle: Çalışma Sayfasını Dışa Aktar
type: docs
url: /tr/export-worksheet-as-format/
keywords: Export worksheet, Cloud storage conversion, File format transformation, API for spreadsheet
description: Bir çalışma sayfasını bulut depolama alanından PDF, CSV ve resimler gibi çeşitli biçimlere verimli bir şekilde dönüştürür
weight: 100
kwords: Çalışma sayfasını dışa aktar, Bulut dönüştürme, PDF, Görüntü biçimleri, Excel, REST API, CSV, JSON, Markdown, Excel'de boş hücreleri yönetme
---
Excel bulut elektronik tablosunu/Excel çalışma sayfasını Aspose.Cells Bulut Web API ile başka bir format dosyasına aktarın.

## **Çalışma Sayfasını API Formatında Dışa Aktar**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|(Gerekli) Alınacak çalışma kitabı dosyasının adı.|
|çalışma sayfası|Sicim|Yol|(Gerekli) Dönüştürülecek belirli çalışma sayfası.|
|biçim|Sicim|Sorgu|(Gerekli) İstenilen çıktı biçimi (örneğin, "png", "pdf", "svg").|
|dosya|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|depolamaAdı|Sicim|Sorgu|(İsteğe bağlı) Özel bulut depolama alanının adı. Belirtilmezse varsayılan depolama alanını kullanın.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çıktı klasörü yolu. Varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|(İsteğe bağlı) Çıktı dosyası Depolama Adı.|
|yazı tipleriKonum|Sicim|Sorgu|(İsteğe bağlı) Gerekirse özel yazı tiplerini belirtin.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarı.|
|şifre|Sicim|Sorgu|E-tablo dosyasına erişim için şifre.|

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

## Neden API Formatında Dışa Aktarım Çalışma Sayfasını kullanmalısınız?

- Bulut dosyalarınızı istediğiniz zaman, istediğiniz yerde farklı formatlara dönüştürebilirsiniz.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API Formatında Dışa Aktarım Çalışma Sayfası Nasıl Kullanılır?

### Çalışma Sayfasını API Formatı Olarak Dışa Aktar

 The[Çalışma Sayfasını API Formatı Olarak Dışa Aktar](https://reference.aspose.cloud/cells/#/ConversionController/ExportWorksheetAsFormat) REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tablo çalışma sayfasını kısa kodlu bir biçim dosyasına aktarmanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}

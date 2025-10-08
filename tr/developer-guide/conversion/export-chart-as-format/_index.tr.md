---
title: Aspose.Cells Cloud Web API - Bir Elektronik Tablo Grafiğini Biçim dosyası olarak dışa aktarın
second_title: Documen
ArticleTitle: Export a Spreadsheet Chart as a Format fil
linktitle: Grafiği Forma Olarak Dışa Aktar
type: docs
url: /tr/export-chart-as-format/
keywords: Export Chart, Aspose.Cells Cloud Web API, Spreadsheet Conversion, PDF Export, Image Export, REST, Excel, CSV, JSO
description: Bulutta saklanan elektronik tablolardaki grafikleri, indirmeye gerek kalmadan doğrudan PDF veya görüntü gibi belirtilen biçimlere verimli bir şekilde dönüştürür
weight: 100
kwords: Grafik, REST, E-Tablo Dönüştürme, PDF, CSV, JSON, Markdown, Excel, Görüntü Biçimi Dışa Aktarma
---
Excel bulut elektronik tablosunu/Aspose.Cells grafiğini API Bulut Web dosyasıyla başka bir format dosyasına aktarın.

## **Tabloyu API Formatında Dışa Aktar**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| isim| Sicim| Yol| (Gerekli) Alınacak çalışma kitabı dosyasının adı.|
| çalışma sayfası| Sicim| Yol| Çalışma sayfası adı|
| grafikIndeksi| Tam sayı| Yol| Grafik endeksi|
| biçim| Sicim| Sorgu| (Gerekli) İstenilen çıktı biçimi (örneğin, "png", "pdf", "svg").|
| dosya| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu; varsayılan olarak null'dır.|
| depolamaAdı| Sicim| Sorgu|(İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolamanın adı; atlanırsa varsayılan depolamayı kullanın.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu; varsayılan olarak null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyası depolama adı.|
| yazı tipleriKonum| Sicim| Sorgu| Özel yazı tipleri kullanın.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

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

## Neden API Formatında Export Elektronik Tablo Grafiğini kullanmalısınız?

- Bulut dosyalarınızı istediğiniz zaman, istediğiniz yerde farklı formatlara dönüştürebilirsiniz.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API Formatında Export E-Tablo Grafiğini Nasıl Kullanabilirim?

### Tabloyu API Formatında Dışa Aktarın

 The[Tabloyu API Formatında Dışa Aktarın](https://reference.aspose.cloud/cells/#/ConversionController/ExportChartAsFormat) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, elektronik tablo grafik verilerini kısa kodlu bir biçim dosyasına aktarmanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}

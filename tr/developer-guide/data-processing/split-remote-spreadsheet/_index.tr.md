---
title: Aspose.Cells Cloud Web API - Bir elektronik tabloyu, her çalışma sayfası için bir tane olmak üzere birden fazla dosyaya bölün
second_title: Documen
ArticleTitle: Split a spreadsheet into multiple files, one for each worksheet
linktitle: Bulutta Uzak Elektronik Tabloyu Bölme
type: docs
url: /tr/split-remote-spreadsheet/
keywords: spreadsheet splitting, cloud spreadsheet API, split Excel file, multi-format outpu
description: Bulut depolama alanında saklanan bir elektronik tabloyu indirmeden birden fazla çıktı biçimine bölün
weight: 100
kwords: Excel, Office Bulut, REST, Elektronik Tablo, PDF, CSV, JSON, Markdown, bölünmüş uzak elektronik tablo
---
Bulutta saklanan elektronik tabloyu 30 çıktı dosya formatına sahip ayrı dosyalara bölün.

## **Bölünmüş Uzaktan Elektronik Tablo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
| isim| Sicim| Yol| Bölünecek çalışma kitabı dosyasının adı.|
| dosya| Sicim| Sorgu| Çalışma kitabının saklandığı klasör yolu.|
| itibaren| Tam sayı| Sorgu| Çalışma sayfası dizinine başla.|
| ile| Tam sayı| Sorgu| Çalışma sayfası dizini sonu.|
| outFormat| Sicim| Sorgu| İstenilen çıktı formatı (örneğin, "Xlsx", "Pdf", "Csv").|
| depolamaAdı| Sicim| Sorgu|(İsteğe bağlı) Özel bulut depolama alanı kullanılıyorsa depolama alanının adı. Belirtilmezse varsayılan depolama alanını kullanın.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyası depolama adı.|
| yazı tipleriKonum| Sicim| Sorgu| Özel yazı tipleri kullanın.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

## **Cevap**

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

## API Split Remote Spreadsheet'i nerede kullanmalıyız?

Birden fazla veri dosyasını birleştirmeniz gerektiğinde API'i kullanabilirsiniz.

## Neden API Split Remote Spreadsheet'i kullanmalısınız?

- Bulut depolama dosyalarının indirilmesine gerek yoktur ve doğrudan bulutta bölünebilir.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## API Bölünmüş Uzaktan E-Tablosunun SDK'larla Nasıl Kullanılacağı

### Bölünmüş Uzaktan Elektronik Tablo API Spesifikasyonu

 The[Bölünmüş Uzaktan Elektronik Tablo API Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) herkesin erişebileceği bir programlama arayüzü tanımlar ve doğrudan bir web tarayıcısından REST etkileşimlerine olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bulutta saklanan elektronik tabloyu kısa kodlarla ayrı dosyalara bölmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{< /tab >}}
{{< /tabs >}}

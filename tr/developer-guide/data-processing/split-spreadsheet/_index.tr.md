---
title: Aspose.Cells Cloud WEb API - Elektronik Tabloyu ayrı dosyalara bölme
second_title: Documen
ArticleTitle: Split the Spreadsheet into separate files
linktitle: Bölünmüş E-Tablo
type: docs
url: /tr/split-spreadsheet/
keywords: Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdow
description: Bulut depolama gerektirmeden yerel bir elektronik tabloyu çeşitli formatlarda birden fazla dosyaya bölün
weight: 100
kwords: Excel API, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Yerel Elektronik Tabloyu Bölme, Bulut İşleme, Dosya Yönetimi, Hata Yönetimi
---
Bulut depolamaya ihtiyaç duymadan yerel elektronik tabloyu 30 çıktı dosya biçimiyle ayrı dosyalara bölün.

## **Bölünmüş Elektronik Tablo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| Elektronik tablo| Dosya| FormVerileri| Bölünecek elektronik tablo dosyasını yükleyin.|
| itibaren| Tam sayı| Sorgu| Başlangıç çalışma sayfası dizinini belirtin.|
| ile| Tam sayı| Sorgu| Bitiş çalışma sayfası dizinini belirtin.|
| outFormat| Sicim| Sorgu| Çıktı dosya formatını tanımlayın.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çıktı çalışma kitabını depolamak için klasör yolu. Varsayılanı null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyasının depolama adını tanımlayın.|
| yazı tipleriKonum| Sicim| Sorgu| Gerekirse özel yazı tiplerini belirtin.|
| yeniden gitmek| Sicim| Sorgu| E-tablo bölgesini ayarlayın.|
| şifre| Sicim| Sorgu| E-tablo dosyasına erişim için şifreyi girin.|

## **Cevap**

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

## API Bölünmüş Hesap Tablosunu nerede kullanmalıyız?

Bir elektronik tabloyu daha fazla dosyaya bölmeniz gerektiğinde API numarasını kullanabilirsiniz.

## Neden API Bölünmüş Hesap Tablosunu kullanmalısınız?

- Bulut depolama alanına ihtiyacınız yok, sadece doğrudan bölün.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## API Bölünmüş Elektronik Tablosunun SDK'larla Nasıl Kullanılacağı

### Bölünmüş Elektronik Tablo API Spesifikasyonu

 The[Bölünmüş Elektronik Tablo API Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, elektronik tabloyu kısa kodlarla ayrı dosyalara bölmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, farklı SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}

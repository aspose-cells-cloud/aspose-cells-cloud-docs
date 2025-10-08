---
title: Aspose.Cells Cloud Web API - CSV, JSON veya XML Verilerini Bir Elektronik Tablo Dosyasına Aktarın
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: Verileri E-Tabloya Aktar
type: docs
url: /tr/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: Aspose.Cells Cloud Web API'i kullanarak CSV, JSON ve XML gibi desteklenen formatlardan verileri bir elektronik tabloya verimli bir şekilde aktarın
weight: 100
kwords: Aspose.Cells Bulut Web API, Veri İçe Aktarma, Office Bulut, REST, Elektronik Tablo, CSV, JSON, XM
---
 Verileri bir elektronik tablo çalışma sayfasına aktarın. İçe aktarılan veri dosyasının desteklenen biçimi:[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) veya[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **Verileri Elektronik Tabloya Aktar API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| veri dosyası| Dosya| FormVerileri| İçe aktarılacak veri dosyasını yükleyin.|
| Elektronik tablo| Dosya| FormVerileri| Hedef elektronik tablo dosyasını yükleyin.|
| çalışma sayfası| Sicim| Sorgu| Verileri içe aktarmak için çalışma sayfasını belirtin.|
| başlangıç hücresi| Sicim| Sorgu|Verileri içe aktarmak için başlangıç konumunu belirtin.|
| sokmak| Boolean| Sorgu| Belirtilen içe aktarma verilerinin eklenip eklenmeyeceğini veya üzerine yazılıp yazılmayacağını belirtir.|
| SayısalVerileri dönüştür| Boolean| Sorgu| İçe aktarma sırasında sayısal verilerin dönüştürülüp dönüştürülmeyeceğini belirtin.|
| ayırıcı| Sicim| Sorgu| CSV formatı için ayırıcıyı belirtin.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyasının depolama adını belirtin.|
| yazı tipleriKonum| Sicim| Sorgu| Kullanılacak özel yazı tiplerini tanımlayın.|
| yeniden gitmek| Sicim| Sorgu| E-tablo bölgesi yapılandırmasını ayarlayın.|
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

## API E-Tablosuna Veri Aktarma işlemini nerede kullanmalıyız?

- Büyük miktarda veriyi elektronik tablo çalışma sayfasına aktarma.
-  İçe aktarılan veri dosyası biçimi[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) Ve[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## API Elektronik Tablosuna Veri Aktarma'yı neden kullanmalısınız?

- Büyük miktarda veriyi elektronik tablolara aktarma.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API E-Tablosuna Veri Aktarma Nasıl Kullanılır

### Verileri Elektronik Tabloya Aktarma API Spesifikasyonu

 The[Verileri Elektronik Tabloya Aktarma API Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) web tarayıcınızdan doğrudan REST etkileşimlerine izin veren, herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak verileri kısa kodlarla bir elektronik tablo çalışma sayfasına aktarmanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

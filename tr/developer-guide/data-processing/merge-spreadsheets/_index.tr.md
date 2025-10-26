---
title: Aspose.Cells Cloud Web API - Birden fazla elektronik tabloyu tek bir elektronik tabloda birleştirin
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: Elektronik Tabloyu Birleştir
type: docs
url: /tr/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: Excel API'i kullanarak yerel elektronik tablo dosyalarını çeşitli biçimlere (XLSX, CSV, PDF) kolayca birleştirin
weight: 100
kwords: Excel API, Elektronik tabloları birleştirme, Office Bulut, REST API, Elektronik tablo birleştirme, CSV biçimi, JSON, Markdow
---
30'dan fazla dosya biçiminde çıktı desteğiyle birden fazla yerel elektronik tablo dosyasını tek bir dosyada birleştirin.

## **Elektronik Tabloyu Birleştir API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
| Elektronik tablo| Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| outFormat| Sicim| Sorgu| Çıktı dosya biçimini belirtin.|
| BirSayfadaBirleştir| Boolean| Sorgu| Tüm verilerin tek bir çalışma sayfasında birleştirilip birleştirilmeyeceğini belirtin.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çıktı çalışma kitabının klasör yolu. Varsayılanı null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyasının depolama adını belirtin.|
| yazı tipleriKonum| Sicim| Sorgu| Kullanılacak özel yazı tiplerini tanımlayın.|
| bölge| Sicim| Sorgu| E-tablo bölgesini ayarlayın.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifreyi girin.|

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

## Merge Local Spreadsheet API'i nerede kullanmalıyız?

Birden fazla veri dosyasını birleştirmeniz gerektiğinde API'i kullanabilirsiniz.

## Neden Merge Local Spreadsheet API'i kullanmalısınız?

- Bulut depolama alanına ihtiyacınız yok, sadece doğrudan birleştirin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## API Yerel E-Tablo Birleştirme SDK'larıyla Nasıl Kullanılır

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)kullanıcıların doğrudan bir web tarayıcısından REST etkileşimleri gerçekleştirmesine olanak tanıyan, herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, birden fazla elektronik tabloyu kısa kodla tek bir elektronik tabloda birleştirmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}

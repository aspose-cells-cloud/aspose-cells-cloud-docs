---
title: Aspose.Cells Cloud Web API - E-Tablolardaki Boş Çalışma Sayfalarını Sil
second_title: Documen
ArticleTitle: Delete Blank Worksheets in a Spreadshee
linktitle: Boş Çalışma Sayfasını Sil
type: docs
url: /tr/delete-spreadsheet-blank-worksheets/
keywords: Aspose.Cells Cloud Web API, Delete Blank Worksheets, Spreadsheet Managemen
description: Herhangi bir veri veya nesne içermeyen tüm boş çalışma sayfalarını elektronik tablodan etkili bir şekilde silin. Çalışma kitabınızı daha iyi performans için optimize edin.
weight: 100
kwords: Excel, Office Bulut, REST, Elektronik Tablo, PDF, CSV, JSON, Markdown
---
Excel elektronik tablosundan herhangi bir veri veya başka nesne içermeyen tüm boş çalışma sayfalarını silin.

## **DeleteSpreadsheetBlankWorksheets API**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-worksheets
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
| Elektronik tablo| Dosya| FormVerileri| Temizlenecek elektronik tablo dosyasını yükleyin.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyası Depolama Adı.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

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

## Delete Spreadsheet Blank Worksheets API kodunu nerede kullanmalıyız?

Verilerinizi dönüştürmeniz gerektiğinde API'i kullanabilirsiniz.

## Delete Spreadsheet Blank Worksheets API'i neden kullanmalısınız?

- Excel elektronik tablosundan herhangi bir veri veya başka nesne içermeyen tüm boş çalışma sayfalarını hızlıca silin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Delete Spreadsheet Blank Worksheets API Nasıl Kullanılır

### Boş Çalışma Sayfalarını Sil API Teknik Özellikleri

 The[Boş Çalışma Sayfalarını Sil API Teknik Özellikleri](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankWorksheets) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, kısa kodla boş çalışma sayfalarını silmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankWorksheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankWorksheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankWorksheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankWorksheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankWorksheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankWorksheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankWorksheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankWorksheets.go" >}}
{{< /tab >}}
{{< /tabs >}}

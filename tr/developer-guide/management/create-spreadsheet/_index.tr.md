---
title: Aspose.Cells Cloud Web API - Bir elektronik tablo şablonuyla yeni bir Elektronik Tablo oluşturun
second_title: Documen
ArticleTitle: Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc
linktitle: E-Tablo Oluştur
type: docs
url: /tr/create-spreadsheet/
keywords: Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancemen
description: Excel API, kullanıcıların belirtilen bir adla yeni bir elektronik tablo oluşturmasına olanak tanır, önceden tanımlanmış içerik veya biçimlendirme için isteğe bağlı şablonları destekler ve kullanıcı üretkenliğini artırır
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir, Elektronik Tablo Oluşturma, Şablon Desteği, Üretkenlik Artışları
---
Belirtilen şablona göre oluşturulmuş, boş veya kullanılabilir bir elektronik tablo olabilen yeni bir elektronik tablo oluşturun.

## **Elektronik Tablo Oluştur API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|---------- ||----------------------- |----- |
|biçim| Sicim| Sorgu| Yeni elektronik tablonun adını belirtir. Bu ad, elektronik tabloyu sistemde tanımlamak için kullanılacaktır.|
| şablon| Sicim| Sorgu| İsteğe bağlı. Sağlanırsa, yeni elektronik tablo belirtilen şablona göre oluşturulur. Bu, önceden tanımlanmış düzenleri ve stilleri uygulamak için faydalı olabilir.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
| outStorageName| Sicim| Sorgu| Çıktı dosyası Depolama Adı.|
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

## Create Spreadsheet API'i nerede kullanmalıyız?

Yeni bir elektronik tabloya ihtiyacınız olduğunda API'i kullanabilirsiniz.

## Neden Create Spreadsheet API'i kullanmalısınız?

- Sadece boş bir elektronik tablo oluşturamazsınız, aynı zamanda bir şablona dayalı belirli bir elektronik tablo da oluşturabilirsiniz.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Create Spreadsheet API Nasıl Kullanılır

### API Elektronik Tablosu Oluşturma Spesifikasyonu

 The[API Elektronik Tablosu Oluşturma Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) herkesin erişebileceği bir programlama arayüzü tanımlar ve doğrudan bir web tarayıcısından REST etkileşimlerine olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, elektronik tabloyu kısa kodla oluşturmanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

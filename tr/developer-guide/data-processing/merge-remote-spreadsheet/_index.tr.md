---
title: Aspose.Cells Cloud Web API - Bir elektronik tabloyu diğerine birleştirin.
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: Uzak Elektronik Tabloyu Birleştir
type: docs
url: /tr/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: Bulut depolama alanında saklanan bir elektronik tablo dosyasını başka bir elektronik tabloyla birleştirebilir ve veri çıktısının biçimini ve konumunu belirleyebilirsiniz.
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, boş hücreleri birleştirme, bulut işleme
---
Bulut depolama alanında saklanan bir elektronik tablo dosyasını başka bir elektronik tabloyla birleştirebilir ve veri çıktısının biçimini ve konumunu belirleyebilirsiniz.

## **Uzaktan Elektronik Tabloyu Birleştir API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|Birleştirilecek çalışma kitabı dosyasının adı.|
|birleştirilmişE-Tablo|Sicim|Sorgu|Birleştirilecek elektronik tablo dosyalarının listesi.|
|dosya|Sicim|Sorgu|Çalışma kitabının saklandığı klasör yolu.|
|outFormat|Sicim|Sorgu|Çıktı dosya biçimi (örneğin, XLSX, PDF).|
|BirSayfadaBirleştir|Boolean|Sorgu|Tüm verilerin tek bir çalışma sayfasında birleştirilmesi isteniyor mu?|
|depolamaAdı|Sicim|Sorgu|(İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolamanın adı. Belirtilmezse varsayılan depolamaya döner.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Birleştirilen çalışma kitabının klasör yolu. Varsayılanı null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyasının depolanacağı yerin adı.|
|yazı tipleriKonum|Sicim|Sorgu|Özel yazı tipi konumu.|
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

## Merge Remote Spreadsheet API'i nerede kullanmalıyız?

- Bulut depolamada birden fazla veri dosyasını birleştirmeniz gerektiğinde.


## Neden Merge Remote Spreadsheet API'i kullanmalısınız?

- Bulut depolama dosyalarının indirilmesine gerek yoktur ve doğrudan bulutta birleştirilebilirler.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## API Uzaktan E-Tablo Birleştirme SDK'larıyla Nasıl Kullanılır

### Uzak Elektronik Tablo Birleştirme API Spesifikasyonu

 The[Uzak Elektronik Tablo Birleştirme API Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) REST etkileşimlerini doğrudan bir web tarayıcısından yürütmek için herkese açık bir programlama arayüzü sağlar.

## Excel API SDK

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tabloyu kısa kodla başka bir elektronik tabloya birleştirmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

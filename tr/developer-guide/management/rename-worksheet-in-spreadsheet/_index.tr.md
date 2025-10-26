---
title: Aspose.Cells Cloud Web API - E-Tabloda Çalışma Sayfasını Yeniden Adlandır
second_title: Documen
ArticleTitle: Rename worksheet in Spreadshee
linktitle: Spreadshee'de Çalışma Sayfasını Yeniden Adlandır
type: docs
url: /tr/rename-worksheet-in-spreadsheet/
keywords: Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet Organizatio
description: Web API uç noktası, kullanıcıların bir çalışma kitabındaki belirli bir çalışma sayfasını yeniden adlandırmasına olanak tanır, böylece organizasyon ve okunabilirlik artar
weight: 100
kwords: Excel API, Çalışma Sayfasını Yeniden Adlandır, Çalışma Kitabı Yönetimi, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir
---
Bir elektronik tabloda çalışma sayfasının adını değiştirin.

## **API E-Tablosundaki çalışma sayfasının adını değiştirin**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|E-tablo dosyasını yükleyin.|
|kaynakAdı|Sicim|Sorgu|Yeniden adlandırılacak çalışma sayfasının mevcut adı.|
|hedefAdı|Sicim|Sorgu|Çalışma kağıdının yeni adı.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılanı null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyası Depolama Adı.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarı.|
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

## API E-Tablosunda Yeniden Adlandır Çalışma Sayfasını Nerede Kullanmalıyız?

Elektronik tablolarda çalışma sayfasının adını değiştirmeniz gerektiğinde API kodunu kullanabilirsiniz.

## API E-Tablosunda Neden Yeniden Adlandır Çalışma Sayfasını Kullanmalısınız?

- Çalışma sayfalarını elektronik tablolardan hızla yeniden adlandırın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API Sayılı E-Tabloda Yeniden Adlandırma Çalışma Sayfasının Nasıl Kullanılacağı

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet)web tarayıcısından doğrudan REST etkileşimlerine izin veren, herkesin erişebileceği bir programlama arayüzünün ayrıntılarını sunar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, elektronik tablolarda hücreler için çalışma sayfası adını yeniden adlandırma işlemini minimum kodla kolayca gerçekleştirmenize olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

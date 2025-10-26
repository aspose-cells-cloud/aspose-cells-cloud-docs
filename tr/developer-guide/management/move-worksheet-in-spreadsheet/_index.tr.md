---
title: Aspose.Cells Cloud Web API - Çalışma Sayfasını Elektronik Tabloda yeni bir konuma taşıyın
second_title: Documen
ArticleTitle: Move worksheet to new position in Spreadshee
linktitle: Çalışma Sayfasını Elektronik Tabloda Taşıma
type: docs
url: /tr/move-worksheet-in-spreadsheet/
keywords: Move Worksheet, Aspose.Cells Cloud Web API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Excel AP
description: MoveWorksheet API, kullanıcıların bir çalışma kitabında belirtilen bir çalışma sayfasını verimli bir şekilde yeniden konumlandırmasını sağlayarak elektronik tablo verilerinin organizasyonunu ve erişilebilirliğini artırır
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, Çalışma Sayfasını Taşıma, Çalışma Kitabı Düzenleme, PDF, CSV, JSON, Markdown
---
Bir çalışma sayfasını elektronik tabloda yeni bir konuma taşıyın.

## **Çalışma sayfasını API numaralı elektronik tablodan taşı**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|E-tablo dosyasını yükleyin.|
|çalışma sayfası|Sicim|Sorgu|Taşınacak çalışma sayfasının geçerli adı.|
|konum|Tam sayı|Sorgu|Çalışma sayfasının yeni konumu.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyası depolama adı.|
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

## API E-Tablosunda Taşıma Çalışma Sayfasını Nerede Kullanmalıyız?

Elektronik tablolarda bir çalışma sayfasını yeni bir konuma taşımanız gerektiğinde API numarasını kullanabilirsiniz.

## API Sayılı E-Tabloda Taşıma Çalışma Sayfasını Neden Kullanmalısınız?

- Çalışma sayfalarını elektronik tablolardan hızla taşıyın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API E-Tablosunda Taşıma Çalışma Sayfasının Nasıl Kullanılacağı

### Çalışma Sayfasını Elektronik Tabloda Taşıma API Spesifikasyonu

 The[Çalışma Sayfasını Elektronik Tabloda Taşıma API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) Bir web tarayıcısından doğrudan REST etkileşimlerini kolaylaştırmak için herkese açık bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, çalışma sayfasını kısa kodla elektronik tabloda taşımanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

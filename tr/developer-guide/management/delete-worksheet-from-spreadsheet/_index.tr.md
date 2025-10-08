---
title: Aspose.Cells Cloud Web API - Elektronik Tablodan Bir Çalışma Sayfasını Sil
second_title: Documen
ArticleTitle: Delete a worksheet from the Spreadshee
linktitle: Çalışma Sayfasını Elektronik Tablodan Sil
type: docs
url: /tr/delete-worksheet-from-spreadsheet/
keywords: delete worksheet, spreadsheet management, Aspose.Cells Cloud Web API, REST API, workbook structure, remove worksheet
description: Bu API uç noktası, kullanıcıların belirtilen bir çalışma sayfasını bir çalışma kitabından silmesine olanak tanır ve gereksiz veya tekrarlayan çalışma sayfalarını ortadan kaldırarak çalışma kitabı yapılarının yönetimini basitleştirir
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel Çalışma Sayfalarını Yönet, Gereksiz Çalışma Sayfalarını Sil
---
Bir çalışma sayfasını elektronik tablodan silin.

## **API numaralı elektronik tablodan çalışma sayfasını sil**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:-               |:-     |:-                         |:-           |
| Elektronik tablo|Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| sayfaAdı| Sicim| Sorgu| Silinecek çalışma sayfasının adını veya tanımlayıcısını belirtir. Bu parametre gereklidir ve çalışma kitabındaki mevcut bir çalışma sayfasının adıyla eşleşmelidir.|
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

## API E-Tablosundan Sil çalışma sayfasını nerede kullanmalıyız?

Elektronik tablolardan bir çalışma sayfasını silmeniz gerektiğinde API numarasını kullanabilirsiniz.

## API numaralı E-Tablodan Çalışma Sayfasını Sil'i neden kullanmalısınız?

- Çalışma sayfalarını elektronik tablolardan hızlıca kaldırın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API E-Tablosundan Sil Çalışma Sayfası Nasıl Kullanılır

### API Elektronik Tablosu'ndan çalışma sayfasını sil

 The[API Elektronik Tablosu'ndan çalışma sayfasını sil](https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, kısa kodla çalışma sayfasını elektronik tablodan silmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

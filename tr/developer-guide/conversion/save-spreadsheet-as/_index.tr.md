---
title: Aspose.Cells Cloud Web API - Elektronik Tabloyu biçim dosyası olarak kaydet
second_title: Documen
ArticleTitle: Save Spreadsheet as a Format fil
linktitle: Elektronik Tabloyu Kaydet
type: docs
url: /tr/save-spreadsheet-as/
keywords: spreadsheet conversion, Save as, Excel to PDF, Excel to CSV, RES
description: Sağlam API'imizi kullanarak bulutta depolanan elektronik tabloları XLSX, PDF ve CSV dahil olmak üzere çeşitli biçimlere zahmetsizce dönüştürün
weight: 100
kwords: Excel API, Office Bulut, REST, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel dosyalarını dönüştür, elektronik tabloyu farklı kaydet, Aspose.Cells Bulut Web AP
---
Bulut elektronik tablosu/Excel dosyasını bulut depolama alanına biçim dosyası olarak kaydedin.

## **E-Tabloyu API olarak kaydet**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
| isim| Sicim| Yol| (Gerekli) Dönüştürülecek çalışma kitabı dosyasının adı.|
| biçim| Sicim| Sorgu| (Gerekli) İstenilen çıktı formatı (örneğin, "Xlsx", "Pdf", "Csv").|
| saveOptionsData| Sınıf| Vücut| (İsteğe bağlı) Seçenek verilerini kaydedin. Varsayılan değer null'dır.|
| dosya| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
| depolamaAdı| Sicim| Sorgu|(İsteğe bağlı) Özel bulut depolama alanı kullanılıyorsa depolama alanının adı. Belirtilmezse varsayılan depolama alanını kullanın.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyası Depolama Adı.|
| yazı tipleriKonum| Sicim| Sorgu| Özel yazı tiplerini kullanın.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

### **Cevap**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## API Save Spread'i neden kullanmalısınız?

- Bulut dosyalarınızı istediğiniz zaman, istediğiniz yerde farklı formatlara dönüştürebilirsiniz.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Json API Tablosunu Nasıl Kullanabilirim?

### E-Tabloyu API Şartnamesi Olarak Kaydet

 The[E-Tabloyu API Şartnamesi Olarak Kaydet](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, bir elektronik tabloyu kısa kodlu bir biçim dosyası olarak kaydetmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{< /tab >}}
{{< /tabs >}}

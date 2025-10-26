---
title: Aspose.Cells Cloud Web API - Eşleşen elektronik tablo dosyalarını uzak bir Klasördeki bir dosyaya birleştirme
second_title: Documen
ArticleTitle: Merge matching spreadsheet files into a file in a remote Folder
linktitle: Uzak Klasördeki Elektronik Tabloları Birleştirme
type: docs
url: /tr/merge-spreadsheets-in-remote-folder/
keywords: Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST AP
description: Bulut depolama alanında saklanan elektronik tablo dosyalarını tek bir dosyada birleştirin ve dosya biçimi, PDF, CSV, Json ve diğer yaygın biçimler gibi çıktı için 30 biçimi destekler
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Elektronik Tabloları Birleştir, Bulut İşleme, Uzaktan Dosya İşleme
---
Eşleşen elektronik tablo dosyalarını uzak klasördeki dosyalarla birleştirin, çıktı dosya biçimi PDF, Csv, Json ve diğer yaygın biçimler gibi 30'dan fazla biçimi destekler.


## **Uzak Klasördeki Elektronik Tabloları Birleştirme API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| dosya| Sicim| Sorgu|Birleştirilen dosyaların saklanacağı klasör.|
| dosyaEşleşmeİfadesi| Sicim| Sorgu| Birleştirilecek dosyaları eşleştirmek için ifade.|
| outFormat| Sicim| Sorgu| İstenilen çıktı dosya biçimi.|
| BirSayfadaBirleştir| Boolean| Sorgu| Tüm verilerin tek bir çalışma sayfasında birleştirilip birleştirilmeyeceğini belirtir.|
| depolamaAdı| Sicim| Sorgu| (İsteğe bağlı) Özel bulut depolama alanının adı; atlanırsa varsayılan depolama alanı kullanılır.|
| çıkış yolu| Sicim| Sorgu| (İsteğe bağlı) Çalışma kitabını depolamak için klasör yolu; varsayılan olarak null'dır.|
|outStorageName| Sicim| Sorgu| Çıktı dosyasının depolanacağı yerin adı.|
| yazı tipleriKonum| Sicim| Sorgu| Özel yazı tiplerini belirtir.|
| bölge| Sicim| Sorgu| E-tablo bölgesini ayarlar.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

## **Cevap**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## Uzak klasör API'de Birleştirme Tablosunu nerede kullanmalıyız?

Birden fazla veri dosyasını birleştirmeniz gerektiğinde API'i kullanabilirsiniz.

## Uzak klasör API'de Birleştirme Elektronik Tablosunu neden kullanmalısınız?

- Bulut depolama dosyalarının indirilmesine gerek yoktur ve doğrudan bulutta birleştirilebilirler.
- Birden fazla elektronik tablo dosyasını toplu olarak birleştirin, Eşleşen ifadeleri destekleyin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## Uzak klasör API'de SDK'larla Birleştirme Elektronik Tablosunun Nasıl Kullanılacağı

### Uzak klasördeki elektronik tabloyu birleştirme API Teknik Özellikleri

 The[Uzak klasördeki elektronik tabloyu birleştirme API Teknik Özellikleri](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) web tarayıcısından doğrudan REST etkileşimlerine izin veren, herkesin erişebileceği bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak eşleşen elektronik tablo dosyalarını kısa kodla uzak klasördeki dosyalarla birleştirmenize olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}

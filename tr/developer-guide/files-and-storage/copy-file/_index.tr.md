---
title: Dosyayı Kopyala - Excel AP
second_title: Documen
linktitle: Kopyala Dosyası
type: docs
url: /tr/copy-file/
keywords: Excel API, Office Cloud, REST API, Spreadsheet Copy, PDF Conversion, CSV Export, JSON Handling, Markdown Support, Copy Excel File, Match Blank Cell
description: Excel için CopyFile API'in elektronik tabloları verimli bir şekilde çoğaltmak ve çeşitli dosya biçimlerini işlemek için nasıl kullanılacağını öğrenin
weight: 100
kwords: Excel API, Office Bulut, REST API, Elektronik Tablo Kopyalama, PDF Dönüştürme, CSV Dışa Aktarma, JSON İşleme, Markdown Desteği, Excel Dosyasını Kopyalama, Boş Hücreyi Eşleştirme
---
## **Excel API: Dosyayı Kopyala**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **İşlev Açıklaması**

 The**copyFile** API, kullanıcıların Excel dosyasını belirtilen bir kaynak yolundan bir hedef yoluna kopyalamasına olanak tanır ve çeşitli depolama seçeneklerini destekler.

###  İstek parametreleri**copyFile** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|-------------- ||--------------------- |-------------------------------------- |
| srcPath| Sicim| Yol| Kopyalanacak dosyanın kaynak yolu.|
| hedefYolu| Sicim| Sorgu| Dosyanın kaydedileceği hedef yol.|
| srcDepolamaAdı| Sicim| Sorgu| Kaynak depolamanın adı.|
| hedefDepolamaAdı| Sicim| Sorgu| Hedef depolama alanının adı.|
| sürüm kimliği| Sicim| Sorgu| Kopyalanacak dosyanın isteğe bağlı sürüm kimliği.|

### **Yanıt Açıklaması**

```json
{
Void
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/CopyFile) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntıları yöneterek proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{< /tab >}}
{{< /tabs >}}

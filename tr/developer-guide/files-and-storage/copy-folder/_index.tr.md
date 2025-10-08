---
title: Klasörü Kopyala
second_title: Documen
linktitle: Klasörü Kopyala
type: docs
url: /tr/copy-folder/
keywords: Excel API, Copy Folder, Office Cloud, REST API, Spreadsheet Management, File Operation
description: API bulut ortamında klasörleri verimli bir şekilde kopyalamak için CopyFolder Aspose.Cells'in nasıl kullanılacağını öğrenin
weight: 100
kwords: Excel, Office Bulut, REST API, Klasörü Kopyala, Dosya Yönetimi, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir
---
## **Excel API: Klasörü Kopyala**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **İşlev Açıklaması**

 The**Klasör Kopyala**API, kullanıcıların Aspose.Cells bulut depolama alanındaki mevcut bir klasörü çoğaltmalarına olanak tanır. Bu işlev, dosyaları verimli bir şekilde yönetmek ve kullanıcıların içerikleri manuel olarak aktarmadan yedeklemeler oluşturmalarına veya çalışmalarını düzenlemelerine olanak tanımak için önemlidir.

###  İstek parametreleri**Klasör Kopyala** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|----------------|--|-----------------------|-------------------------------------|
| srcPath| Sicim| Yol| Kopyalanacak kaynak klasörün yolu.|
| hedefYolu| Sicim| Sorgu| Yeni klasörün oluşturulacağı yol.|
| srcDepolamaAdı| Sicim| Sorgu| Kaynak klasörü içeren depolamanın adı.|
| hedefDepolamaAdı| Sicim| Sorgu| Klasörün kopyalanacağı hedef depolama alanının adı.|

### **Yanıt Açıklaması**

```json
{
Void
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}

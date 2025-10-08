---
title: Klasörü Sil
second_title: Documen
linktitle: Klasörü Sil
type: docs
url: /tr/delete-folder/
keywords: Delete folder, Aspose.Cells API, RESTful API, Excel file management, cloud storag
description: Aspose.Cells'deki deleteFolder API'i kullanarak Aspose.Cells'deki bir klasörün nasıl silineceğini, parametreler ve kod örnekleri dahil olmak üzere öğrenin
weight: 100
kwords: Excel API, Office Bulut, REST API, Elektronik tablo yönetimi, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki klasörü sil
---
## **Excel API : Klasörü Sil**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **İşlev Açıklaması**

`deleteFolder` API, kullanıcıların Aspose.Cells ile ilişkili bulut depolama alanından belirli bir klasörü kaldırmasına olanak tanır. Bu, organizasyonu korumak ve depolama alanını etkili bir şekilde yönetmek için yararlı olabilir.

###  İstek parametreleri**deleteFolder** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| yol| Sicim| Yol| Silinecek klasörün yolu.|
| depolamaAdı| Sicim| Sorgu| Klasörün bulunduğu depolama alanının adı.|
| yinelemeli| Boolean| Sorgu| Silmenin yinelemeli olup olmayacağını ve klasördeki tüm içeriklerin de silineceğini belirtir.|

### **Yanıt Açıklaması**

```json
{
Void
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder) herkesin erişebileceği bir programlama arayüzü tanımlar ve doğrudan bir web tarayıcısından REST etkileşimleri gerçekleştirmenize olanak tanır.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntıları yöneterek proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}

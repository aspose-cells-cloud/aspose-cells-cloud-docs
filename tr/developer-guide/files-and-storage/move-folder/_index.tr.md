---
title: Klasörü Taşı
second_title: Documen
linktitle: Klasörü Taşı
type: docs
url: /tr/move-folder/
keywords: Move folder API, Excel API, Folder management, REST API, Aspose.Cells, Cloud storag
description: Bu dokümantasyon, Aspose.Cells bulut depolama alanındaki klasörleri yönetmek için API Klasörünü Taşıma'nın kullanımına ilişkin kapsamlı bir kılavuz sağlar
weight: 100
kwords: Excel API, Klasörü taşı API, Office Bulut, REST API, Elektronik tablo yönetimi, PDF, CSV, JSON, Markdown, Bir çalışma sayfasındaki tüm boş hücreleri eşleştir Excel
---
## **Excel API: Klasörü Taşı**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **İşlev Açıklaması**

API numaralı bu cihaz, kullanıcıların Aspose.Cells bulut depolama alanında bir klasörü bir konumdan diğerine taşımasına olanak tanır. Dosyaları düzenlemek ve bulut depolama alanını etkili bir şekilde yönetmek için olmazsa olmazdır.

###  İstek parametreleri**Klasörü taşı** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|----------------|--|------------------------|--------------------------------------------------------|
| srcPath| Sicim| Yol| Taşınacak klasörün kaynak yolu.|
| hedefYolu| Sicim| Sorgu| Klasörün taşınması gereken hedef yol.|
| srcDepolamaAdı| Sicim| Sorgu| Kaynak depolamanın adı.|
| hedefDepolamaAdı| Sicim| Sorgu| Hedef depolama alanının adı.|

### **Yanıt Açıklaması**

```json
{
Void
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}

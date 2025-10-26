---
title: Aspose.Cells AP'den Dosyayı İndirin
second_title: Developer Guide for Aspose.Cells AP
linktitle: AP Dosyasını İndir
type: docs
url: /tr/download-file/
keywords: Aspose.Cells API, Download File, REST API, Excel File, Office Cloud, Spreadsheet Download, File Management, File Retrieval, CSV, PDF, JSON, Markdow
description: Aspose.Cells API'i kullanarak Excel, PDF, CSV ve daha fazlasını içeren dosyaları nasıl indireceğinizi öğrenin
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel Dosyasını İndir, Boş Cells'i Al
---
## **Excel API: Dosyayı İndir**

```
GET http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **İşlev Açıklaması**

 The**Dosyayı indir** API, Aspose Bulut depolama alanında depolanan dosyaları almanızı sağlar. Bu işlev, elektronik tablolar, PDF'ler ve CSV'ler dahil olmak üzere çeşitli dosya biçimlerini yönetmek ve bunlara erişmek için gereklidir.

###  İstek parametreleri**Dosyayı indir** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| yol| Sicim| Yol| İndirmek istediğiniz dosyanın yolu.|
| depolamaAdı| Sicim| Sorgu| Dosyanın alınacağı depolama alanının adı.|
| sürüm kimliği| Sicim| Sorgu| İndirilecek dosyanın sürüm tanımlayıcısı (varsa).|

### **Yanıt Açıklaması**

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

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) herkesin erişebileceği bir programlama arayüzü tanımlar ve doğrudan bir web tarayıcısından REST etkileşimleri gerçekleştirmenize olanak tanır.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntıları yönetir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}

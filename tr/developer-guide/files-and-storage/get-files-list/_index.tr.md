---
title: Dosya Listesini Alın - Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: Dosyaları Al Listesi
type: docs
url: /tr/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: Aspose.Cells API'i kullanarak belirtilen bir klasörden dosya listesinin nasıl alınacağını öğrenin. Bu kılavuz, istek parametreleri, yanıt yapısı ve çeşitli programlama dillerindeki kod örnekleri hakkında ayrıntılar sağlar.
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Bulut Dosya Yönetimi, Dosya Listesini Al
---
## **Excel API: Dosya Listesini Al**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **İşlev Açıklaması**

 The**getFilesList**API, kullanıcıların Aspose.Cells bulut depolama alanındaki belirli bir dizinde bulunan dosya ve klasörlerin kapsamlı bir listesini almalarına olanak tanır. Bu uç nokta, dosyaları verimli bir şekilde yönetmek için çok önemlidir ve çeşitli dosya biçimlerini destekler.

###  İstek parametreleri**getFilesList** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| yol| Sicim| Yol| Dosya listesinin alınacağı bulut depolama alanındaki klasörün yolu.|
| depolamaAdı| Sicim| Sorgu| Erişilecek depolama alanının adı.|

### **Yanıt Açıklaması**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) REST etkileşimlerini doğrudan bir web tarayıcısından etkinleştiren, kolay entegrasyon ve test imkânı sağlayan, herkese açık bir programlama arayüzü tanımlar.

## Excel API SDK

 Bir SDK kullanmak, geliştirme sürecinizi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntıları yöneterek proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Bulut SDK'sının tam listesi için lütfen şu adresi ziyaret edin:[GitHub deposu](https://github.com/aspose-cells-cloud).

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}

---
title: Disk Usag'ı Alın
second_title: Documen
linktitle: Disk Usag'ı Alın
type: docs
url: /tr/get-disk-usage/
keywords: API, Disk Usage, Aspose, Cloud, Excel, REST, Storage, Disc Space, SDK, Programming Interfac
description: Aspose Bulutunda Excel API için geçerli disk kullanımını alın
weight: 100
kwords: Disk Kullanımı, Excel API, Aspose Bulut, REST API, Depolama Bilgileri, SDK Örnekleri, Programlama Arayüzü
---
## **Excel API : GetDiskUsage**

```
GET http://api.aspose.cloud/v4.0/cells/storage/disk
```

### **İşlev Açıklaması**

Bu API uç noktası, Aspose Bulut ortamında Excel API için geçerli disk kullanımını alır ve geliştiricilerin uygulamaları tarafından kullanılan depolama alanını izlemelerine olanak tanır.

###  İstek parametreleri**getDiskUsage** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|depolamaAdı|Sicim|Sorgu|Disk kullanımının alınacağı depolama alanının adı.|

### **Yanıt Açıklaması**

```json
{
  "Name": "DiskUsage",
  "Description": [
    "Class for disk space information."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": [
        "Amount of disk space used by the application."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": [
        "Total available disk space."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntıları yöneterek proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{< /tab >}}
{{< /tabs >}}

---
title: Dosya Sürümünü Al
second_title: Documen
linktitle: Dosya Sürümünü Al
type: docs
url: /tr/get-file-versions/
keywords: file versions, Excel API, Office Cloud, REST API, spreadsheet management, document histor
description: Aspose.Cells Bulutunda depolanan dosyaların sürümlerini alın ve yönetin, belge yönetimini ve iş birliğini geliştirin
weight: 100
kwords: Dosya Sürümlerini Alın, Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, belge yönetimi
---
## **Excel API: Dosya Sürümlerini Al**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **İşlev Açıklaması**

 The**DosyaSürümleriniAl** API, kullanıcıların Aspose.Cells Bulutunda depolanan belirli bir dosyanın farklı sürümlerini almalarına olanak tanır. Bu işlevsellik, belge bütünlüğünü korumak ve zaman içindeki değişiklikleri izlemek için çok önemlidir.

###  İstek parametreleri**DosyaSürümleriniAl** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| yol| Sicim| Yol| Sürümlerinin alınacağı dosyanın yolu.|
| depolamaAdı| Sicim| Sorgu| Dosyanın bulunduğu depolama alanının adı.|

### **Yanıt Açıklaması**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)REST etkileşimlerini doğrudan bir web tarayıcısından yürütmek için kapsamlı bir programlama arayüzü sağlar.

## Excel API SDK

 Bir SDK kullanmak, düşük seviyeli karmaşıklıkları soyutlayarak geliştirmeyi kolaylaştırır ve geliştiricilerin temel işlevlere odaklanmasını sağlar.[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli programlama dillerinde Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{< /tab >}}
{{< /tabs >}}

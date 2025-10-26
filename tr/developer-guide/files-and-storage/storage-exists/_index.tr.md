---
title: Depolama Var
second_title: Documen
linktitle: Depolama Var
type: docs
url: /tr/storage-exists/
keywords: Excel API, Storage Exists, REST API, Office Cloud, Cloud Storage, Excel Worksheet, Check Storage, Data Management, API Integratio
description: Aspose.Cells REST API'i kullanarak depolama alanının mevcut olup olmadığını nasıl kontrol edeceğinizi öğrenin. Bu kılavuz, ayrıntılı API uç nokta bilgileri, istek parametreleri ve yanıt açıklamaları sağlar.
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir
---
## **Excel API : Depolama Mevcut**

```
GET http://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **İşlev Açıklaması**

 The**depolamaVar**API, belirtilen bir depolama alanının Aspose.Cells bulut hizmetinde mevcut olup olmadığını kontrol eder. Bu işlevsellik, depolama alanına bağlı tüm işlemlerin hatasız bir şekilde devam etmesini sağlamak için kritik öneme sahiptir.

###  İstek parametreleri**depolamaVar** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|depolamaAdı|Sicim|Yol|Varlığı kontrol edilecek depolamanın adı.|

### **Yanıt Açıklaması**

```json
{
  "Name": "StorageExist",
  "Description": [
    "Indicates whether the specified storage exists."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/StorageController/StorageExists) Geliştiricilerin doğrudan bir web tarayıcısı üzerinden REST API ile sorunsuz bir şekilde etkileşim kurmasına olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en etkili yoludur. Bir SDK, düşük seviyeli uygulama ayrıntılarını özetleyerek geliştiricilerin proje görevlerine odaklanmalarını sağlar. Mevcut Aspose.Cells Bulut SDK'larının kapsamlı bir listesi için lütfen şu adresi ziyaret edin:[GitHub deposu](https://github.com/aspose-cells-cloud).

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerine API çağrılarının nasıl yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}

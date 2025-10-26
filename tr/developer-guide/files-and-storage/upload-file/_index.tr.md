---
title: Dosyayı Aspose Cep Telefonuna Yükle
second_title: Developer Guide for File Uploa
linktitle: Dosyayı Yükle
type: docs
url: /tr/upload-file/
keywords: Aspose, file upload, Excel API, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, upload Excel files, match blank cell
description: Aspose Cells API'i kullanarak dosyaların nasıl yükleneceğine dair kapsamlı kılavuz, parametreler ve yanıt yapısı dahil
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir, dosyayı yükle
---
## **Aspose Cells API: Dosya Yükle**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **İşlev Açıklaması**

 The**Dosyayı yükle** API, geliştiricilerin dosyaları doğrudan Aspose Cells ile işlenmek üzere bulut depolama alanına yüklemelerini sağlar.

###  İstek parametreleri**Dosyayı yükle** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
| Dosyaları Yükle| Dosya| FormVerileri|Dosyaları bulut depolama alanına yükleyin.|
| yol| Sicim| Yol| Bulut depolama alanındaki hedef yol. Dosyanın yükleneceği yolu belirtin.|
| depolamaAdı| Sicim| Sorgu| Dosyanın yükleneceği depolama alanının adı.|

### **Yanıt Açıklaması**

```json
{
  "Name": "FilesUploadResult",
  "Description": [
    "File upload result"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": [
        "List of uploaded file names"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": [
        "List of errors."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/UploadFile) API'in ayrıntılı bir açıklamasını sağlar ve geliştiricilerin doğrudan bir web tarayıcısından REST etkileşimleri gerçekleştirmesini sağlar.

## Aspose Cells API SDK

 Bir SDK kullanmak, düşük seviyeli ayrıntıları yöneterek geliştirme verimliliğini artırır ve geliştiricilerin proje görevlerine odaklanmasını sağlar.[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının kapsamlı listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}

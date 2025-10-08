---
title: Aspose.Cells Cloud WEb API - Genel Anahtar Alın
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: Kamu Anahtarını Alın
type: docs
url: /tr/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: Güvenli veri şifrelemesi için asimetrik bir genel anahtar alın
weight: 100
kwords: asimetrik şifreleme, genel anahtar, REST API, Excel API, güvenlik, veri şifreleme, API entegrasyonu, JSON, API belgeleri
---
Asimetrik şifreleme algoritmasından genel anahtarı alır.

## **API Genel Anahtarını Alın**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
|||||

### **Cevap**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

## SDK'larla API genel anahtarını nasıl kullanırım?

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) web tarayıcınızdan doğrudan REST etkileşimleri gerçekleştirmenizi sağlayan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları yöneterek, hücreler için genel anahtarı minimum kodla kolayca almanızı sağlar.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

---
title: Aspose.Cells Cloud Web API - Erişim İzni Sonrası
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: Erişim İzni Sonrası
type: docs
url: /tr/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: Kullanıcı isteklerini Aspose Bulut kimlik doğrulama sunucusuna ileten bir proxy hizmeti gibi davranan ve ortaya çıkan erişim belirtecini istemciye güvenli bir şekilde döndüren Cells Bulut Alma Belirteci API'i kullanarak bir Erişim Belirteci alın.
weight: 100
kwords: Excel, Office Bulut, REST API, Kimlik Doğrulama, Jeton Yönetimi, Ara Yazılım Entegrasyonu, Güvenli API, Aspose Bulut
---
Cells Cloud Get Token API'i İstemci Kimliği ve Gizli Anahtarı ile kullanarak bir Erişim Belirteci alın.

## **Posta Erişim Jetonu API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| İstemci Kimliği| sicim| sorgu| İstemci Kimliği|
| Müşteri Sırrı| sicim| sorgu| Müşteri Sırrı|

### **Cevap**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## SDK'larla API genel anahtarını nasıl kullanırım?

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları yöneterek, hücreler için erişim belirtecini minimum kodla kolayca uygulamanıza olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Cloud SDK'larının tam listesi için. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

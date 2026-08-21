---
title: "Aspose.Cells Cloud API – Genel Anahtarı Al (v4.0) | REST Dokümantasyonu"
second_title: "Belge"
ArticleTitle: "Genel Anahtarı Al"
linktype: "Genel Anahtarı Al"
type: docs
url: /get-public-key/
keywords: "Aspose.Cells, Genel Anahtar, RSA, API, Bulut"
description: "Aspose.Cells Cloud ile veri şifrelemek için kullanılan RSA genel anahtarını alın. Uç nokta, parametreler, örnek istek/yanıt, durum kodları ve SDK kullanım örneklerini içerir."
weight: 100
---

Bu API, asimetrik şifreleme algoritmasından genel anahtarı alır.

**Özet:** Aspose.Cells Genel Anahtar API’sini kullanarak, bulutta Excel dosyaları ile çalışırken verileri şifrelemek için gereken RSA genel anahtarını (2048-bit) edinin. Uç nokta, anahtarı JSON formatında döndürür ve OAuth 2.0 ile korunur.

## **Genel Anahtar API’si**

**Önkoşullar:**  
Bu uç noktayı çağırmadan önce `Cells.Read` kapsamını içeren geçerli bir OAuth 2.0 erişim jetonu edinin.

### **Web API’si**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**Örnek İstek (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür    | Konum   | Açıklama                                                                   |
| ------------- | ------ | ------- | -------------------------------------------------------------------------- |
| Authorization | string | Header  | OAuth2 kimlik doğrulaması için Bearer jetonu (zorunludur).                |
| Accept        | string | Header  | İstenen yanıt formatı, örneğin `application/json` (isteğe bağlı, varsayılan JSON’dur). |

### **Yanıt**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT jetonu.                                   |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                       |

## Genel Anahtar API’sini SDK’lar ile Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey), web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, temel alınan ayrıntıları işler ve genel anahtarı en az kodla uygulamanıza entegre etmenize olanak tanır.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıda en yaygın diller için somut örnekler verilmiştir:

---
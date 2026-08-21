---
title: "Aspose.Cells Cloud Web API - Post Erişim Belirteci"
second_title: "Doküman"
ArticleTitle: "İstemci Kimliği ve Gizli Anahtarı ile Erişim Belirteci Alın"
linktitle: "Post Erişim Belirteci"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, Bulut, Erişim Belirteci, OAuth2, API, Kimlik Doğrulama, REST, Excel, Office Bulut"
description: "İstemci kimliğinizi ve gizli anahtarınızı kullanarak POST /cells/connect/token uç noktasını çağırarak Aspose.Cells Cloud için bir OAuth2 erişim belirteci alın."
weight: 100
---

İstemci kimliği ve gizli anahtarı ile Cells Cloud Get Token API'sini kullanarak bir erişim belirteci alın.

## Post Erişim Belirteci API

Uç noktayı çağırmadan önce şunların olduğundan emin olun:

* Kayıtlı bir Aspose Cloud hesabınız.  
* Aspose Cloud portalında oluşturulan bir **İstemci Kimliği** ve **İstemci Gizli Anahtarı**.  

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Konum                         | Açıklama                                          |
| ------------- | ----- | ----------------------------- | ------------------------------------------------- |
| grant_type    | string | gövde (form‑url‑encoded)      | OAuth için gerekli sabit değer `client_credentials`. |
| client_id     | string | gövde (form‑url‑encoded)      | size verilen istemci tanımlayıcısı.              |
| client_secret | string | gövde (form‑url‑encoded)      | İstemci kimliğiyle ilişkili gizli anahtar.       |

**Örnek istek (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

### Yanıt

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**HTTP Durum Kodları**

| Kod | Anlam                        | Açıklama                                              |
|-----|------------------------------|-------------------------------------------------------|
| 200 | Tamam                        | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek                 | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz                     | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük                | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Sunucu İç Hatası             | Beklenmeyen sunucu hatası. |

**Hata işleme örneği**

```json
{
  "error": "invalid_client",
  "error_description": "İstemci kimlik doğrulaması başarısız oldu."
}
```

## Get public key API'sini SDK’lar ile Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken), bir web tarayıcısından doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, başlamak için en hızlı yoldur. SDK, temel HTTP ayrıntılarını soyutlar ve minimum kodla Cells için bir erişim belirteci almanızı sağlar.

Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın. Bir SDK, alt seviye ayrıntıları yöneterek size proje görevlerinize odaklanmanızı sağlar.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:  
---
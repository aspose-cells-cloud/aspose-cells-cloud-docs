---
title: "Aspose.Cells Cloud Web API - Aspose Cells Cloud Durumunu Alın"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud Durumunu Alın"
linktype: "Aspose.Cells Cloud Durumunu Alın"
type: docs
url: /tr/get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, Bulut API, Sağlık Kontrolü, Excel, REST"
description: "Aspose.Cells Cloud Hizmeti’nin sağlık durumunu gerçek zamanlı olarak izleyin."
weight: 100
---

Aspose.Cells Cloud Hizmeti’nin sağlık durumunu gerçek zamanlı olarak alın.

**Ön Gereksinimler:** Bu API’yi çağırmak için Aspose Cloud istemci kimlik bilgilerinizi kullanarak bir Bearer erişim jetonu edinmelisiniz. Jetonu `Authorization` başlığında `Bearer {access_token}` olarak ekleyin.

## **Aspose.Cells Cloud Durumunu Alın**

### **Web API’si**

Uç nokta HTTP **GET** yöntemini kullanır ve istek gövdesi gerektirmez.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür   | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                |
| ------------- | ----- | ---------------------------- | --------------------------------------- |
| Authorization | String | Başlık                      | Kimlik doğrulama için Bearer jetonu (zorunludur). |
| format        | String | Sorgu                       | İstenen yanıt formatı, örneğin `json`. |

### **Yanıt**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**Yanıt Şeması**

| Alan      | Tür               | Açıklama                                   |
| --------- | ----------------- | ------------------------------------------ |
| status    | string            | Hizmet durumu (`OK`, `Degraded`, vb.).    |
| service   | string            | Hizmetin adı.                              |
| timestamp | string (ISO‑8601) | Durum kontrolünün yapıldığı zaman.         |

API, Aspose.Cells Cloud hizmetinin mevcut sağlık **durumunu** içeren standart bir JSON yükü döndürür.

**HTTP Durum Kodları**

- **200 OK** – Hizmet sağlıklı ve yanıt durum bilgilerini içerir.
- **401 Unauthorized** – Eksik veya geçersiz kimlik doğrulama jetonu.
- **503 Service Unavailable** – Hizmet şu anda bakım nedeniyle kapalı veya sorun yaşıyor olabilir.

## Get Aspose.Cells Cloud Status API’sini SDK’lar ile Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus), bir web tarayıcısından doğrudan REST etkileşimlerinde bulunmanıza olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak entegrasyonu basitleştirir ve tekrarlayan kod miktarını azaltır. SDK, alt seviye ayrıntıları yönetir ve Aspose.Cells Cloud çalışma durumunu minimum çabayla almanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

---
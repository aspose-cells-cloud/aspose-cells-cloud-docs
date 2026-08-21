---
title: "Aspose.Cells Cloud – Hizmet Sağlığını Kontrol Et (API)"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud Sağlıktan Kontrolü"
linktitle: "Bulut Hizmet Sağlığını Kontrol Et"
type: docs
url: /check-cloud-service-health/
keywords: "Aspose.Cells Cloud, API sağlık kontrolü, REST durumu, bulut hizmeti izleme"
description: "Aspose.Cells Cloud sağlığını gerçek zamanlı olarak izleyin. GET /v4.0/cells/status/check uç noktasını, parametrelerini, yanıt formatını ve SDK örneklerini öğrenin."
weight: 100
---

Aspose.Cells Cloud hizmetlerinin sağlığını kontrol edin.

**Ön Gereksinimler**  
Bu uç noktayı çağırmak için geçerli bir Aspose Cloud erişim belirteci (token) sahibi olmanız gerekir. Belirteci almak için Aspose Cloud Dashboard’da bir uygulama kaydedin ve istemci kimliği (client-id) ile istemci sırrı (client-secret) kullanarak OAuth2 belirteç uç noktasından Bearer belirteci isteyin. Belirteci aşağıdaki gibi `Authorization` başlığına ekleyin.

## **Bulut Hizmet Sağlığını Kontrol Et**

### **Web API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek Parametreleri**

| Parametre     | Tür     | Gerekli | Açıklama                                                       |
| ------------- | ------- | ------- | -------------------------------------------------------------- |
| Authorization | başlık  | Evet    | Kimlik doğrulama için Bearer belirteci (`Authorization: Bearer <token>`). |
| detail        | sorgu   | Hayır   | Ayrıntılı bileşen bilgilerini dahil etmek için `true` olarak ayarlayın. |
| Accept        | başlık  | Hayır   | İstenen yanıt formatı; varsayılan değer `application/json`.   |

### **Yanıt**

Hizmet, istek başarıyla tamamlandığında bir JSON yükü döndürür.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "İşletimde",
    "storage": "İşletimde",
    "database": "İşletimde"
  }
}
```

**HTTP durum kodları**

| Kod | Anlamı              | Açıklama                                                  |
| --- | ------------------- | --------------------------------------------------------- |
| 200 | OK (Tamam)          | Hizmet sağlıklı; yukarıdaki JSON örneğine bakın.           |
| 401 | Yetkisiz            | Geçersiz veya eksik kimlik doğrulama belirteci.            |
| 503 | Hizmet Kullanılamıyor | Hizmet şu anda sağlıklı değil veya bakım altında.          |
| 4xx | İstemci hatası      | Yanlış istek parametreleri veya bozuk istek.               |
| 5xx | Sunucu hatası       | Beklenmeyen sunucu hatası; daha sonra yeniden deneyin.     |

## Aspose.Cells Cloud Durum API’sini SDK’larla Nasıl Kullanılır

### OpenAPI Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, temel alınan ayrıntıları yöneterek Cells için minimum kodla bir bulut sağlığı kontrolü uygulamanızı sağlar.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıda, en yaygın SDK’larla sağlıktan kontrol uç noktasını nasıl çağıracağınızla ilgili örnek kod parçacıkları verilmiştir.

---
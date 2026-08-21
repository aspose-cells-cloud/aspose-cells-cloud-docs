---
title: "Aspose.Cells Cloud API ile Başlangıç – Excel Dosyalarını 3 Basit Adımda İşleyin"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud Başlangıç Kılavuzu"
linktitle: "Başlangıç"
type: docs
url: /getting-started/
description: "Aspose.Cells Cloud REST API kullanarak Excel dosyalarını nasıl yükleyeceğinizi, dönüştüreceğinizi ve indireceğinizi üç basit adımda öğrenin. cURL kod örneklerini içerir."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, elektronik tablo dönüştürme, Excel'den PDF'e, bulut elektronik tablo, Aspose.Cells Cloud API"
---

- [Genel Bakış](/cells/overview/)
- [Hızlı Başlangıç](/cells/quickstart/)
- [Mevcut SDK’lar](/cells/available-sdks/)
- [Desteklenen Platformlar](/cells/supported-platforms/)
- [Desteklenen Dosya Biçimleri](/cells/supported-file-formats/)
- [Aspose.Cells Cloud’u Deneyin](/cells/evaluate-aspose-cells/)
- [Fiyatlandırma Planı](/cells/pricing-plan/)
- [Teknik Destek](/cells/technical-support/)
- [Docker Konteynerini Nasıl Çalıştırırız?](/cells/how-to-run-docker-container/)

**Başlangıç Kılavuzu**

Başlamadan önce geçerli bir **Aspose Cloud API anahtarı** ve **depolama adı**na sahip olduğunuzdan emin olun. Bu kimlik bilgileri, sonraki tüm API çağrıları için gereklidir.

**Adım 1: Excel dosyası yükleme**  
Kaynak çalışma kitabınızı Aspose Cloud deposuna yükleyin.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*İstek gövdesi*: Dosya ikili akış olarak (`application/octet‑stream`) gönderilir.  
*Gerekli parametreler*:

- `path` – dosyanın kaydedileceği depo yolu (örneğin, `klasör/sample.xlsx`).

**Adım 2: Çalışma kitabını PDF’e dönüştürme**  
Dosya depolandıktan sonra dönüştürme isteği gönderin.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*Gerekli parametreler*:

- `name` – yüklenen çalışma kitabının adı (örneğin, `sample.xlsx`).
- `format` – hedef biçim (`pdf`).
- `outputPath` – dönüştürülen dosyanın kaydedileceği depo yolu (örneğin, `klasör/result.pdf`).

*Örnek yanıt yükü* (JSON):

```json
{
  "status": "OK",
  "outputPath": "klasör/result.pdf"
}
```

**Adım 3: Dönüştürülmüş PDF’yi indirme**  
Oluşan PDF’yi depodan alın.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*Gerekli parametreler*:

- `outputPath` – önceki adımda oluşturulan PDF’nin yolu.

**Örnek İstek / Yanıt Özeti**

| İşlem | HTTP Yöntemi | Uç Nokta (örnek) | Parametreler | Başarı Durumu |
|-------|--------------|------------------|--------------|----------------|
| Yükleme | PUT | /cells/storage/file/{path} | `path` (depolama konumu) | 200 OK |
| Dönüştürme | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| İndirme | GET | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**Yaygın Hata Kodları**

- **400 Bad Request (Bad Request)** – Eksik veya geçersiz parametreler.  
- **401 Unauthorized (Unauthorized)** – Geçersiz veya eksik erişim jetonu.  
- **404 Not Found (Not Found)** – Belirtilen dosya veya yol mevcut değil.  
- **500 Internal Server Error (Internal Server Error)** – Beklenmeyen sunucu hatası; yeniden deneyin veya destek ile iletişime geçin.
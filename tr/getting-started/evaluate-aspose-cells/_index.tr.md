---
title: "Aspose.Cells Cloud'ı Değerlendirin"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud'ı Değerlendirin"
LinkTitle: "Değerlendir"
type: docs
url: /evaluate-aspose-cells/
description: "Excel dosyalarını ve diğer elektronik tablo formatlarını oluşturma, dönüştürme, birleştirme, bölme, koruma ve manipüle etme için REST API olan Aspose.Cells Cloud’u keşfedin."
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - elektronik tablo manipülasyonu
  - ücretsiz deneme
  - değerlendir
---

**Aspose.Cells Cloud** REST API’lerini Aspose Cloud Dashboard’da ücretsiz deneme hesabı oluşturarak değerlendirebilirsiniz. Kayıt olduktan sonra aylık 150 API çağrısı yapmanızı sağlayan bir **Client Id** (İstemci Kimliği) ve **Client Secret** (İstemci Sırrı) alacaksınız.

**Ön Gereksinimler**  
Başlamadan önce aktif bir internet bağlantınız ve desteklenen bir geliştirme ortamınız olduğundan emin olun. API doğrudan HTTP üzerinden çağrılabilir veya kolay entegrasyon için Aspose.Cells SDK’larından birini (.NET, Java, Python, PHP vb.) kullanabilirsiniz.

**Hızlı başlangıç adımları**

1. **Ücretsiz deneme hesabı oluşturun** – [Aspose Cloud Dashboard](https://dashboard.aspose.cloud) adresine gidin, kaydolun ve e-posta adresinizi doğrulayın.  
2. **Kimlik bilgilerini edinin** – Dashboard’da **Kimlik Doğrulama** (Authentication) bölümü altında *Client Id* ve *Client Secret* değerlerini bulun.  
3. **Erişim belirteci oluşturun** – Kimlik bilgilerinizle (`grant_type=client_credentials`, `client_id`, `client_secret` form-urlencoded olarak) `https://api.aspose.cloud/connect/token` adresine bir `POST` isteği gönderin (tam yük bilgisi için API referansına bakın).  
4. **İlk API çağrınızı yapın** – Belirteci `Authorization: Bearer <token>` başlığına ekleyin ve basit bir uç noktayı çağırın, örneğin: `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`.  

Ücretsiz deneme, hizmetin yeteneklerini herhangi bir maliyet olmadan erken aşamada geliştirme ve test etmenize olanak tanır.

**API referans özeti**

| İşlem | Yöntem | URL | Gerekli parametreler | Örnek yanıt |
|-------|--------|-----|---------------------|-------------|
| Erişim belirtecini alın | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret` (form-urlencoded) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| Çalışma sayfalarını listele | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | Yol: `{file}` – yüklenmiş çalışma kitabının adı; Başlık: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

Ayrıntılı fiyatlandırma, kullanım sınırları ve ek plan seçenekleri için [Deneme Planı](https://purchase.aspose.cloud/trial) sayfasına bakın.
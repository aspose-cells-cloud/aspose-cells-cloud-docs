---
title: "Aspise.Cells Cloud Web API – Diğer Özellikler: Sağlık Kontrolü, Genel Anahtarı Alın"
linktitle: "Diğer Özellikler"
ArticleTitle: "Diğer Özellikler: Sağlık Kontrolü, Genel Anahtarı Alın"
second_title: "Belge"
type: docs
url: /tr/other-features/
keywords: "Aspose.Cells, Cloud API, sağlık kontrolü, genel anahtar, erişim jetonu, Excel, REST"
description: "Aspose.Cells Cloud’un diğer özelliklerini keşfedin: sağlık kontrolü uç noktası, genel anahtar alma ve jeton oluşturma işlemleriyle Excel API entegrasyonlarınızı güvenli hale getirin."
weight: 180
---

**Ön Gereksinimler** – Aşağıda listelenen özellikleri kullanmak için geçerli bir Aspose Cloud aboneliğine ve kimlik doğrulama için etkin bir **İstemci Kimliği** / **İstemci Sırrı** çiftine sahip olmanız gerekir.

Bu “Diğer Özellikler”, Aspose.Cells Cloud API’si için temel destek işlemleri sağlar: hizmetin erişilebilirliğini ve düzgün çalıştığını doğrulama, kriptografik anahtarları alma ve erişim jetonları oluşturma gibi. Genellikle çalışma kitaplığıyla ilgili uç noktalarla çalışmadan önce çağrılırlar.

- **[Aspose.Cells Cloud Sağlık Kontrolü](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Aspose.Cells Cloud hizmetine ulaşılabilir olduğunu ve düzgün çalıştığını doğrulayın. Başarılı bir çağrı, JSON olarak `{ "status": "OK" }` ve HTTP durumu kodu **200** döndürür. İş akışınızın erken aşamasında gereksiz hataları önlemek için bu uç noktayı kullanın.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">Daha fazla bilgi edinin</a>

- **[Aspose.Cells Cloud Çalışma Durumunu Alın](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Hizmetin şu anki çalışma zamanı durumunu alın. Yanıt, API’nin tam olarak çalışır durumda mı, bakım modunda mı yoksa sorunlar yaşıyor mu olduğunu gösterir.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">Daha fazla bilgi edinin</a>

- **[Genel Anahtarı Alın](https://docs.aspose.cloud/cells/get-public-key/)**  
  Aspose.Cells Cloud tarafından verilen JWT jetonlarını doğrulamak için kullanılan RSA genel anahtarını (PEM formatında) alın. Bu anahtar, jetonları sunucu tarafınızda doğrularken gereklidir.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">Daha fazla bilgi edinin</a>

- **[İstemci Kimliği ve Sırrı ile Erişim Jetonu Alın](https://docs.aspose.cloud/cells/post-access-token/)**  
  **client_credentials** yetkilendirme türü kullanarak bir OAuth 2.0 erişim jetonu oluşturun. İsteğe gövdesine **İstemci Kimliğinizi** ve **İstemci Sırrınızı** ekleyin; yanıt `access_token`, `token_type` ve `expires_in` değerlerini içerir. Bu jeton, sonraki tüm API çağrıları için `Authorization` başlığına eklenmelidir.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">Daha fazla bilgi edinin</a>
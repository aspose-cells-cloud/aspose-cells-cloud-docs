---
title: "Aspose.Cells Cloud Docker Konteynerini Nasıl Çalıştırılır?"
secondtitle: "Belge"
ArticleTitle: "Aspose.Cells Cloud Docker Konteynerini Nasıl Çalıştırılır?"
linktitle: "Konteyner Çalıştırma"
type: docs
url: /tr/run-aspose-cells-cloud-docker-container/
description: "Aspose.Cells Cloud’u Windows Server 2022’de Docker konteyneri olarak nasıl başlatacağınızı öğrenin. Deneme, ölçülü faturalandırma, lisans faturalandırma, depolama yapılandırması ve sağlık kontrolü için adım adım komutlar."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, deneme modu, ölçülü faturalandırma, lisans faturalandırma, depolama yapılandırması"
---

Aspose.Cells Cloud Docker, Aspose.Cells Cloud API’sini yerel olarak veya özel bir bulutta barındıran, çalıştırılmaya hazır konteyner imajı sağlar. Bu kılavuz, konteyneri **Deneme**, **Ölçülü Faturalandırma** ve **Lisans Faturalandırma** olmak üzere üç yaygın lisanslama modunda nasıl başlatacağınızı gösterir; ayrıca bir erişim belirteci (token) kullanan bir varyasyon da içerir. Tüm komutlar, Windows Server 2022’de PowerShell için yazılmıştır; Linux kullanıyorsanız hacim yollarını (volume paths) uygun şekilde değiştirin.

**Ön Gereksinimler**

- Docker Engine 20.10 veya üzeri sürümün yüklü ve çalışır durumda olması.  
- PowerShell 5.1 veya PowerShell 7+.  
- Konteyner içindeki 5000 numaralı portun (ana makine portu 47900’e eşlenir) açık olması ve ana makinenin güvenlik duvarının 47900 numaralı porta gelen trafiğe izin vermesi.  
- Ölçülü veya Lisans faturalandırma modları için `LicensePublicKey`, `LicensePrivateKey` veya lisans dosyanızın hazır olması; erişim belirteci modu kullanıyorsanız `AccessToken` bilgisine sahip olmanız gerekir.  
- Konteyner için depolama olarak kullanılacak yerel bir klasör (örneğin `C:\data`).

**Hızlı Başlangıç (Deneme modu)**  

Aşağıdaki komutu çalıştırarak konteyneri deneme modunda başlatın:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## Aspose.Cells Cloud Docker Konteynerini Deneme Modunda Çalıştırma

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Konteyner ön plan modunda çalışır ve ana makinedeki **47900** portunu dinler; bu port, konteynerin iç 5000 numaralı portuna yönlendirilir.

## Aspose.Cells Cloud Docker Konteynerini Ölçülü Faturalandırma Modunda Çalıştırma

```powershell
# Windows Server 2022
# Ölçülü faturalandırma modu: LicensePublicKey ve LicensePrivateKey’i ortam değişkenleri olarak ayarlayın.
# Depolama klasörünü bağlayın (ana makine → konteyner)
#   -v c:/data:c:/data
# API’nin sistem yazı tiplerine erişebilmesi için Windows yazı tipi klasörünü bağlayın
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Konteyner ayrık (detached) modda (`-d`) çalışır. Başladıktan sonra hizmetin erişilebilir olduğunu doğrulayabilirsiniz:

```powershell
curl http://localhost:47900/v3.0/health
```

**Örnek `storageResource.json` dosyası**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## Aspose.Cells Cloud Docker Konteynerini Lisans Faturalandırma Modunda Çalıştırma

```powershell
# Windows Server 2022
# Lisans faturalandırma modu: LicenseFile ortam değişkeni ile lisans dosyasını sağlayın.
# Depolama klasörünü bağlayın (ana makine → konteyner)
#   -v c:/data:c:/data
# Windows yazı tipi klasörünü bağlayın
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## Aspose.Cells Cloud Docker Konteynerini Erişim Belirteci ile Çalıştırma

```powershell
# Windows Server 2022
# Erişim belirteci modu: AccessToken’i ve isteğe bağlı olarak ölçülü faturalandırma anahtarlarını ayarlayın.
# Depolama klasörünü bağlayın
#   -v c:/data:c:/data
# Windows yazı tipi klasörünü bağlayın
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Konteyneri başlattıktan sonra, daha önce gösterilen aynı sağlık kontrolü komutu ile hizmetin çalıştığını doğrulayın.

## Referans Belgesi

- [Aspose.Cells Cloud Docker Konteyneri depolama yapılandırması nasıl yapılır?](https://docs.aspose.cloud/cells/docker/storage/)

---

### Sorun Giderme

- **Sağlık kontrolü başarısız oluyorsa** – 47900 numaralı portun güvenlik duvarı tarafından engellenmediğinden ve konteynerin çalıştığından (`docker ps`) emin olun.  
- **Lisans hataları** – `LicensePublicKey`, `LicensePrivateKey` veya `LicenseFile` değerlerinin doğru olduğundan ve ortam değişkenlerinin fazla boşluk içermediğinden emin olun.  
- **Depolama erişilemiyor** – Ana makinedeki klasörün (`c:/data`) mevcut olduğundan ve Docker’in bunu okuyup yazmaya yetkili olduğundan emin olun.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud Docker Konteynerini Nasıl Çalıştırılır?",
  "description": "Aspose.Cells Cloud’u Windows Server 2022’de Docker konteyneri olarak başlatmak için adım adım kılavuz; deneme, ölçülü faturalandırma, lisans faturalandırma ve erişim belirteci modlarını kapsar.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, deneme modu, ölçülü faturalandırma, lisans faturalandırma, depolama yapılandırması"
}
</script>
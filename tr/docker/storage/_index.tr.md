---
title: "Aspose.Cells Bulut Docker Konteyneri Depolama Konumunu Ayarlama"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Bulut Docker Konteyneri Depolama Yapılandırması"
linktitle: "Konteyner Depolama"
type: docs
url: /tr/docker/storage/
description: "Aspose.Cells Bulut Docker konteynerleri için depolama konumunu JSON, PowerShell veya Bash kullanarak yapılandırın."
weight: 30
keywords: "Aspose.Cells, Docker, konteyner depolama, JSON yapılandırması, PowerShell, Bash"
---

**Özet**: Bu kılavuz, Aspose.Cells Bulut Docker konteynerleri için depolama konumunu Windows ve Linux üzerinde JSON yapılandırma dosyaları ve Docker run komutlarını kullanarak nasıl yapılandıracağını gösterir.

## Varsayılan Depolama Yapılandırması ##

**Ön Gereksinimler**: Docker Engine 20.10+ yüklü, geçerli Aspose.Cells Bulut lisans anahtarlarınıza (`LicensePublicKey` ve `LicensePrivateKey`) sahip olduğunuz ve depolama için kullanmayı planladığınız ana bilgisayar klasörünün (örneğin, Windows'ta `c:/data` veya Linux'ta `/data`) uygun izinlerle mevcut olduğundan emin olun.

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Varsayılan Konum ##

- **windows**

```powershell
c:\app\storageResource.json
```

- **linux**

```bash
/app/storageResource.json
```

## Özel Depolama Yapılandırması ##

Aspose.Cells Bulut verileri için farklı bir klasör kullanmanız gerektiğinde özel bir depolama profili belirtin.

```bash
docker run -d \
  -v c:/data:c:/data \   # ana bilgisayar klasörünü konteyner depolaması olarak bağlayın
  -p 47900:5000 \        # API bağlantı noktası eşlemesi
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Linux örneği*:

```bash
docker run -d \
  -v /data:/data \   # ana bilgisayar klasörünü konteyner depolaması olarak bağlayın
  -p 47900:5000 \    # API bağlantı noktası eşlemesi
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**Referans Belgesi**:

- [Aspose.Cells Bulut Docker konteynerini nasıl çalıştıracağınız.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Docker Konteyner Özellikleri](https://docs.aspose.cloud/cells/docker/container-features/)
- [Aspose.Cells Bulut Docker Görüntüsünü İndirme](https://docs.aspose.cloud/cells/docker/download-image/)
- [Konteyner Etiketlerini Yönetme](https://docs.aspose.cloud/cells/docker/manage-tags/)
---
title: Aspose.Cells Cloud Docker Container depolama için depolama konumu nasıl ayarlanır?
second_title: Documen
ArticleTitle: Aspose.Cells Cloud Docker Container Storage Configuratio
linktitle: Konteyner Depolama
type: docs
url: /tr/docker/storage/
description: Aspose.Cells Cloud Docker Konteyner depolaması için depolama konumu nasıl ayarlanır?
weight: 30
kwords: Excel Bulut Docker Konteyneri, Kendi Bulut Docker Konteyneri, REST Docker Konteyneri, Elektronik Tablo, PDF, CSV, Json, Markdown, Docker Görüntüsü, Docker Konteynerini Çalıştırma
---
## Varsayılan Depolama Yapılandırması ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

``` json

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

``` json

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

##  Varsayılan Konum ##

- **pencereler**

```powershell

c:\app\storageResource.json

```

- **Linux**

```linux

/app/storageResource.json


```

##  Özel Depolama Yapılandırması ##

Müşteri depolama klasörünü belirttiğinde Aspose.Cells Bulut görüntü dosyası için depolama profilini yeniden belirtmeniz gerekiyor.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**Referans Belgesi** :

- [Aspose.Cells Cloud Docker konteyneri nasıl çalıştırılır.]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)

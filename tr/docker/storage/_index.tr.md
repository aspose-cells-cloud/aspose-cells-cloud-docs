﻿---
title: Depo
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/docker/storage/
description: Aspose.Cells Cloud for Docker hakkında depolama konumu nasıl ayarlanır?
weight: 30
---
##  Varsayılan Depolama Yapılandırması ##

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

##  Varsayılan pozisyon ##


- **pencereler**

```powershell

c:\app\storageResource.json

```

- **linux**

```linux

/app/storageResource.json


```

##  Özel Depolama Yapılandırması ##

Müşteri, depolama klasörünü belirttiğinde, Aspose.Cells Bulut görüntü dosyası için depolama profilini yeniden belirtmeniz gerekir.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Referans Belgesi** : 
  - [Docker Çalıştır]( https://docs.docker.com/engine/reference/commandline/run/)
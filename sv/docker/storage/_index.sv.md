---
title: Så här ställer du in lagringspositionen för Aspose.Cells Cloud Docker Container-lagring
second_title: Documen
ArticleTitle: Aspose.Cells Cloud Docker Container Storage Configuratio
linktitle: Containerlagring
type: docs
url: /sv/docker/storage/
description: Så här ställer du in lagringspositionen för Aspose.Cells Cloud Docker Container-lagring
weight: 30
kwords: Excel Cloud Docker-behållare, Self-Cloud Docker-behållare, REST Docker-behållare, kalkylblad, PDF, CSV, JSON, Markdown, Docker-avbildning, Run Docker-behållare
---
## Standardkonfiguration för lagring ##

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

##  Standardposition ##

- **fönster**

```powershell

c:\app\storageResource.json

```

- **Linux**

```linux

/app/storageResource.json


```

##  Anpassad lagringskonfiguration ##

Behöver ange om lagringsprofilen för molnbildsfilen Aspose.Cells när kunden anger en lagringsmapp.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**Referensdokument** :

- [Hur man kör Cloud Docker-containern Aspose.Cells.]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)

---
title: Förvaring
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/docker/storage/
description: Hur man ställer in lagringsposition för Aspose.Cells Cloud för Docker
weight: 30
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Lagring
---
##  Standardkonfiguration för lagring ##

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

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Referensdokument** : 
  - [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)

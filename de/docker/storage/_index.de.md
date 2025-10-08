---
title: So legen Sie die Speicherposition für Aspose.Cells Cloud Docker Container-Speicher fest
second_title: Documen
ArticleTitle: Aspose.Cells Cloud Docker Container Storage Configuratio
linktitle: Containerlagerung
type: docs
url: /de/docker/storage/
description: So legen Sie die Speicherposition für Aspose.Cells Cloud Docker Container-Speicher fest
weight: 30
kwords: Excel Cloud-Docker-Container, Self-Cloud-Docker-Container, REST-Docker-Container, Tabellenkalkulation, PDF, CSV, Json, Markdown, Docker-Image, Docker-Container ausführen
---
## Standardspeicherkonfiguration ##

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

- **Fenster**

```powershell

c:\app\storageResource.json

```

- **Linux**

```linux

/app/storageResource.json


```

##  Benutzerdefinierte Speicherkonfiguration ##

Das Speicherprofil für die Cloud-Image-Datei Aspose.Cells muss neu angegeben werden, wenn der Kunde einen Speicherordner angeben muss.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**Referenzdokument** :

- [So führen Sie den Cloud Docker-Container Aspose.Cells aus.]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)

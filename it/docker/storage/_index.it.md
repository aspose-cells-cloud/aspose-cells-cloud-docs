---
title: Come impostare la posizione di archiviazione per Aspose.Cells Cloud Docker Container storage
second_title: Documen
ArticleTitle: Aspose.Cells Cloud Docker Container Storage Configuratio
linktitle: Container Storag
type: docs
url: /it/docker/storage/
description: Come impostare la posizione di archiviazione per l'archiviazione del contenitore Cloud Docker Aspose.Cells
weight: 30
kwords: Excel Contenitore Docker cloud, Contenitore Docker self-cloud, Contenitore Docker REST, Foglio di calcolo, PDF, CSV, Json, Markdown, Immagine Docker, Esegui contenitore Docker
---
## Configurazione di archiviazione predefinita ##

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

##  Posizione predefinita ##

- **finestre**

```powershell

c:\app\storageResource.json

```

- **Linux**

```linux

/app/storageResource.json


```

##  Configurazione di archiviazione personalizzata ##

È necessario specificare nuovamente il profilo di archiviazione per il file immagine cloud Aspose.Cells quando il cliente deve specificare la cartella di archiviazione.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**Documento di riferimento** :

- [Come eseguire il contenitore Cloud Docker Aspose.Cells.]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)

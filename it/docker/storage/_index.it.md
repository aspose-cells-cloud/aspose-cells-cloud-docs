---
title: Storag
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/docker/storage/
description: Come impostare la posizione di archiviazione su Aspose.Cells Cloud per Docker
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Archiviazione
---
##  Configurazione di archiviazione predefinita ##

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

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Documento di riferimento** : 
  - [Esecuzione Docker]( https://docs.docker.com/engine/reference/commandline/run/)

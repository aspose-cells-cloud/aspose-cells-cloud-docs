---
title: Storag
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/docker/storage/
description: So legen Sie die Speicherposition etwa Aspose.Cells Cloud für Docker fest
weight: 30
---
##  Standardspeicherkonfiguration ##

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

##  Grundposition ##


- **Fenster**

```powershell

c:\app\storageResource.json

```

- **Linux**

```linux

/app/storageResource.json


```

##  Benutzerdefinierte Speicherkonfiguration ##

Das Speicherprofil für die Cloud-Image-Datei Aspose.Cells muss neu angegeben werden, wenn der Kunde einen Speicherordner angibt.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Referenzdokument** : 
  - [Docker-Run]( https://docs.docker.com/engine/reference/commandline/run/)
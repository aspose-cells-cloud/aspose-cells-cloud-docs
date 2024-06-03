---
title: Lagerung
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/docker/storage/
description: So legen Sie die Speicherposition für Aspose.Cells Cloud für Docker fest
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Speicher
---
##  Standardmäßige Speicherkonfiguration ##

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

- **linux**

```linux

/app/storageResource.json


```

##  Benutzerdefinierte Speicherkonfiguration ##

Das Speicherprofil für die Cloud-Image-Datei Aspose.Cells muss erneut angegeben werden, wenn der Kunde einen Speicherordner angeben muss.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Referenzdokument** : 
  - [Docker-Ausführung]( https://docs.docker.com/engine/reference/commandline/run/)

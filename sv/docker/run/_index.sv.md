---
title: Ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/docker/run/
description: Hur man kör Aspose.Cells Cloud for Docker
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Run
---
## Exponera port

Hamn | Beskrivning | Nödvändig
---|:--:|---:
5000 | Mapp med typsnitt, som kommer att användas för att rendera dokument | Sann


##  Erforderliga volymer ##
Monteringsbana i container | Beskrivning | Nödvändig
---|:--:|---:
C:\fonts | Mapp med typsnitt, som kommer att användas för att rendera dokument | falsk
C:\data | Fillagringsmapp | falsk

##  Kör parametrar ##

Namn | Beskrivning | Nödvändig
---|:--:|---:
LicensePublicKey | Licensens offentliga nyckel | Sann
LicensPrivateKey | Licensens privata nyckel | Sann
lagringsuppgifterFilsökväg | Lagringskonfigurationsfilsökväg. Standardfilen är ./storageResource.json | Sann

##  Kör kommando ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}


**Referensdokument** : 
  - [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)

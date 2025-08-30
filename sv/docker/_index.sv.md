---
title: Docke
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells Moln
weight: 30
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Docker
---
## Aspose.Cells Molndocker

Aspose.Cells Cloud Image är tillgänglig för Linux, Microsoft, Windows 11 Pro, Microsoft, Windows Server 2016, Microsoft, Windows Server 2019, Microsoft, Windows Server 2022.

## API Referens - Aspose.Cells Cloud Docker

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## Exponera porten

Port | Beskrivning | Obligatorisk
---|:--:|---:
5000 | Mapp med teckensnitt, som kommer att användas för att rendera dokument | sant

##  Nödvändiga volymer ##

Monteringssökväg i container | Beskrivning | Obligatorisk
---|:--:|---:
C:\fonts | Mapp med teckensnitt, som kommer att användas för att rendera dokument | false
C:\data | Fillagringsmapp | falskt

##  Körparametrar ##

Namn | Beskrivning | Obligatoriskt
---|:--:|---:
LicensePublicKey | Licensens publika nyckel | true
LicensePrivateKey | Licensens privata nyckel | true
storagesCredentialsFilePath | Sökväg till konfigurationsfil för lagring. Standardfilen är ./storageResource.json | true

##  Kör kommando ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}

**Referensdokument** :

- [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)
-

se:

- [Nedladdningsinformation](/cells/sv/docker/downloads/)
- [Kör versionsinformation](/cells/sv//docker/tag-list/)
- [Lagringsinformation](/cells/sv/docker/storage/)

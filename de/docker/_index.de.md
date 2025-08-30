---
title: Docke
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells Cloud
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Docker
---
## Aspose.Cells Cloud Docker

Aspose.Cells Cloud Image ist verfügbar für Linux, Microsoft Windows 11 Pro, Microsoft Windows Server 2016, Microsoft Windows Server 2019, Microsoft Windows Server 2022.

## API Referenz - Aspose.Cells Cloud Docker

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## Port freigeben

Port | Beschreibung | Erforderlich
---|:--:|---:
5000 | Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden | true

##  Erforderliche Mengen ##

Mount-Pfad im Container | Beschreibung | Erforderlich
---|:--:|---:
C:\fonts | Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden | false
C:\data | Dateispeicherordner | false

##  Ausführungsparameter ##

Name | Beschreibung | Erforderlich
---|:--:|---:
LicensePublicKey | Öffentlicher Schlüssel der Lizenz | true
LicensePrivateKey | Privater Schlüssel der Lizenz | true
storagesCredentialsFilePath | Speicherkonfigurationsdateipfad. Standarddatei ist ./storageResource.json | true

##  Befehl ausführen ##

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

**Referenzdokument** :

- [Docker-Ausführung]( https://docs.docker.com/engine/reference/commandline/run/)
-

sehen:

- [Informationen zum Download](/cells/de/docker/downloads/)
- [Informationen zur Ausführungsversion](/cells/de//docker/tag-list/)
- [Speicherinformationen](/cells/de/docker/storage/)

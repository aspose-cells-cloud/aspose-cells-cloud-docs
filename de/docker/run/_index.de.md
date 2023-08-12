---
title: Ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/docker/run/
description: So führen Sie Aspose.Cells Cloud für Docker aus
weight: 30
---
## Port freigeben

Hafen | Beschreibung | Erforderlich
---|:--:|---:
5000 | Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden | WAHR


##  Erforderliche Mengen ##
Mountpfad im Container | Beschreibung | Erforderlich
---|:--:|---:
C:\fonts | Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden | FALSCH
C:\Daten | Dateispeicherordner | FALSCH

##  Laufparameter ##

Name | Beschreibung | Erforderlich
---|:--:|---:
LicensePublicKey | Öffentlicher Schlüssel der Lizenz | WAHR
LicensePrivateKey | Privater Schlüssel der Lizenz | WAHR
storagesCredentialsFilePath | Speicherkonfigurationsdateipfad. Die Standarddatei ist ./storageResource.json | WAHR

##  Führen Sie den Befehl aus ##

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


**Referenzdokument** : 
  - [Docker-Run]( https://docs.docker.com/engine/reference/commandline/run/)
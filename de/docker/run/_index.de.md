---
title: Ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/docker/run/
description: So führen Sie Aspose.Cells Cloud für Docker aus
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Ausführen
---
## Port freigeben

Port | Beschreibung | Erforderlich
---|:--:|---:
5000 | Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden | true


##  Erforderliche Mengen ##
Einhängepfad im Container | Beschreibung | Erforderlich
---|:--:|---:
C:\fonts | Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden | false
C:\data | Dateispeicherordner | false

##  Ausführungsparameter ##

Name | Beschreibung | Erforderlich
---|:--:|---:
LicensePublicKey | Öffentlicher Schlüssel der Lizenz | true
LicensePrivateKey | Privater Schlüssel der Lizenz | true
storagesCredentialsFilePath | Speicherkonfigurationsdateipfad. Standarddatei ist ./storageResource.json | true

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
  - [Docker-Ausführung]( https://docs.docker.com/engine/reference/commandline/run/)

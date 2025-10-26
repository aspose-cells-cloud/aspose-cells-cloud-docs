---
title: So führen Sie Aspose.Cells Cloud Docker Containe aus
second_title: Documen
ArticleTitle: How to run Aspose.Cells Cloud Docker Containe
linktitle: Container Ru
type: docs
url: /de/run-aspose-cells-cloud-docker-container/
description: So führen Sie Aspose.Cells Cloud Docker Container aus. Aspose.Cells Cloud Docker Container ist ein von Aspose bereitgestellter Containerdienst, der auf Docker basiert und es Ihnen ermöglicht, die Funktionen der Aspose.Cells Cloud API in lokalen oder privaten Cloud-Umgebungen bereitzustellen, ohne auf die öffentlichen Cloud-Dienste von Aspose angewiesen zu sein.
weight: 30
kwords: Excel Cloud-Docker-Container, Self-Cloud-Docker-Container, REST-Docker-Container, Tabellenkalkulation, PDF, CSV, Json, Markdown, Docker-Image, Docker-Container ausführen
---
## Führen Sie den Aspose.Cells Cloud Docker Container im Testmodus aus

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## Führen Sie den Cloud Docker Container Aspose.Cells im getakteten Abrechnungsmodus aus

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Führen Sie den Cloud Docker Container Aspose.Cells im Lizenzabrechnungsmodus aus

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```



## Referenzdokument

- [So konfigurieren Sie den Aspose.Cells Cloud Docker Container-Speicher.](https://docs.aspose.cloud/cells/docker/storage/)

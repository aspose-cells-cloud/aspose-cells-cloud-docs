---
title: Come eseguire Aspose.Cells Cloud Docker Container
second_title: Documen
ArticleTitle: How to run Aspose.Cells Cloud Docker Containe
linktitle: Contenitore Ru
type: docs
url: /it/run-aspose-cells-cloud-docker-container/
description: Come eseguire Aspose.Cells Cloud Docker Container. Aspose.Cells Cloud Docker Container è un servizio containerizzato fornito da Aspose basato su Docker, che consente di distribuire le funzionalità di Aspose.Cells Cloud API in ambienti cloud locali o privati senza fare affidamento sui servizi cloud pubblici di Aspose
weight: 30
kwords: Excel Contenitore Docker cloud, Contenitore Docker self-cloud, Contenitore Docker REST, Foglio di calcolo, PDF, CSV, Json, Markdown, Immagine Docker, Esegui contenitore Docker
---
## Esegui Aspose.Cells Cloud Docker Container in modalità di prova

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## Esegui Aspose.Cells Cloud Docker Container in modalità di fatturazione a consumo

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Esegui Aspose.Cells Cloud Docker Container in modalità di fatturazione della licenza

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```



## Documento di riferimento

- [Come configurare l'archiviazione del contenitore Cloud Docker Aspose.Cells.](https://docs.aspose.cloud/cells/docker/storage/)

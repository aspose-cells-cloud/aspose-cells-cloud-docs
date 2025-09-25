---
title: "How to run Aspose.Cells Cloud Docker Container"
second_title: "Document"
ArticleTitle: "How to run Aspose.Cells Cloud Docker Container"
linktitle: "Container Run"
type: docs
url: /run-aspose-cells-cloud-docker-container/
description: "How to run Aspose.Cells Cloud Docker Container"
weight: 30
kwords: Excel Cloud Docker Container, Self-Cloud Docker Container, REST Docker Container, Spreadsheet, PDF, CSV, Json, Markdown, Docker Image, Docker Container
---

## Run Aspose.Cells Cloud Docker Container in Trial Mode

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## Run Aspose.Cells Cloud Docker Container in Metered Billing Mode

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Run Aspose.Cells Cloud Docker Container in License Billing Mode

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Run Aspose.Cells Cloud Docker Container with access token

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000 -e AccessToken=ace8955d11cf82e9189ea349976da6f -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Reference Document

- [How to configure Aspose.Cells Cloud Docker Container storage.](https://docs.aspose.cloud/cells/docker/storage/)

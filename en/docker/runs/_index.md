---
title: "How to Run Aspose.Cells Cloud Docker Container"
second_title: "Document"
ArticleTitle: "How to Run Aspose.Cells Cloud Docker Container"
linktitle: "Container Run"
type: docs
url: /run-aspose-cells-cloud-docker-container/
description: "Learn how to launch Aspose.Cells Cloud in a Docker container on Windows Server 2022. Step‑by‑step commands for trial, metered‑billing, and license‑billing modes, plus prerequisites, storage setup, and health‑check examples."
weight: 30
keywords: "Aspose.Cells Cloud Docker, trial mode, metered billing, license billing, Docker run command, storage configuration, Windows Server 2022"
---

Aspose.Cells Cloud Docker provides a ready‑to‑run container image that hosts the Aspose.Cells Cloud API locally or in a private cloud. This guide shows how to start the container in three common licensing modes—**Trial**, **Metered Billing**, and **License Billing**—and includes a variant that uses an access token. All commands are written for PowerShell on Windows Server 2022; adapt the volume paths if you are using Linux.

## Run Aspose.Cells Cloud Docker Container in Trial Mode

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

The container runs in the foreground and listens on host port **47900**, which forwards to the container’s internal port **5000**.

## Run Aspose.Cells Cloud Docker Container in Metered Billing Mode

```powershell
# Windows Server 2022
# Metered‑billing mode: set LicensePublicKey and LicensePrivateKey as environment variables.
# Bind a storage folder (host → container)
#   -v c:/data:c:/data
# Bind the Windows fonts folder so the API can access system fonts
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

The container runs in detached mode (`-d`). After it starts, you can verify that the service is reachable:

```powershell
curl http://localhost:47900/v3.0/health
```

## Run Aspose.Cells Cloud Docker Container in License Billing Mode

```powershell
# Windows Server 2022
# License‑billing mode: provide a license file via the LicenseFile environment variable.
# Bind a storage folder (host → container)
#   -v c:/data:c:/data
# Bind the Windows fonts folder
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## Run Aspose.Cells Cloud Docker Container with Access Token

```powershell
# Windows Server 2022
# Access‑token mode: set AccessToken together with optional metered‑billing keys.
# Bind a storage folder
#   -v c:/data:c:/data
# Bind the Windows fonts folder
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

After starting the container, confirm the service is operational with the same health‑check command shown earlier.

## Reference Document

- [How to configure Aspose.Cells Cloud Docker Container storage.](https://docs.aspose.cloud/cells/docker/storage/)
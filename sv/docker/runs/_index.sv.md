---
title: Hur man kör Aspose.Cells Cloud Docker-behållaren
second_title: Documen
ArticleTitle: How to run Aspose.Cells Cloud Docker Containe
linktitle: Container Ru
type: docs
url: /sv/run-aspose-cells-cloud-docker-container/
description: "Så här kör du Aspose.Cells Cloud Docker Container. Aspose.Cells Cloud Docker Container är en containerbaserad tjänst som tillhandahålls av Aspose och är baserad på Docker, vilket gör att du kan distribuera funktionerna i Aspose.Cells Cloud API i lokala eller privata molnmiljöer utan att förlita dig på Aspose:s publika molntjänster."
weight: 30
kwords: Excel Cloud Docker-behållare, Self-Cloud Docker-behållare, REST Docker-behållare, kalkylblad, PDF, CSV, JSON, Markdown, Docker-avbildning, Run Docker-behållare
---
## Kör Aspose.Cells Cloud Docker Container i testläge

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## Kör Aspose.Cells Cloud Docker-behållaren i faktureringsläge med mätning

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Kör Aspose.Cells Cloud Docker-behållaren i licensfaktureringsläge

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```



## Referensdokument

- [Så här konfigurerar du Aspose.Cells Cloud Docker Container-lagring.](https://docs.aspose.cloud/cells/docker/storage/)

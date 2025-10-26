---
title: Comment exécuter Aspose.Cells Cloud Docker Containe
second_title: Documen
ArticleTitle: How to run Aspose.Cells Cloud Docker Containe
linktitle: Conteneur Ru
type: docs
url: /fr/run-aspose-cells-cloud-docker-container/
description: Comment exécuter Aspose.Cells Cloud Docker Container. Aspose.Cells Cloud Docker Container est un service conteneurisé fourni par Aspose qui est basé sur Docker, vous permettant de déployer les fonctionnalités du Aspose.Cells Cloud API dans des environnements cloud locaux ou privés sans dépendre des services cloud publics de Aspose
weight: 30
kwords: Excel Conteneur Docker Cloud, Conteneur Docker Cloud autonome, Conteneur Docker REST, Feuille de calcul, PDF, CSV, Json, Markdown, Image Docker, Exécuter le conteneur Docker
---
## Exécutez le conteneur Cloud Docker Aspose.Cells en mode d'essai

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## Exécutez le conteneur Cloud Docker Aspose.Cells en mode de facturation mesurée

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Exécutez le conteneur Cloud Docker Aspose.Cells en mode de facturation de licence

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```



## Document de référence

- [Comment configurer le stockage du conteneur Cloud Docker Aspose.Cells.](https://docs.aspose.cloud/cells/docker/storage/)

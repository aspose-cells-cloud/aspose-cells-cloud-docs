---
title: Cómo ejecutar Aspose.Cells Cloud Docker Container
second_title: Documen
ArticleTitle: How to run Aspose.Cells Cloud Docker Containe
linktitle: Contenedor Ru
type: docs
url: /es/run-aspose-cells-cloud-docker-container/
description: Cómo ejecutar Aspose.Cells Cloud Docker Container. Aspose.Cells Cloud Docker Container es un servicio en contenedores proporcionado por Aspose que se basa en Docker, lo que le permite implementar las funcionalidades de Aspose.Cells Cloud API en entornos de nube local o privada sin depender de los servicios de nube pública de Aspose.
weight: 30
kwords: Excel Contenedor Docker en la nube, contenedor Docker en la nube propia, contenedor Docker REST, hoja de cálculo, PDF, CSV, JSON, Markdown, imagen Docker, ejecutar contenedor Docker
---
## Ejecute Aspose.Cells Cloud Docker Container en modo de prueba

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## Ejecutar el contenedor Docker en la nube Aspose.Cells en modo de facturación medida

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Ejecute el contenedor Docker en la nube Aspose.Cells en modo de facturación de licencias

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```



## Documento de referencia

- [Cómo configurar el almacenamiento del contenedor Docker en la nube Aspose.Cells.](https://docs.aspose.cloud/cells/docker/storage/)

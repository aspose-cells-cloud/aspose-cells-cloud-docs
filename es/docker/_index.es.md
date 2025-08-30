---
title: Muelle
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells Nube
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Docker
---
## Aspose.Cells Nube Docker

La imagen de nube Aspose.Cells está disponible para Linux, Microsoft Windows 11 Pro, Microsoft Windows Server 2016, Microsoft Windows Server 2019, Microsoft Windows Server 2022.

## Referencia API - Aspose.Cells Cloud Docker

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## Puerto de exposición

Puerto | Descripción | Requerido
---|:--:|---:
5000 | Carpeta con fuentes que se usarán para renderizar documentos | verdadero

##  Volúmenes requeridos ##

Ruta de montaje en el contenedor | Descripción | Obligatorio
---|:--:|---:
C:\fonts | Carpeta con fuentes que se usarán para renderizar documentos | falso
C:\data | Carpeta de almacenamiento de archivos | falso

##  Parámetros de ejecución ##

Nombre | Descripción | Obligatorio
---|:--:|---:
LicensePublicKey | Clave pública de la licencia | verdadero
ClavePrivadaDeLicencia | Clave privada de la licencia | verdadero
storagesCredentialsFilePath | Ruta del archivo de configuración de almacenamiento. El archivo predeterminado es ./storageResource.json | true

##  Comando Ejecutar ##

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

**Documento de referencia** :

- [Ejecución de Docker]( https://docs.docker.com/engine/reference/commandline/run/)
-

ver:

- [Descargar información](/cells/es/docker/downloads/)
- [Información de la versión de ejecución](/cells/es//docker/tag-list/)
- [Información de almacenamiento](/cells/es/docker/storage/)

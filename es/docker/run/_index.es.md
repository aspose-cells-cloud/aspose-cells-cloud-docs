---
title: ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/docker/run/
description: Cómo ejecutar Aspose.Cells Cloud para Docker
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Ejecutar
---
## Exponer puerto

Puerto | Descripción | Requerido
---|:--:|---:
5000 | Carpeta con fuentes, que se utilizará para representar documentos | verdadero


##  Volúmenes requeridos ##
Montar ruta en contenedor | Descripción | Requerido
---|:--:|---:
C:\fuentes | Carpeta con fuentes, que se utilizará para representar documentos | FALSO
C:\datos | Carpeta de almacenamiento de archivos | FALSO

##  Ejecutar parámetros ##

Nombre | Descripción | Requerido
---|:--:|---:
LicenciaPublicKey | Clave pública de la licencia | verdadero
LicenciaClavePrivada | Clave privada de la licencia | verdadero
almacenamientosCredencialesFilePath | Ruta del archivo de configuración del almacenamiento. El archivo predeterminado es ./storageResource.json | verdadero

##  Ejecutar comando ##

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


**Documento de referencia** : 
  - [Ejecución de ventana acoplable]( https://docs.docker.com/engine/reference/commandline/run/)

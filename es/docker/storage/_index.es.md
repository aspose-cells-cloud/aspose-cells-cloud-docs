---
title: Almacenamiento
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/docker/storage/
description: Cómo configurar la posición de almacenamiento en Aspose.Cells Cloud for Docker
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Almacenamiento
---
##  Configuración de almacenamiento predeterminada ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

``` json

{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

``` json

{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}

```

{{< /tab >}}

{{< /tabs >}}

##  Posición predeterminada ##


- **ventanas**

```powershell

c:\app\storageResource.json

```

- **Linux**

```linux

/app/storageResource.json


```

##  Configuración de almacenamiento personalizada ##

Es necesario volver a especificar el perfil de almacenamiento para el archivo de imagen en la nube Aspose.Cells cuando el cliente necesita especificar la carpeta de almacenamiento.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Documento de referencia** : 
  - [Ejecución de Docker]( https://docs.docker.com/engine/reference/commandline/run/)

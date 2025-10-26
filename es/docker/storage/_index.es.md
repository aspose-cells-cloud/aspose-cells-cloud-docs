---
title: Cómo configurar la posición de almacenamiento para el contenedor de almacenamiento en la nube Aspose.Cells
second_title: Documen
ArticleTitle: Aspose.Cells Cloud Docker Container Storage Configuratio
linktitle: Almacenamiento en contenedores
type: docs
url: /es/docker/storage/
description: Cómo configurar la posición de almacenamiento para el contenedor Docker en la nube Aspose.Cells
weight: 30
kwords: Excel Contenedor Docker en la nube, contenedor Docker en la nube propia, contenedor Docker REST, hoja de cálculo, PDF, CSV, JSON, Markdown, imagen Docker, ejecutar contenedor Docker
---
## Configuración de almacenamiento predeterminada ##

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

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**Documento de referencia** :

- [Cómo ejecutar el contenedor Docker en la nube Aspose.Cells.]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)

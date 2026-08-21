---
title: "Cómo configurar la posición de almacenamiento para el contenedor Docker de Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Configuración del almacenamiento del contenedor Docker de Aspose.Cells Cloud"
linktitle: "Almacenamiento del contenedor"
type: docs
url: /docker/storage/
description: "Configure la ubicación de almacenamiento para contenedores Docker de Aspose.Cells Cloud mediante archivos JSON, PowerShell o Bash."
weight: 30
keywords: "Aspose.Cells, Docker, almacenamiento de contenedor, configuración JSON, PowerShell, Bash"
---

**Resumen**: Esta guía muestra cómo configurar la ubicación de almacenamiento para contenedores Docker de Aspose.Cells Cloud en Windows y Linux mediante archivos de configuración JSON y comandos `docker run`.

## Configuración predeterminada del almacenamiento ##

**Requisitos previos**: Asegúrese de tener instalado Docker Engine 20.10 o superior, contar con claves de licencia válidas de Aspose.Cells Cloud (`LicensePublicKey` y `LicensePrivateKey`), y que la carpeta del host que pretende utilizar como almacenamiento (por ejemplo, `c:/data` en Windows o `/data` en Linux) exista y tenga los permisos adecuados.

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "Primer almacenamiento",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Local": [
    {
      "Name": "Primer almacenamiento",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Ubicación predeterminada ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## Configuración personalizada del almacenamiento ##

Especifique un perfil de almacenamiento personalizado cuando necesite utilizar una carpeta distinta para los datos de Aspose.Cells Cloud.

```bash
docker run -d \
  -v c:/data:c:/data \   # montar carpeta del host como almacenamiento del contenedor
  -p 47900:5000 \        # asignar puerto de la API
  -e LicensePublicKey=suPublicKeyDeLicencia \
  -e LicensePrivateKey=suPrivateKeyDeLicencia \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Ejemplo para Linux*:

```bash
docker run -d \
  -v /data:/data \   # montar carpeta del host como almacenamiento del contenedor
  -p 47900:5000 \    # asignar puerto de la API
  -e LicensePublicKey=suPublicKeyDeLicencia \
  -e LicensePrivateKey=suPrivateKeyDeLicencia \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**Documento de referencia**:

- [Cómo ejecutar el contenedor Docker de Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Características del contenedor Docker](https://docs.aspose.cloud/cells/docker/container-features/)
- [Descarga de la imagen Docker de Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/download-image/)
- [Gestión de etiquetas de contenedor](https://docs.aspose.cloud/cells/docker/manage-tags/)
---
title: "Manual de operación de Aspose.Cells Cloud Docker: aloje la aplicación Aspose.Cells Cloud en su propia infraestructura privada."
second_title: "Documento"
ArticleTitle: "Manual de operación de Aspose.Cells Cloud Docker"
linktitle: "Docker"
type: docs
url: /es/docker-developer-guide/
aliases: [  /es/docker/ , /es/docker/run/ ]
description: "Implemente Aspose.Cells Cloud como contenedor Docker en una infraestructura privada o en instalaciones propias, lo que permite procesar hojas de cálculo (Excel, PDF, CSV, JSON, Markdown) sin usar la nube pública de Aspose."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Imagen Docker",
    "API de hojas de cálculo",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Nube privada",
    "Implementación",
  ]
weight: 30
---

Aspose.Cells Cloud es un servicio de procesamiento de hojas de cálculo basado en la nube que admite la creación, edición, conversión y manipulación de archivos en formatos como Excel. Puede configurarse rápidamente como un entorno de servicio independiente mediante implementación con Docker, simplificando la gestión de dependencias y los procesos de implementación multiplataforma.

Este manual proporciona una introducción detallada a todos los pasos operativos: desde la preparación del entorno hasta la verificación del servicio.

## Preparación del entorno

Antes de implementar el contenedor Docker de Aspose.Cells Cloud, asegúrese de que el entorno local cumpla con los siguientes requisitos de dependencias, para evitar fallos de implementación por componentes ausentes.

### Componentes básicos de dependencia

- **Motor Docker:** motor principal del entorno de ejecución de contenedores, responsable de crear y gestionar contenedores. La versión mínima requerida es la **18.09.0**.
- **Sistemas operativos:** sistemas operativos mainstream que admiten Docker

  | Tipo de sistema operativo | Versión                   |
  | :------------------------ | :------------------------ |
  | Windows                   | Windows 10/11             |
  | Windows Server            | 2016 / 2019 / 2022        |
  | Linux                     | CentOS 7+ / Ubuntu 20.04+ |

- **Recursos de hardware:** asegúrese de que el servicio se ejecute sin problemas para evitar bloqueos por falta de recursos.
  - CPU: 2 núcleos o más.
  - Memoria: 4 GB o más.
  - Disco: 10 GB de espacio libre.

### Condiciones previas clave

- **Licencia de Aspose:** registre una cuenta oficial de Aspose para obtener una licencia válida (puede solicitar una versión de prueba o adquirir una versión comercial). Sin licencia, la funcionalidad del servicio podría verse restringida. Consulte la página [Licencia](https://purchase.aspose.com/buy) para obtener más detalles.
- **Conectividad de red:** asegúrese de que el entorno de implementación pueda acceder a Docker Hub (para extraer imágenes).

## Obtención de la imagen Docker de Aspose.Cells Cloud

La imagen de Aspose.Cells Cloud está alojada en Docker Hub y puede extraerse directamente mediante el comando `docker pull`, sin necesidad de compilación manual.

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## Ejecución del contenedor Docker de Aspose.Cells Cloud

### Parámetros de ejecución

| Nombre                        | Descripción                                                                 | Observaciones                                                |
| ----------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------ |
| LicensePublicKey              | Establece la clave pública de la licencia cuando se usa el modo de facturación basado en medición. | Solo es efectivo si se adopta el modo de facturación basado en medición. |
| LicensePrivateKey             | Establece la clave privada de la licencia cuando se usa el modo de facturación basado en medición. | Solo es efectivo si se adopta el modo de facturación basado en medición. |
| storagesCredentialsFilePath   | Ruta al archivo de configuración de almacenamiento. El archivo predeterminado es `./storageResource.json`. |                                                              |
| LicenseFile                   | Establece el archivo de licencia cuando se usa el modo de facturación basado en archivo de licencia. | Solo es efectivo si se adopta el modo de facturación basado en archivo de licencia. |
| AccessToken                   | Token para acceder a la API.                                                | Si está vacío, no se requiere verificación de token.         |

### Comando de ejecución

Ejecutar el contenedor en modo de prueba es tan sencillo como esto:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Para una ejecución completa con todas las funciones, obtenga una [licencia basada en medición](https://purchase.aspose.com/faqs/licensing/metered/) y monte una carpeta del host para el almacenamiento de archivos. El comando de ejecución en este caso sería el siguiente:

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### Referencia de la API – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### Puertos expuestos

| Puerto | Descripción                                    | Obligatorio |
| ------ | ---------------------------------------------- | ----------- |
| 5000   | Carpeta con fuentes utilizadas para renderizar documentos | Sí          |

### Volúmenes obligatorios

| Ruta de montaje en el contenedor | Descripción                                    | Obligatorio | Observaciones                                                  |
| -------------------------------- | ---------------------------------------------- | ----------- | -------------------------------------------------------------- |
| C:\fonts                         | Carpeta con fuentes utilizadas para renderizar documentos | No          | Resuelve problemas de hojas de cálculo/Excel causados por fuentes ausentes. |
| C:\data                          | Carpeta de almacenamiento de archivos          | No          | Aumenta el espacio de almacenamiento para facilitar la gestión y el acceso a archivos. |

## Documentación de referencia

- [Funcionalidad principal del contenedor Docker de Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker-container-features/)
- [Cómo configurar el almacenamiento del contenedor Docker de Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/storage/)
- [Cómo ejecutar el contenedor Docker de Aspose.Cells Cloud](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
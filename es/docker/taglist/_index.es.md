---
title: "Etiquetas de imágenes Docker de Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Etiquetas de imágenes Docker de Aspose.Cells Cloud"
linktype: "Etiquetas de imagen"
type: docs
url: /docker/tag-list/
description: "Encuentre las etiquetas más recientes de imágenes Docker de Aspose.Cells Cloud para Windows Server (2016-2022) y Linux. Obtenga los comandos de extracción, detalles de arquitectura y notas de actualización en un solo lugar."
weight: 30
keywords:
  - "Etiquetas de imágenes Docker de Aspose.Cells Cloud"
  - "Comandos de extracción Docker"
  - "Etiquetas Docker para Windows Server"
  - "Etiquetas Docker para Linux"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud proporciona imágenes Docker listas para ejecutarse para Windows Server (2016, 2019, 2022) y Linux.  
Cada imagen lleva una **etiqueta** que identifica la versión del producto y el sistema operativo objetivo.  
Utilice las etiquetas que aparecen a continuación para extraer la imagen exacta que necesita, y consulte los ejemplos de extracción y ejecución adjuntos para una puesta en marcha rápida.

*Última actualización: 2026-07-01*

**Requisitos previos:** Asegúrese de tener instalado Docker Engine 20.10 o posterior y poseer una clave de licencia válida de Aspose.Cells Cloud. Las imágenes se han compilado para las versiones específicas de Windows Server indicadas o para Linux x64.

## Imágenes para Windows Server 2016 ##

Etiquetas | Arquitectura | Dockerfile | Observaciones
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile no publicado – consulte las [notas de la versión](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016) para obtener detalles de compilación. | No se prevé ninguna etiqueta posterior para Windows Server 2016; esta es la última versión publicada.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

Recursos adicionales: [Descarga Docker](/cells/docker/downloads/), [Notas de la versión](/cells/release-notes/), [Requisitos previos](/cells/docker/prerequisites/).  
Consulte la [Descripción general de Docker](/cells/docker/) para obtener información adicional.

## Imágenes para Windows Server 2019 ##

Etiquetas | Arquitectura | Dockerfile | Observaciones
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile no publicado – consulte las [notas de la versión](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019) para obtener detalles de compilación. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

Recursos adicionales: [Descarga Docker](/cells/docker/downloads/), [Notas de la versión](/cells/release-notes/), [Requisitos previos](/cells/docker/prerequisites/).  
Consulte la [Descripción general de Docker](/cells/docker/) para obtener información adicional.

## Imágenes para Windows Server 2022 ##

Etiquetas | Arquitectura | Dockerfile | Observaciones
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile no publicado – consulte las [notas de la versión](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022) para obtener detalles de compilación. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

Recursos adicionales: [Descarga Docker](/cells/docker/downloads/), [Notas de la versión](/cells/release-notes/), [Requisitos previos](/cells/docker/prerequisites/).  
Consulte la [Descripción general de Docker](/cells/docker/) para obtener información adicional.

## Imágenes para Linux ##

Etiquetas | Arquitectura | Dockerfile | Observaciones
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile no publicado – consulte las [notas de la versión](https://github.com/aspose-cells/dockerfiles/tree/main/linux) para obtener detalles de compilación. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

Recursos adicionales: [Descarga Docker](/cells/docker/downloads/), [Notas de la versión](/cells/release-notes/), [Requisitos previos](/cells/docker/prerequisites/).  
Consulte la [Descripción general de Docker](/cells/docker/) para obtener información adicional.

**Registro de cambios de versión**

Etiqueta | Cambios
---|---
`ltsc2016.23.5.0` | Versión final para Windows Server 2016; incluye parches de seguridad y mejoras de rendimiento.
`ltsc2019.25.10.0` | Actualizado a Aspose.Cells 25.10.0; agrega soporte para nuevas fórmulas y correcciones de errores.
`ltsc2022.25.10.0` | Idéntica a la etiqueta 2019, optimizada para el entorno de ejecución de Windows Server 2022.
`linux.25.10.0` | Imagen base de Linux con Aspose.Cells 25.10.0; incluye dependencias actualizadas y optimizaciones específicas para Linux.  
---
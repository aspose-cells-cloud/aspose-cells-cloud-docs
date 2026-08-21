---
title: "Funcionalidad principal de Aspose.Cells Cloud Docker: conversión de hojas de cálculo, fusión, división, protección, procesamiento de datos, y más."
second_title: "Documento"
ArticleTitle: "Funcionalidad principal de Aspose.Cells Cloud Docker"
linktitle: "Características"
type: docs
url: /docker-container-features/
description: "Ejecute la API de Aspose.Cells Cloud localmente con el contenedor Docker de Aspose.Cells Cloud: un servicio basado en Docker y empaquetado en contenedores que ofrece procesamiento completo de hojas de cálculo, privacidad y capacidad sin conexión, sin recurrir a la nube pública de Aspose."
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - Conversión de hojas de cálculo
  - Procesamiento de Excel
  - Exportación a PDF
  - Manejo de CSV
  - API REST
  - Servicio empaquetado en contenedores
  - Nube privada
  - Procesamiento sin conexión
---

## ¿Qué es el contenedor Docker de Aspose.Cells Cloud?

El contenedor Docker de Aspose.Cells Cloud es un servicio empaquetado en contenedores proporcionado por Aspose, basado en Docker, que le permite implementar las funcionalidades de la API de Aspose.Cells Cloud en entornos locales o en nubes privadas, sin depender de los servicios públicos en la nube de Aspose.

## ¿Por qué usar el contenedor Docker de Aspose.Cells Cloud?

El contenedor Docker de Aspose.Cells Cloud es un servicio potente para el procesamiento de hojas de cálculo, que admite:

### Funcionalidades principales

- Lectura y escritura de archivos de Excel (XLS, XLSX, CSV, ODS, etc.)
- Cálculo de fórmulas, gráficos, formato condicional, tablas dinámicas, etc.
- Conversión de formatos (por ejemplo, Excel a PDF, HTML, imágenes, etc.)
- Operaciones con celdas, configuración de estilos, gestión de hojas de cálculo, etc.

El contenedor Docker de Aspose.Cells Cloud encapsula estas funcionalidades como una API RESTful y las empaqueta en una imagen Docker, lo que le permite ejecutarla en su propia infraestructura.

### Ventajas principales

| Beneficios               | Descripción                                                                 |
| ---------------------- | --------------------------------------------------------------------------- |
| Privacidad y seguridad de los datos | Todo el procesamiento de archivos se realiza dentro de su red privada; no es necesario cargar datos en una nube de terceros. |
| Disponibilidad sin conexión | No depende de la nube pública de Aspose, por lo que es adecuado para entornos de intranet o aislados. |
| Escalabilidad            | Escalado horizontal sencillo mediante Docker/Kubernetes.                                    |
| API unificada            | Totalmente compatible con la API pública de Aspose.Cells Cloud; no requiere cambios en el código. |
| Control de licencia        | Admite dos tipos de autorización; elija la que mejor se adapte a su situación. |

## Cómo usar el contenedor Docker de Aspose.Cells Cloud

Consulte la guía del usuario: [Cómo usar el contenedor Docker de Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container).

**Requisitos previos**

- Motor Docker 20.10 o posterior instalado en la máquina anfitriona.  
- Un mínimo de 2 GB de RAM y 2 núcleos de CPU asignados al contenedor para cargas de trabajo típicas.  
- Archivo de licencia válido de Aspose.Cells Cloud (o token de acceso) colocado en un directorio que será montado dentro del contenedor.

**Inicio rápido**

1. Descargue la imagen Docker: `docker pull aspose/cells-cloud`.  
2. Ejecute el contenedor, montando los directorios de licencia y datos, por ejemplo:  
   ```bash
   docker run -d -p 8080:80 \
     -v /ruta/hacia/licencia:/app/license \
     -v /ruta/hacia/datos:/app/data \
     aspose/cells-cloud
   ```  
3. Acceda a la API REST en `http://localhost:8080/v3.0/`. Para obtener información detallada sobre el uso de la API, consulte la [referencia de la API de Aspose.Cells Cloud](https://docs.aspose.cloud/cells/api-reference/).

## Documentación de referencia

- [Cómo configurar el almacenamiento del contenedor Docker de Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/docker/storage/)
---
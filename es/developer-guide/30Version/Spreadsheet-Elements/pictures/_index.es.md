---
title: "Trabajar con imágenes de Excel"
second_title: "Documentos"
linktype: "Imágenes"
type: docs
url: /pictures/
aliases: [/working-with-pictures/]
keywords: "Excel, imagen, Aspose.Cells Cloud, API REST, manejo de imágenes, imágenes de Excel"
description: "Aprenda a recuperar, agregar, actualizar y eliminar imágenes en hojas de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye ejemplos de código en C#, Java, Python y más."
weight: 100
ArticleTitle: "Trabajar con imágenes de Excel – Documentación de Aspose.Cells Cloud"
---

## Trabajar con imágenes en un archivo de Excel

Esta guía explica cómo trabajar con **imágenes** (también llamadas gráficos) en hojas de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Cubre las operaciones principales relacionadas con imágenes: recuperación, adición, actualización y eliminación de imágenes de Excel, y le dirige hacia ejemplos detallados para cada tarea.

**Requisitos previos**: una cuenta de Aspose.Cells Cloud, una clave API válida y el SDK correspondiente instalado para el lenguaje elegido.

- [Cómo obtener una imagen en un formato específico desde una hoja de cálculo de Excel.](/cells/pictures/get/) – Recuperar una única imagen en el formato solicitado (PNG, JPEG, etc.) desde una hoja de cálculo.  
- [Cómo obtener toda la información de las imágenes desde una hoja de cálculo de Excel.](/cells/pictures/get-all/) | Listar metadatos de todas las imágenes contenidas en una hoja de cálculo.  
- [Cómo agregar una imagen a una hoja de cálculo de Excel.](/cells/pictures/add/) – Insertar una nueva imagen en una hoja de cálculo, especificando su posición y tamaño.  
- [Cómo actualizar una imagen específica desde una hoja de cálculo de Excel.](/cells/pictures/update/) – Modificar las propiedades (por ejemplo, dimensiones, posición) de una imagen existente.  
- [Cómo eliminar todas las imágenes de una hoja de cálculo de Excel.](/cells/pictures/clear/) – Eliminar todos los objetos de imagen de una hoja de cálculo en una única llamada.  
- [Cómo eliminar una imagen específica desde una hoja de cálculo de Excel.](/cells/pictures/delete/) – Eliminar una única imagen identificada por su índice.  

**Referencia de la API**

**Obtener una imagen en un formato específico**

| Método HTTP | Punto final | Parámetros obligatorios | Solicitud de ejemplo | Respuesta de ejemplo | Códigos de estado |
|-------------|-------------|-------------------------|----------------------|----------------------|-------------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (ruta), `sheetName` (ruta), `pictureIndex` (ruta), `format` (consulta) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | Datos binarios de imagen (PNG, JPEG, etc.) | 200 OK, 400 Solicitud incorrecta, 401 No autorizado, 404 No encontrado, 500 Error del servidor |

**Obtener toda la información de las imágenes**

| Método HTTP | Punto final | Parámetros obligatorios | Solicitud de ejemplo | Respuesta de ejemplo | Códigos de estado |
|-------------|-------------|-------------------------|----------------------|----------------------|-------------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (ruta), `sheetName` (ruta) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | Matriz JSON con metadatos de imágenes (índice, nombre, posición, tamaño) | 200 OK, 400, 401, 404, 500 |

**Agregar una imagen**

| Método HTTP | Punto final | Parámetros obligatorios | Cuerpo de solicitud de ejemplo | Respuesta de ejemplo | Códigos de estado |
|-------------|-------------|-------------------------|--------------------------------|----------------------|-------------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (ruta), `sheetName` (ruta) | `{ "image": "<imagen-codificada-en-base64>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Creado, 400, 401, 404, 500 |

**Actualizar una imagen**

| Método HTTP | Punto final | Parámetros obligatorios | Cuerpo de solicitud de ejemplo | Respuesta de ejemplo | Códigos de estado |
|-------------|-------------|-------------------------|--------------------------------|----------------------|-------------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (ruta), `sheetName` (ruta), `pictureIndex` (ruta) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**Eliminar todas las imágenes**

| Método HTTP | Punto final | Parámetros obligatorios | Solicitud de ejemplo | Respuesta de ejemplo | Códigos de estado |
|-------------|-------------|-------------------------|----------------------|----------------------|-------------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (ruta), `sheetName` (ruta) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "Todas las imágenes se han eliminado." }` | 200 OK, 400, 401, 404, 500 |

**Eliminar una imagen específica**

| Método HTTP | Punto final | Parámetros obligatorios | Solicitud de ejemplo | Respuesta de ejemplo | Códigos de estado |
|-------------|-------------|-------------------------|----------------------|----------------------|-------------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (ruta), `sheetName` (ruta), `pictureIndex` (ruta) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Imagen eliminada." }` | 200 OK, 400, 401, 404, 500 |

**Temas relacionados**

Explore otras operaciones relacionadas con imágenes en Aspose.Cells Cloud:  
- [Trabajar con formas](/cells/shapes/) – agregar, editar y eliminar formas gráficas.  
- [Trabajar con gráficos](/cells/charts/) – crear y manipular objetos de gráficos.  
- [Trabajar con imágenes en hojas de cálculo](/cells/images/) – incrustar y administrar archivos de imagen sin procesar.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Trabajar con imágenes de Excel – Documentación de Aspose.Cells Cloud",
  "description": "Guía para recuperar, agregar, actualizar y eliminar imágenes de Excel mediante la API REST de Aspose.Cells Cloud.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "imágenes de Excel, Aspose.Cells Cloud, API REST, manejo de imágenes",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>
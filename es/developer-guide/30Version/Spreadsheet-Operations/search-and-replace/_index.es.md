---
title: "Buscar y reemplazar contenido de texto en archivos de Excel"
second_title: "Documentación"
linktitle: "Buscar y reemplazar"
type: docs
url: /search-and-replace/
aliases: [/working-with-text/, /text/]
description: "Aprenda cómo buscar y reemplazar texto en libros y hojas de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye el formato de solicitud, código de ejemplo para .NET, Java, Python y manejo de errores."
keywords: "Aspose.Cells Cloud, Excel, buscar y reemplazar, API REST, .NET, Java, Python"
weight: 20
ArticleTitle: "Buscar y reemplazar texto en archivos de Excel mediante la API de Aspose.Cells Cloud"
---

Las operaciones de texto son procesos complejos para los archivos de Excel. Muchos factores contribuyen a esta complejidad y deben considerarse durante el procesamiento. Aspose.Cells Cloud proporciona una forma confiable para buscar y reemplazar texto en una amplia variedad de formatos de hojas de cálculo.

Trabajar con texto en libros de Excel a menudo requiere localizar cadenas específicas y actualizarlas en varias hojas. La API de Aspose.Cells Cloud simplifica esta tarea al proporcionar una operación unificada de **búsqueda y reemplazo** que funciona con cualquier formato de hoja de cálculo admitido.

## Resumen

Buscar y reemplazar le permite localizar cadenas específicas en un libro o en una hoja de cálculo particular y sustituirlas por nuevos valores. La operación funciona con todos los formatos admitidos por Aspose.Cells Cloud, como **XLS, XLSX, XLSM, XLSB, ODS, CSV** y otros. Utilizando la función de **búsqueda y reemplazo**, puede limpiar rápidamente datos, corregir errores tipográficos repetidos o aplicar convenciones de nomenclatura masivas en todo un libro.

## Requisitos previos

- Una cuenta activa de Aspose.Cloud con un **Client‑Id** y un **Client‑Secret** válidos.
- Token de acceso obtenido mediante el flujo de autenticación OAuth 2.0.
- El libro de trabajo objetivo debe estar almacenado en el almacenamiento de Aspose Cloud o ser accesible mediante una URL pública.
- SDK necesario instalado (por ejemplo, Aspose.Cells‑Cloud para .NET, Java o Python).

## Referencia de la API

**Método:** `POST`  
**Punto de conexión**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| Parámetro        | Tipo    | Obligatorio | Descripción                                                                       |
| ---------------- | ------- | ----------- | --------------------------------------------------------------------------------- |
| `fileName`       | string  | Sí          | Nombre del libro de trabajo (incluida la extensión).                             |
| `folder`         | string  | No          | Ruta de la carpeta en el almacenamiento en la nube.                              |
| `storage`        | string  | No          | Nombre del almacenamiento, si no es el predeterminado.                           |
| `sheetName`      | string  | No          | Nombre de la hoja de cálculo específica; si se omite, la operación aplica al libro completo. |
| `searchString`   | string  | Sí          | Texto que se va a buscar.                                                         |
| `replaceString`  | string  | Sí          | Texto con el que se reemplazarán las ocurrencias encontradas.                    |
| `ignoreCase`     | boolean | No          | Establecer en `true` para realizar una búsqueda que no distinga entre mayúsculas y minúsculas. |
| `matchWholeCell` | boolean | No          | Establecer en `true` para reemplazar solo coincidencias de celdas completas.    |

**Encabezados**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**Cuerpo de la solicitud (JSON)**

```json
{
  "searchString": "ValorAntiguo",
  "replaceString": "ValorNuevo",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Hoja1"
}
```

**Respuesta correcta (JSON)**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## Formatos admitidos

| Formato                               | Extensión                 |
| ------------------------------------- | ------------------------- |
| Libro de trabajo de Excel             | .xls, .xlsx, .xlsm, .xlsb |
| Hoja de cálculo OpenDocument          | .ods                      |
| CSV                                   | .csv                      |
| Otros (según lo admitido por Aspose.Cells) | —                         |

## Ejemplos de código

A continuación se presentan ejemplos mínimos para tres SDK populares. Reemplace `{clientId}`, `{clientSecret}` y otros marcadores de posición con sus valores reales. Estos ejemplos demuestran cómo realizar una operación de **búsqueda y reemplazo** mediante programación.

## Manejo de errores y casos extremos

| Código HTTP | Significado                                           | Acción recomendada                                                   |
| ----------- | ----------------------------------------------------- | -------------------------------------------------------------------- |
| 400         | Solicitud incorrecta: faltan o son inválidos los parámetros | Verifique los campos obligatorios y los tipos de datos.            |
| 401         | No autorizado: token inválido o caducado             | Actualice el token de acceso.                                       |
| 404         | No encontrado: el libro o la hoja de cálculo no existe | Verifique el nombre del archivo, la ruta de la carpeta y `sheetName`. |
| 415         | Tipo de medio no admitido: formato de archivo inválido | Asegúrese de que el archivo cargado esté en un formato de Excel o CSV admitido. |
| 202         | Aceptado: solicitud aceptada para procesamiento      | Consulte el estado de la operación si se utiliza procesamiento asíncrono. |
| 204         | Sin contenido: operación correcta sin cuerpo         | Se aplicó el reemplazo; no se devolvió información adicional.     |
| 500         | Error interno del servidor: fallo inesperado         | Reintente tras un breve retraso; contacte con el soporte de Aspose si el problema persiste. |

**Notas:**  
- Los libros grandes podrían exceder los límites de tamaño de solicitud; considere cargar primero el archivo en el almacenamiento en la nube.  
- Cuando `ignoreCase` se establece en `true`, tenga en cuenta que los mapeos de mayúsculas/minúsculas según la configuración regional pueden afectar los resultados.  
- Usar `matchWholeCell` con fórmulas no reemplazará coincidencias parciales dentro del texto de la fórmula.

## Búsqueda y reemplazo en archivos de Excel

- [Cómo obtener elementos de texto de un libro de trabajo de Excel.](/cells/workbook/get-text-items/)  
- [Cómo obtener elementos de texto de una hoja de cálculo de Excel.](/cells/worksheets/get-text-items/)  
- [Cómo buscar texto en un libro de trabajo de Excel.](/cells/workbook/find-text/)  
- [Cómo buscar texto en una hoja de cálculo de Excel.](/cells/worksheets/find-text/)  
- [Cómo buscar texto en archivos de Excel sin cargar un archivo.](/cells/search/)  
- [Cómo reemplazar texto en un libro de trabajo de Excel.](/cells/workbook/replace-text/)  
- [Cómo reemplazar texto en una hoja de cálculo de Excel.](/cells/worksheets/replace-text/)  
- [Cómo reemplazar texto en archivos de Excel sin cargar un archivo.](/cells/replace/)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Buscar y reemplazar texto en archivos de Excel mediante la API de Aspose.Cells Cloud",
  "description": "Documentación sobre el punto de conexión de búsqueda y reemplazo de Aspose.Cells Cloud, incluido el formato de solicitud, parámetros, ejemplos y manejo de errores.",
  "url": "https://docs.aspose.cloud/cells/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, buscar y reemplazar, API, REST"
}
</script>
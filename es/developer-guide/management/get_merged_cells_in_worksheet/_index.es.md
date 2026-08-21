---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "Obtener celdas fusionadas en hoja de cálculo – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "GetMergedCellsInWorksheet"
type: docs
url: /es/cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, celdas fusionadas, hoja de cálculo, API"
description: "Obtener todas las áreas de celdas fusionadas de una hoja de cálculo local."
weight: 1000
---

## El método Get Merged Cells In Worksheet de Aspose.Cells Cloud Web Services

Obtiene todas las áreas de celdas fusionadas de una hoja de cálculo local.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | File | FormData | Cargar archivo de hoja de cálculo. |
| worksheet | String | Query | Nombre de la hoja de cálculo. |
| region | String | Query | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password | String | Query | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------- | ---- | ----------- |
| N/A | N/A | Esta operación no acepta un cuerpo JSON; el archivo de hoja de cálculo se envía mediante `multipart/form-data`. |

### **Respuesta**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|------|---------|-------------|
| 200 | OK | Áreas de celdas fusionadas recuperadas correctamente. |
| 400 | Solicitud incorrecta | Uno o más parámetros de solicitud no son válidos o faltan. |
| 401 | No autorizado | La autenticación falló: token JWT no válido o ausente. |
| 413 | Carga útil demasiado grande | El archivo de hoja de cálculo cargado supera el límite de tamaño permitido. |
| 500 | Error interno del servidor | Se produjo un error inesperado en el servidor. |

## Cómo usar Get Merged Cells In Worksheet con SDK

### Especificación de Get Merged Cells In Worksheet

La [Especificación de la API Get Merged Cells In Worksheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Usar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Hoja1&region=es-ES&password=MiContraseña" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'Spreadsheet=@ejemplo.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
 `[TBD]`
---
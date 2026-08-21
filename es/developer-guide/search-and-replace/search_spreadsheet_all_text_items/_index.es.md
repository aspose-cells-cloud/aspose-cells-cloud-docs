---
title: "Buscar todos los elementos de texto en una hoja de cálculo"
ArticleTitle: "Buscar todos los elementos de texto en una hoja de cálculo – Aspose.Cells Cloud API"
second_title: "Documentos"
linktype: "docs"
url: /es/cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, Búsqueda, Elementos de texto, API"
description: "Buscar todos los elementos de texto dentro de un archivo de hoja de cálculo utilizando la API de Aspose.Cells Cloud."
weight: 100
---

## Búsqueda de todos los elementos de texto en una hoja de cálculo mediante los servicios web de Aspose.Cells Cloud

Este método busca todos los elementos de texto dentro de un archivo local de hoja de cálculo. Admite la búsqueda en todas las hojas y celdas del libro, identificando las apariciones del término buscado. La operación se realiza del lado del servicio en la nube y no requiere almacenamiento en la nube. Asegúrese de tener los permisos necesarios para leer el archivo de origen. Si el archivo de origen no puede accederse o se produce un error durante el proceso de búsqueda (por ejemplo, un formato de archivo no admitido), se lanzará una excepción adecuada. Según los detalles de la implementación, el método podría devolver las ubicaciones de las coincidencias (por ejemplo, nombre de la hoja, coordenadas de la celda).

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|------|----------------------------------------|-------------|
| Spreadsheet | Archivo | FormData | Cargar archivo de hoja de cálculo. |
| region | Cadena | Query | Configuración regional o de idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta al formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password | Cadena | Query | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Respuesta**

```json
{
  "SearchResults": [
    {
      "SheetName": "Hoja1",
      "CellName": "A1",
      "Text": "Texto de ejemplo"
    }
    // ... más elementos
  ],
  "TotalCount": 42
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | La solicitud se completó correctamente y la respuesta contiene todos los elementos de texto encontrados. |
| 400 | Solicitud incorrecta | URL no válida o parámetros de solicitud mal formados. |
| 401 | No autorizado | La autenticación ha fallado o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible. |
| 413 | Carga demasiado grande | El archivo cargado excede el límite de tamaño permitido. |
| 500 | Error interno del servidor | Se ha producido una anomalia en la obtención de datos de la hoja de cálculo. |

## Cómo utilizar la función de búsqueda de todos los elementos de texto en una hoja de cálculo con SDK

### Especificación de la búsqueda de todos los elementos de texto en una hoja de cálculo

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems}" rel="noopener noreferrer">Especificación de la API de Búsqueda de todos los elementos de texto en una hoja de cálculo</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilice HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=es-ES&password=miContraseña" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F "Spreadsheet=@ejemplo.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "SearchResults": [
    {
      "SheetName": "Hoja1",
      "CellName": "A1",
      "Text": "Texto de ejemplo"
    }
    // ... más elementos
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstrae los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
 `[TBD]`
---
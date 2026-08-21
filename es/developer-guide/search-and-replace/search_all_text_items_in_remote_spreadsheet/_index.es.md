---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "SearchAllTextItemsInRemoteSpreadsheet"
type: docs
url: /es/cells/{name}/search/content/all-textitems
aliases: []
keywords: "búsqueda, elementos de texto, Aspose.Cells"
description: "Buscar todos los elementos de texto en una hoja de cálculo remota mediante Aspose.Cells Cloud."
weight: 100
---

## El método SearchAllTextItemsInRemoteSpreadsheet de los servicios web de Aspose.Cells Cloud

Este método busca todos los elementos de texto dentro de un archivo de hoja de cálculo remoto. Admite la búsqueda en todas las hojas y celdas del libro, identificando las ocurrencias del término buscado. La operación se realiza en la nube, sin requerir almacenamiento local. Asegúrese de tener los permisos necesarios para leer el archivo de origen. Si no se puede acceder al archivo de origen o si ocurre un error durante el proceso de búsqueda (por ejemplo, un formato de archivo no admitido), se lanzará una excepción adecuada. El método puede devolver las ubicaciones de las coincidencias (por ejemplo, nombre de la hoja, coordenadas de la celda), según los detalles de la implementación.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|--------|------------------------------------------|-------------|
| name                 | string | Ruta                                     | Nombre del archivo del libro. |
| folder               | string | Cadena de consulta                       | Ruta de la carpeta donde se almacena el libro. |
| storageName          | string | Cadena de consulta                       | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Utilice el almacenamiento predeterminado si se omite. |
| region               | string | Cadena de consulta                       | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | string | Cadena de consulta                       | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| [TBD]                |      | [TBD]       |

### **Respuesta**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | La solicitud se realizó correctamente y la respuesta contiene todos los elementos de texto encontrados en la hoja de cálculo. |
| 400 | Solicitud incorrecta | URL o parámetros de solicitud no válidos. |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible. |
| 413 | Carga útil demasiado grande | La carga útil de la solicitud excede el tamaño permitido. |
| 500 | Error interno del servidor | El libro ha encontrado una anomalía al obtener los datos. |

## Cómo utilizar SearchAllTextItemsInRemoteSpreadsheet con SDK

### Especificación de SearchAllTextItemsInRemoteSpreadsheet

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet" rel="noopener noreferrer">Especificación de la API SearchAllTextItemsInRemoteSpreadsheet</a> define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilice HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Hoja1",
      "CellAddress": "A1",
      "Text": "Texto de ejemplo"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud mediante diversos SDK:
`[TBD]`
---
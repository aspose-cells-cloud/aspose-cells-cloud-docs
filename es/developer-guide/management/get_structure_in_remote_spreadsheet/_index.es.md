---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Get Structure In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "GetStructureInRemoteSpreadsheet"
type: docs
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, spreadsheet, structure"
description: "Recuperar los metadatos estructurales de un libro de Excel remoto, incluyendo hojas de cálculo, tablas, tablas dinámicas, gráficos, formas y otra información fundamental."
weight: 100
---

## La operación Get Structure In Remote Spreadsheet de los Servicios Web de Aspose.Cells Cloud

Convertir estructuralmente los metadatos fundamentales, hojas de cálculo, tablas, tablas dinámicas, gráficos, formas y otra información de un libro de Excel en un objeto JSON de tipo JObject, para escenarios como la exportación de datos, respuestas de API y registro de registros.

### Punto de acceso de la API web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|------|-------------------------------------|-------------|
| name | string | Ruta | Nombre del archivo de hoja de cálculo. |
| folder | string | Consulta | Carpeta donde se encuentra el archivo. (Opcional) |
| storageName | string | Consulta | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Se utiliza el almacenamiento predeterminado si se omite. |
| region | string | Consulta | Configuración regional/lingüística de la hoja de cálculo (por ejemplo, `en-US`, `fr-FR`). Influye en el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password | string | Consulta | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Respuesta**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**Códigos de estado de la respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | Estructura del libro recuperada correctamente. |
| 400 | Solicitud incorrecta | Parámetros de solicitud inválidos. |
| 401 | No autorizado | Falló la autenticación o falta el token. |
| 413 | Carga útil demasiado grande | El cuerpo de la solicitud excede el tamaño permitido. |
| 500 | Error interno del servidor | Error inesperado en el servidor. |

## Cómo utilizar Get Structure In Remote Spreadsheet con SDKs

### Especificación de Get Structure In Remote Spreadsheet

La [especificación de la API Get Structure In Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose Cells Cloud utilizando diversos SDK:
`[TBD]`
---
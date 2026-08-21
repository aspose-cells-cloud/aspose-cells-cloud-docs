---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "GetSpreadsheetStructure"
type: docs
url: /cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, Estructura de hoja de cálculo, API"
description: "Convierte estructuralmente los metadatos principales, hojas de cálculo, tablas, tablas dinámicas, gráficos, formas y otra información de un libro de Excel en un objeto JSON de tipo JObject."
weight: 1000
---

## GetSpreadsheetStructure de los Servicios Web de Aspose.Cells Cloud

Convierte estructuralmente los metadatos principales, hojas de cálculo, tablas, tablas dinámicas, gráficos, formas y otra información de un libro de Excel en un objeto JSON de tipo JObject, para escenarios como la exportación de datos, respuestas de API y registro de registros.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|--------|--------------------------------------|-------------|
| Spreadsheet          | File   | FormData (cuerpo)                    | Cargar archivo de hoja de cálculo. |
| region               | String | Query                                | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Query                                | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| Spreadsheet          | File | Cargar archivo de hoja de cálculo. |

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
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**Códigos de estado de la respuesta**

| Código | Significado              | Descripción |
|--------|--------------------------|-------------|
| 200    | OK                       | Se recuperó correctamente la estructura de la hoja de cálculo. |
| 400    | Solicitud incorrecta     | Parámetros de solicitud inválidos o formato de archivo incorrecto. |
| 401    | No autorizado            | Falló la autenticación o falta el token JWT. |
| 413    | Carga demasiado grande    | El archivo cargado excede el límite de tamaño permitido. |
| 500    | Error interno del servidor | Se produjo un error inesperado en el servidor. |

## Cómo usar GetSpreadsheetStructure con SDK

### Especificación de GetSpreadsheetStructure

La [Especificación de la API GetSpreadsheetStructure](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=es-ES&password=yourPassword" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@ejemplo.xlsx'
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
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud mediante diversos SDK:
`[TBD]`
---
---
title: "Convertir tabla en tabla dinámica"
second_title: "Documentos"
linktype: Convertir
type: docs
url: /pivot-tables/convert-table-to-pivottable/
aliases:
  [
    /create-a-pivottable-with-table/,
    /create-new-pivot-table-with-list-object-as-source-data/,
  ]
keywords: "tabla dinámica, objeto de lista, Aspose.Cells Cloud, API REST, convertir tabla en tabla dinámica"
description: "Aprenda cómo crear una tabla dinámica a partir de un objeto de lista utilizando la API REST de Aspose.Cells Cloud. Incluye detalles de la solicitud, ejemplo de cURL y referencias a SDK."
weight: 60
ArticleTitle: "Convertir tabla en tabla dinámica – Documentación de Aspose.Cells Cloud"
---

Esta API REST crea una **tabla dinámica** a partir de un objeto de lista.

Una tabla dinámica resume datos de un objeto de lista, permitiéndole analizar e informar sobre grandes conjuntos de datos directamente dentro del libro.

**Prerrequisitos:**
- Un token JWT portador válido para autenticación.
- El libro debe existir en la ubicación de almacenamiento especificada.
- La hoja de cálculo de destino debe contener el objeto de lista que desea resumir.

## API PostWorksheetListObjectSummarizeWithPivotTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                |
|----------------------|---------|-----------|--------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro.              |
| sheetName            | string  | path      | Hoja de cálculo que contiene el objeto de lista. |
| listObjectIndex      | integer | path      | Índice del objeto de lista dentro de la hoja de cálculo. |
| destsheetName        | string  | query     | Nombre de la hoja de cálculo de destino.   |
| request              | object  | body      | Carga útil JSON que define la tabla dinámica. |
| folder               | string  | query     | Ruta de carpeta donde se encuentra el libro. |
| storageName          | string  | query     | Nombre del almacenamiento.                 |

El cuerpo de la solicitud debe seguir el esquema JSON definido a continuación:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Nombre de la nueva tabla dinámica." },
    "DestCellName": { "type": "string", "description": "Celda superior izquierda de la tabla dinámica (por ejemplo, \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Índices basados en cero de los campos que se colocarán en filas."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Índices basados en cero de los campos que se colocarán en columnas."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Índices basados en cero de los campos que se usarán como campos de datos."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

La <a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*Nota: Utilice el punto de acceso de producción (`api.aspose.cloud`) en entornos en vivo. El punto de acceso de QA (`api-qa.aspose.cloud`) está destinado únicamente a pruebas. Se requiere HTTPS para todas las llamadas de producción.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Códigos de estado HTTP**

| Código | Significado                   | Descripción                                                 |
|--------|-------------------------------|-------------------------------------------------------------|
| 200    | OK                            | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta          | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                 | Token JWT inválido o ausente.                               |
| 413    | Payload demasiado grande       | El archivo subido excede el límite de tamaño.               |
| 500    | Error interno del servidor    | Error inesperado en el servidor.                            |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:
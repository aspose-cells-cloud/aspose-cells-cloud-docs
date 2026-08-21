---
title: "Importar datos JSON en Excel"
second_title: "Documento"
linktitle: "Importar JSON"
type: docs
url: /es/import-json-data-into-excel/
aliases: [  /es/import/json/ ]
keywords: "Aspose.Cells Cloud, importación JSON, API de Excel, importación REST de JSON, ejemplos de SDK"
description: "Aprenda cómo importar datos JSON en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye detalles del punto de conexión, ejemplos de solicitud y respuesta, y código de SDK para .NET, Java y Python."
weight: 40
---

Esta **API REST importa datos JSON** en una hoja de cálculo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro    | Ubicación     | Tipo   | Descripción                                                                                          |
| ----------------------- | ------------- | ------ | ---------------------------------------------------------------------------------------------------- |
| name                    | Ruta          | string | Nombre del archivo del libro de cálculo.                                                             |
| importJsonRequest       | Cuerpo HTTP   | clase  | Carga útil de la solicitud que contiene los detalles de la importación JSON.                        |
| password                | Cadena de consulta | string | Contraseña para abrir el libro de cálculo (si está protegido).                                       |
| folder                  | Cadena de consulta | string | Carpeta que contiene el libro de cálculo original.                                                  |
| storageName             | Cadena de consulta | string | Nombre del almacenamiento donde reside el libro de cálculo.                                         |
| outPath                 | Cadena de consulta | string | Ruta del archivo de salida tras la importación. Si se omite, el libro de cálculo actualizado se devuelve en la respuesta. |
| outStorageName          | Cadena de consulta | string | Nombre del almacenamiento para el archivo de salida.                                                |
| checkExcelRestriction   | Cadena de consulta | string | Indicador que especifica si se deben aplicar restricciones específicas de Excel (true/false).      |

### **Ejemplo de cuerpo de solicitud**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### Respuesta

Una solicitud correcta devuelve **HTTP 200** con una carga útil JSON similar a:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Códigos de estado posibles:

| Código | Significado                              |
| ------ | ---------------------------------------- |
| 200    | Importación realizada correctamente     |
| 400    | Solicitud incorrecta: faltan o son inválidos los datos |
| 401    | No autorizado: token inválido o ausente  |
| 500    | Error interno del servidor               |


## Cómo utilizar la API PostWorkbookImportJson con SDK

### Especificación de la API PostWorkbookImportJson

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. Los SDK gestionan los detalles de bajo nivel, permitiéndole centrarse en la lógica de su negocio. Para obtener una lista completa de los SDK de Aspose.Cells Cloud, visite el [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

---
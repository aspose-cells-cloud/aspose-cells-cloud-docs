---
title: Aspose.Cells Cloud Web API - Reemplazar el contenido de la hoja de cálculo en una hoja de cálculo remota
second_title: Documen
ArticleTitle: Replace Worksheet Content in Remote a Spreadshee
linktitle: Reemplazar el contenido de la hoja de trabajo remota
type: docs
url: /es/replace-content-in-remote-worksheet/
keywords: Aspose.Cells Cloud Web API, Replace Content, Remote Worksheet, Cloud Spreadsheet, Text Replacement, Office Cloud Integratio
description: Reemplace texto de manera eficiente en la hoja de cálculo de una hoja de cálculo remota utilizando Aspose.Cells API
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel, ReplaceContentInRemoteWorksheet
---
Reemplace de manera eficiente el texto especificado dentro de una hoja de cálculo de un archivo de hoja de cálculo remoto.

## **Reemplazar contenido en la hoja de trabajo remota API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| nombre| Cadena| Camino| El nombre del archivo del libro de trabajo que se va a modificar.|
| hoja de trabajo| Cadena| Camino| Especifique la hoja de trabajo para el reemplazo.|
| buscarTexto| Cadena| Consulta| El texto a buscar en la hoja de trabajo.|
| reemplazarTexto| Cadena| Consulta| El texto con el que se reemplazará el texto buscado.|
| carpeta| Cadena| Consulta| La ruta de la carpeta donde se almacena el libro de trabajo.|
| nombreDeAlmacenamiento| Cadena| Consulta|(Opcional) El nombre del almacenamiento si se usa almacenamiento en la nube personalizado. Si se omite, utilice el almacenamiento predeterminado.|
| región| Cadena| Consulta| La configuración de la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo.|

### **Respuesta**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Dónde debemos utilizar el contenido Reemplazar de la hoja de trabajo en la hoja de cálculo remota API?

Cuando necesite reemplazar el contenido de una hoja de trabajo en una hoja de cálculo remota, puede usar este API.

## ¿Por qué debería utilizar Reemplazar contenido de la hoja de trabajo en la hoja de cálculo remota API?

- Reemplace rápidamente el contenido de la hoja de trabajo en hojas de cálculo remotas.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la función Reemplazar contenido de la hoja de cálculo en la hoja de cálculo remota API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteWorksheet) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite reemplazar el contenido de la hoja de cálculo en celdas con un mínimo de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web Aspose.Cells utilizando varios SDK:

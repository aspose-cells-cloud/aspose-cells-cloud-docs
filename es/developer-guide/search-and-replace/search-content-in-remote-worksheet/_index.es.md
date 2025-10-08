---
title: Aspose.Cells Cloud Web API - Buscar contenido de la hoja de cálculo en una hoja de cálculo remota
second_title: Documen
ArticleTitle: Search Worksheet Content in Remote Spreadshee
linktitle: Buscar contenido de la hoja de trabajo remota
type: docs
url: /es/search-content-in-remote-worksheet/
keywords: Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet AP
description: Busque texto de manera eficiente dentro de una hoja de cálculo remota almacenada en la nube
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel, Búsqueda remota en hojas de cálculo
---
Busque texto específico dentro de una hoja de cálculo de una hoja de cálculo remota almacenada en el almacenamiento en la nube.

## **Detalles de la interfaz**

## **Buscar contenido en la hoja de trabajo remota**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|nombre|Cadena|Camino|El nombre del archivo del libro de trabajo que se buscará.|
|hoja de trabajo|Cadena|Camino|El nombre de la hoja de trabajo.|
|buscarTexto|Cadena|Consulta|El texto a buscar.|
|ignorandoCase|Booleano|Consulta|Indica si se deben ignorar mayúsculas y minúsculas durante la búsqueda.|
|carpeta|Cadena|Consulta|La ruta de la carpeta donde se almacena el libro de trabajo.|
|nombreDeAlmacenamiento|Cadena|Consulta|(Opcional) El nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Si se omite, se utiliza el almacenamiento predeterminado.|
|región|Cadena|Consulta|La configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|La contraseña para abrir el archivo de hoja de cálculo.|

### **Respuesta**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
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

## ¿Dónde debemos utilizar el contenido de búsqueda dentro de la hoja de cálculo API?

Cuando necesite buscar contenido dentro de la hoja de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar la función de búsqueda de contenido dentro de la hoja de cálculo API?

- Busque contenido sin esfuerzo dentro de una hoja de cálculo remota con este API.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la búsqueda de enlaces rotos dentro de la hoja de cálculo API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) define una interfaz de programación de acceso público y permite interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente la búsqueda de contenido en las celdas de las hojas de cálculo con un código mínimo.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web Aspose.Cells utilizando varios SDK:

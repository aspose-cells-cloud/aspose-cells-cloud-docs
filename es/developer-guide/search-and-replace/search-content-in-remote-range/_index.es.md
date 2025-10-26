---
title: Aspose.Cells Cloud Web API - Buscar contenido de rango en hoja de cálculo remota
second_title: Documen
ArticleTitle: Search Range Content in Remote Spreadshee
linktitle: Buscar contenido de rango remoto
type: docs
url: /es/search-content-in-remote-range/
keywords: Excel API, Remote Spreadsheet Search, Cloud Storage, Data Retrieval, Spreadsheet Search, Text Search AP
description: Busque texto de manera eficiente dentro de un rango específico de una hoja de cálculo remota almacenada en la nube usando Excel API
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, Búsqueda de texto, JSON, CSV, PDF, Markdown, Coincidir en blanco Cells en Excel
---
Busque texto específico dentro de un rango de una hoja de cálculo remota.

## **Buscar contenido en el rango remoto API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|nombre|Cadena|Camino|El nombre del archivo de hoja de cálculo.|
|hoja de trabajo|Cadena|Camino|El nombre de la hoja de trabajo.|
|área de celda|Cadena|Camino|El rango de celdas dentro del cual se realizará la búsqueda.|
|buscarTexto|Cadena|Consulta|El texto a buscar.|
|ignorandoCase|Booleano|Consulta|Especifique si la búsqueda debe ignorar la distinción entre mayúsculas y minúsculas.|
|carpeta|Cadena|Consulta|La carpeta en la que se almacena el archivo.|
|nombreDeAlmacenamiento|Cadena|Consulta|(Opcional) El nombre del almacenamiento si se usa almacenamiento en la nube personalizado. Si se omite, utilice el almacenamiento predeterminado.|
|regresar|Cadena|Consulta|La configuración de la región de la hoja de cálculo.|
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

## ¿Dónde debemos utilizar el contenido de búsqueda dentro del rango de la hoja de cálculo API?

Cuando necesite buscar contenido dentro del rango de la hoja de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar la función de búsqueda de contenido dentro del rango de la hoja de cálculo API?

- Busque contenido sin esfuerzo dentro de un rango de hoja de cálculo remota con este API.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la búsqueda de enlaces rotos dentro del rango de la hoja de cálculo API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteRange) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente la búsqueda de contenido dentro del rango de celdas de las hojas de cálculo con un código mínimo.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}

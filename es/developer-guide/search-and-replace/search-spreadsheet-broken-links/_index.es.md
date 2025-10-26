---
title: Aspose.Cells Cloud Web API - Buscar enlaces rotos en una hoja de cálculo
second_title: Documen
ArticleTitle: Search Spreadsheet Broken Links in a Spreadshee
linktitle: Hoja de cálculo de búsqueda Enlace roto
type: docs
url: /es/search-spreadsheet-broken-links/
keywords: search broken links, spreadsheet API, Excel broken links, REST API, Office Cloud integratio
description: Busque de manera eficiente enlaces rotos en hojas de cálculo locales utilizando Excel API
weight: 100
kwords: Excel API, buscar enlaces rotos, Office Nube, REST API, Gestión de hojas de cálculo, PDF, CSV, JSON, Markdown, identificar enlaces rotos, reparar hipervínculo
---
Busque enlaces rotos dentro de hojas de cálculo locales.

## **Buscar hoja de cálculo Enlaces rotos API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/broken-links
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo que se va a analizar.|
|hoja de trabajo|Cadena|Consulta|Especifique la hoja de trabajo para el examen.|
|área de celda|Cadena|Consulta|Define el área de la celda para el análisis.|
|región|Cadena|Consulta|Establecer la configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|Proporcione la contraseña para acceder al archivo de hoja de cálculo.|

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

## ¿Dónde debemos utilizar la búsqueda de enlaces rotos dentro de la hoja de cálculo API?

Cuando necesite buscar enlaces rotos dentro de la hoja de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar la búsqueda de enlaces rotos dentro de la hoja de cálculo API?

- Busque sin esfuerzo enlaces rotos dentro de una hoja de cálculo remota con este API.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la búsqueda de enlaces rotos en la hoja de cálculo API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks) define una interfaz de programación de acceso público que le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente la búsqueda de enlaces rotos en celdas de hojas de cálculo con un mínimo de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{< /tab >}}
{{< /tabs >}}

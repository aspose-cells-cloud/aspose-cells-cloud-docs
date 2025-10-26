---
title: Aspose.Cells Cloud Web API - Buscar enlaces rotos de rango en hoja de cálculo remota
second_title: Documen
ArticleTitle: Search Broken Links of Range in Remote a Spreadshee
linktitle: Buscar rango remoto Enlace roto
type: docs
url: /es/search-broken-links-in-remote-range/
keywords: broken links, remote spreadsheet, Excel API, REST API, link checker, hyperlink validation, cloud storag
description: Busque de manera eficiente enlaces rotos dentro de un rango específico de una hoja de cálculo remota almacenada en la nube
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, enlaces rotos, validación de hipervínculos, almacenamiento en la nube
---
Busque de forma eficiente enlaces rotos dentro de un rango específico de una hoja de cálculo remota almacenada en la nube.

## **Buscar enlaces rotos en el rango remoto API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| nombre| Cadena| Camino| El nombre del archivo del libro de trabajo que se va a buscar.|
| hoja de trabajo| Cadena| Camino| Especifique la hoja de trabajo para la búsqueda.|
| área de celda| Cadena| Camino| Especifique el área de celda para la búsqueda.|
| carpeta| Cadena| Consulta| La ruta de la carpeta donde se almacena el libro de trabajo.|
| nombreDeAlmacenamiento| Cadena| Consulta|(Opcional) El nombre del almacenamiento si se usa almacenamiento en la nube personalizado. Si se omite, utilice el almacenamiento predeterminado.|
| región| Cadena| Consulta| La configuración de la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo.|

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

## ¿Dónde debemos utilizar la búsqueda de enlaces rotos dentro del rango de la hoja de cálculo API?

Cuando necesite buscar enlaces rotos dentro del rango de la hoja de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar la búsqueda de enlaces rotos dentro del rango de la hoja de cálculo API?

- Busque rápidamente enlaces rotos dentro del rango de la hoja de cálculo.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la búsqueda de enlaces rotos dentro del rango de la hoja de cálculo API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchBrokenLinksInRemoteRange) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente la búsqueda de celdas dentro del rango de hojas de cálculo con un mínimo de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}

---
title: Obtener la versión del archivo
second_title: Documen
linktitle: Obtener la versión del archivo
type: docs
url: /es/get-file-versions/
keywords: file versions, Excel API, Office Cloud, REST API, spreadsheet management, document histor
description: Recupere y administre las versiones de los archivos almacenados en la nube Aspose.Cells, mejorando la gestión y colaboración de documentos
weight: 100
kwords: Obtener versiones de archivos, Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, gestión de documentos
---
## **Excel API: Obtener versiones de archivos**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Descripción de la función**

 El**Obtener versiones de archivos** API permite a los usuarios recuperar las diferentes versiones de un archivo específico almacenado en la nube Aspose.Cells. Esta funcionalidad es crucial para mantener la integridad del documento y rastrear los cambios a lo largo del tiempo.

###  Los parámetros de solicitud de**Obtener versiones de archivos** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| camino| Cadena| Camino| La ruta al archivo del que se recuperarán las versiones.|
| nombreDeAlmacenamiento| Cadena| Consulta| El nombre del almacenamiento donde se encuentra el archivo.|

### **Descripción de la respuesta**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)Proporciona una interfaz de programación integral para ejecutar interacciones REST directamente desde un navegador web.

## Excel API SDK

 El uso de un SDK optimiza el desarrollo al abstraer las complejidades de bajo nivel, lo que permite a los desarrolladores centrarse en las funcionalidades principales. Explore[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web Aspose.Cells en varios lenguajes de programación:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{< /tab >}}
{{< /tabs >}}

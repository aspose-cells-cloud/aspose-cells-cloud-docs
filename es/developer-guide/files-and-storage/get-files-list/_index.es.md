---
title: Obtener lista de archivos - Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: Obtener lista de archivos
type: docs
url: /es/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: Aprenda a recuperar una lista de archivos de una carpeta específica usando Aspose.Cells API. Esta guía proporciona detalles sobre los parámetros de solicitud, la estructura de respuesta y ejemplos de código en varios lenguajes de programación.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Gestión de archivos en la nube, Obtener lista de archivos
---
## **Excel API: Obtener lista de archivos**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Descripción de la función**

 El**obtenerListaDeArchivos**API permite a los usuarios recuperar una lista completa de archivos y carpetas dentro de un directorio específico en el almacenamiento en la nube Aspose.Cells. Este punto final es crucial para la gestión eficiente de archivos y admite diversos formatos de archivo.

###  Los parámetros de solicitud de**obtenerListaDeArchivos** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| camino| Cadena| Camino| La ruta a la carpeta en el almacenamiento en la nube desde donde recuperar la lista de archivos.|
| nombreDeAlmacenamiento| Cadena| Consulta| El nombre del almacenamiento al que acceder.|

### **Descripción de la respuesta**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) define una interfaz de programación de acceso público que permite interacciones REST directamente desde un navegador web, lo que facilita la integración y las pruebas.

## Excel API SDK

 Utilizar un SDK es la mejor manera de acelerar su proceso de desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite concentrarse en las tareas de su proyecto. Para obtener una lista completa de los SDK en la nube Aspose.Cells, visite[Repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código ilustran cómo invocar los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}

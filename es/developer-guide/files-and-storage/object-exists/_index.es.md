---
title: El objeto existe
second_title: Documen
linktitle: El objeto existe
type: docs
url: /es/object-exists/
keywords: Excel API, Object Exists, REST API, Aspose, File Management, Excel, Office Cloud, Spreadsheet, PDF, CSV, JSON, Markdow
description: El objeto existe API comprueba si existe un archivo o carpeta especificado en el almacenamiento en la nube Aspose.Cells
weight: 100
kwords: Excel API, Objeto existente, REST API, Aspose, Office Nube, Gestión de archivos, Hoja de cálculo, PDF, CSV, JSON, Markdown, Comprobar existencia de archivo en Excel
---
## **Excel API: El objeto existe**

```
GET http://api.aspose.cloud/v4.0/cells/storage/exist/{path}
```

### **Descripción de la función**

El `objectExists` API permite a los desarrolladores verificar la existencia de un archivo o carpeta específicos dentro del almacenamiento en la nube Aspose.Cells.

###  Los parámetros de solicitud de**objectExiste** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|camino|Cadena|Camino|La ruta al archivo o carpeta en el almacenamiento en la nube.|
|nombreDeAlmacenamiento|Cadena|Consulta|El nombre del almacenamiento donde se encuentra el archivo.|
|ID de versión|Cadena|Consulta|El ID de la versión del archivo (si corresponde).|

### **Descripción de la respuesta**

```json
{
  "Name": "ObjectExist",
  "Description": [
    "Object exists"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates that the file or folder exists."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    },
    {
      "Name": "IsFolder",
      "Description": [
        "True if it is a folder, false if it is a file."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

## Excel API SDK

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ObjectExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ObjectExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ObjectExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ObjectExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ObjectExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ObjectExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ObjectExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ObjectExists.go" >}}
{{< /tab >}}
{{< /tabs >}}

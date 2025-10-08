---
title: Almacenamiento existente
second_title: Documen
linktitle: Almacenamiento existente
type: docs
url: /es/storage-exists/
keywords: Excel API, Storage Exists, REST API, Office Cloud, Cloud Storage, Excel Worksheet, Check Storage, Data Management, API Integratio
description: Aprenda a comprobar si existe almacenamiento mediante el REST Aspose.Cells API. Esta guía proporciona información detallada del punto final API, parámetros de solicitud y descripciones de respuesta.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel
---
## **Excel API : Existe almacenamiento**

```
GET http://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Descripción de la función**

 El**almacenamientoExiste**API comprueba si existe un almacenamiento específico en el servicio en la nube Aspose.Cells. Esta función es fundamental para garantizar que todas las operaciones que dependen del almacenamiento se realicen sin errores.

###  Los parámetros de solicitud de**almacenamientoExiste** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|nombreDeAlmacenamiento|Cadena|Camino|El nombre del almacenamiento cuya existencia se comprobará.|

### **Descripción de la respuesta**

```json
{
  "Name": "StorageExist",
  "Description": [
    "Indicates whether the specified storage exists."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
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

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/StorageExists) define una interfaz de programación de acceso público, que permite a los desarrolladores interactuar sin problemas con REST API directamente desde un navegador web.

## Excel API SDK

 Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. Un SDK abstrae los detalles de implementación de bajo nivel, lo que permite a los desarrolladores concentrarse en las tareas de su proyecto. Para obtener una lista completa de los SDK en la nube Aspose.Cells disponibles, visite[Repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código demuestran cómo realizar llamadas API a servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}

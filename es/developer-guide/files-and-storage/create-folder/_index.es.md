---
title: Crear carpeta en Excel AP
second_title: Developer Guide for Aspose.Cell
linktitle: Crear carpeta
type: docs
url: /es/create-folder/
keywords: Excel API, Create Folder, Office Cloud, REST API, Cloud Storage, Folder Management, Excel, Spreadsheet, PDF, CSV, JSON, Markdow
description: Aprenda a crear una carpeta en Excel API usando REST
weight: 100
kwords: Crear carpeta, Excel API, Office Nube, REST API, Almacenamiento en la nube, Administración de carpetas, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel
---
## **Excel API: Crear carpeta**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Descripción de la función**

 El**crearCarpeta** API permite a los usuarios crear una nueva carpeta en la ruta especificada dentro del almacenamiento en la nube de Excel API. Esta funcionalidad es esencial para organizar archivos y mantener un directorio estructurado.

###  Los parámetros de solicitud de**crearCarpeta** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|----------|--|------------------------|---------------------------------|
| camino| Cadena| Camino| La ruta donde se creará la carpeta.|
| nombreDeAlmacenamiento| Cadena| Consulta| El nombre del almacenamiento a utilizar.|

### **Descripción de la respuesta**

```json
{
Void
}
```

## Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

## Excel API SDK

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}

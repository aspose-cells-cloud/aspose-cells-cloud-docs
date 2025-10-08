---
title: Copiar carpeta
second_title: Documen
linktitle: Copiar carpeta
type: docs
url: /es/copy-folder/
keywords: Excel API, Copy Folder, Office Cloud, REST API, Spreadsheet Management, File Operation
description: Aprenda a utilizar CopyFolder API para copiar carpetas de manera eficiente en el entorno de nube Aspose.Cells
weight: 100
kwords: Excel, Office Nube, REST API, Copiar carpeta, Gestión de archivos, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel
---
## **Excel API: Copiar carpeta**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Descripción de la función**

 El**Copiar carpeta**API permite a los usuarios duplicar una carpeta existente en el almacenamiento en la nube Aspose.Cells. Esta función es esencial para gestionar archivos eficientemente, ya que permite a los usuarios crear copias de seguridad u organizar su trabajo sin tener que transferir el contenido manualmente.

###  Los parámetros de solicitud de la**Copiar carpeta** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|----------------|--|-----------------------|-------------------------------------|
| ruta_origen| Cadena| Camino| La ruta de la carpeta de origen a copiar.|
| ruta de destino| Cadena| Consulta| La ruta donde se creará la nueva carpeta.|
| nombreDeAlmacenamientoOrigen| Cadena| Consulta| El nombre del almacenamiento que contiene la carpeta de origen.|
| nombreDeAlmacenamientoDeDestino| Cadena| Consulta| El nombre del almacenamiento de destino donde se debe copiar la carpeta.|

### **Descripción de la respuesta**

```json
{
Void
}
```

## Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

## Excel API SDK

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}

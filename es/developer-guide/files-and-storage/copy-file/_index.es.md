---
title: Copiar archivo - Excel AP
second_title: Documen
linktitle: Copiar archivo
type: docs
url: /es/copy-file/
keywords: Excel API, Office Cloud, REST API, Spreadsheet Copy, PDF Conversion, CSV Export, JSON Handling, Markdown Support, Copy Excel File, Match Blank Cell
description: Aprenda a utilizar CopyFile API para Excel para duplicar eficientemente hojas de cálculo y manejar varios formatos de archivo.
weight: 100
kwords: Excel API, Office Nube, REST API, Copia de hoja de cálculo, Conversión PDF, Exportación CSV, Manejo de JSON, Compatibilidad con Markdown, Copiar archivo Excel, Coincidir con celda en blanco
---
## **Excel API: Copiar archivo**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Descripción de la función**

 El**Copiar archivo** API permite a los usuarios duplicar un archivo Excel desde una ruta de origen especificada a una ruta de destino, admitiendo varias opciones de almacenamiento.

###  Los parámetros de solicitud de**Copiar archivo** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|-------------- ||--------------------- |-------------------------------------- |
| ruta_origen| Cadena| Camino| La ruta de origen del archivo que se va a copiar.|
| ruta de destino| Cadena| Consulta| La ruta de destino donde se guardará el archivo.|
| nombreDeAlmacenamientoOrigen| Cadena| Consulta| El nombre del almacenamiento de origen.|
| nombreDeAlmacenamientoDeDestino| Cadena| Consulta| El nombre del almacenamiento de destino.|
| ID de versión| Cadena| Consulta| ID de versión opcional del archivo a copiar.|

### **Descripción de la respuesta**

```json
{
Void
}
```

## Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FileController/CopyFile) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

## Excel API SDK

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{< /tab >}}
{{< /tabs >}}

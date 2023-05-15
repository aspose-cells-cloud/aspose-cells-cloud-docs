---
title: Objeto existente
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/storage/object-exists/
keywords: Learn how to check object exist with Aspose Cells Cloud REST API
description: Aprenda a verificar la existencia de objetos con Aspose Cells Cloud REST API SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 100
---
Este REST API indica verificar si `file or folder exists`.
 
## RESET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino| Ruta de archivo o carpeta, por ejemplo, '/archivo.ext' o '/carpeta'|
| NombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|
| versiónId| cadena| consulta| Id. de la versión del archivo|

 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Exists": true,
  "IsFolder": false
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Familia SDK de la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
 
 
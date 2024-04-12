---
title: Copiar archivo
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/file/copy/
keywords: Learn how to copy file with Aspose Cells Cloud REST API
description: Aprenda a copiar archivos con Aspose Cells Cloud REST API SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 100
---
Este REST API indica `copy file`.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| srcPath| cadena| camino| Ruta del archivo fuente, por ejemplo, '/carpeta/archivo.ext'|
| rutadestino| cadena| consulta| Ruta del archivo de destino|
| srcNombreAlmacenamiento| cadena| consulta| Nombre del almacenamiento de origen|
| nombredealmacenamientodestino| cadena| consulta| Nombre del almacenamiento de destino|
| ID de versión| cadena| consulta|ID de versión del archivo para copiar|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/File/CopyFile) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Familia de SDK en la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:
 
 
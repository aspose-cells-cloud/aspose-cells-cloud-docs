---
title: División por lotes
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API admite archivos divididos por lotes. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 100
---
Este REST API indica al `batch split` de expediente elegible.
 
## RESET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| Solicitud de división por lotes|| cuerpo||

**Propiedades de BatchSplitRequest**
 
Nombre | Tipo | Descripción | notas
------------ | ------------- | ------------- | -------------
 Carpeta de origen | cadena | | [opcional]Almacenamiento de origen | cadena | | [opcional]Condición de coincidencia | Solicitud de condición de coincidencia | | [opcional]Formato | cadena | | [opcional]FromIndex | entero | | [opcional]ToIndex | entero | | [opcional]Carpeta de salida | cadena | | [opcional]GuardarOpciones | GuardarOpciones | | [opcional]**Propiedades de MatchConditionRequest**
 
Nombre | Tipo | Descripción | notas
------------ | ------------- | ------------- | -------------
 RegexPatrón | cadena | | [opcional]Condiciones de coincidencia completa | cadena[]| | [opcional] El[Especificación de API abierta](https://reference.aspose.cloud/cells/#/Batch/PostBatchsplit) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
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
 
## Familia SDK de la nube
 
Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en sus tareas divididas. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
 
 
  
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< tab tabNum="10" >}}


{{< /tab >}}

{{< /tabs >}}


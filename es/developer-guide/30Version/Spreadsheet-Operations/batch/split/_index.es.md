---
title: División por lotes
second_title: Documen
type: docs
url: /es/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API admite la división de archivos por lotes. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, División por lotes
---
Este REST API indica el `batch split` del archivo elegible.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| Solicitud de división por lotes|| cuerpo||

**Propiedades de BatchSplitRequest**

Nombre | Tipo | Descripción | Notas
------------ | ------------- | ------------- | -------------
 CarpetaOrigen | cadena | | [opcional]AlmacenamientoOrigen | cadena | | [opcional]CondiciónDeCoincidencia | SolicitudDeCondiciónDeCoincidencia | | [opcional]Formato | cadena | | [opcional]DesdeÍndice | entero | | [opcional]HastaÍndice | entero | | [opcional]CarpetaDeSalida | cadena | | [opcional]OpcionesDeGuardado | OpcionesDeGuardado | | [opcional]**Propiedades de MatchConditionRequest**

Nombre | Tipo | Descripción | Notas
------------ | ------------- | ------------- | -------------
 RegexPattern | cadena | | [opcional]FullMatchConditions | cadena[]| | [opcional]El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

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

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y te permite concentrarte en tus tareas divididas. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

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

{{< /tabs >}}

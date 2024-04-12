---
title: Protección por lotes
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/batch/protect
keywords: Batch protection of multiple Excel files
description: Aspose.Cells Cloud API admite la protección por lotes de múltiples archivos de Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 100
---
Este REST API indica el `batch protection` de archivos elegibles.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/protect
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| solicitud de protección por lotes|| cuerpo||

**Propiedades de solicitud de protección por lotes**
 
Nombre | Tipo | Descripción | Notas
------------ | ------------- | ------------- | -------------
Carpeta de origen | cadena | | [opcional]Condición de coincidencia | Solicitud de condición de coincidencia | | [opcional]Tipo de protección | cadena | | [opcional]Contraseña | cadena | | [opcional]Carpeta exterior | cadena | | [opcional]**Propiedades de MatchConditionRequest**
 
Nombre | Tipo | Descripción | Notas
------------ | ------------- | ------------- | -------------
 Patrón de expresión regular | cadena | | [opcional]Condiciones de coincidencia completa | cadena[]| | [opcional]El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/PostProtectConvert) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}" 
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


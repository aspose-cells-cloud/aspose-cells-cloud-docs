---
title:  Ordenar rango
second_title: Aspose.Cells Cloud Documen
linktitle: Sor
type: docs
keywords: Range Sort
url: /es/ranges/sort/
description:  Establece el borde del contorno alrededor de un rango de celdas.
weight: 20
---
Este REST API indica clasificación de rango.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

 Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|nombre|Cadena|Camino|El nombre del libro de trabajo.|
|nombre de la hoja|Cadena|Camino|El nombre de la hoja de trabajo.|
|rangoOperar|Clase|Cuerpo| Solicitud de clasificación de rango|
|carpeta|Cadena|Consulta|Carpeta del libro de trabajo original.|
|nombredealmacenamiento|Cadena|Consulta|Nombre del almacenamiento.|



 El[Especificación de API abierta](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Consulte el repositorio de GitHub para obtener una lista completa de Aspose.Cells SDK de nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:


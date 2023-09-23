---
title:  Segmentación de inserción de objetos de lista
second_title: Aspose.Cells Cloud Documen
linktitle: Insertar rebanada
type: docs
keywords: Insert slicer for list object
url: /es/list-objects/insert-slicer/
description:  Insertar segmentación para el objeto de lista.
weight: 20
---
 Este REST API indica insertar segmentación para el objeto de lista en una hoja de trabajo Excel.

## RSET API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer

```

 Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|nombre|Cadena|Camino||
|nombre de la hoja|Cadena|Camino||
|lista de índice de objetos|Entero|Camino||
|columnaÍndice|Entero|Consulta||
|destCellName|Cadena|Consulta||
|carpeta|Cadena|Consulta||
|nombredealmacenamiento|Cadena|Consulta||



 El[Especificación de API abierta](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectInsertSlicer) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
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

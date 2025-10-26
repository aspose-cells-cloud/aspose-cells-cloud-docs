---
title: Mover archivo
second_title: Documen
linktitle: Mover archivo
type: docs
url: /es/move-file/
keywords: Move file, Aspose.Cells API, File Management, Excel API, REST API, Cloud Storage, Spreadsheet Manipulatio
description: Aprenda a usar MoveFile API para administrar archivos en el almacenamiento en la nube Aspose.Cells
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Mover archivo, Gestión de archivos, Almacenamiento en la nube
---
## **Excel API: Mover archivo**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Descripción de la función**

 El**moverArchivo** API permite mover un archivo de una ubicación a otra dentro del almacenamiento en la nube Aspose.Cells. Esto resulta especialmente útil para organizar archivos y gestionar el almacenamiento eficazmente.

###  Los parámetros de solicitud de**moverArchivo** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|---------------|--|------------------------|--------------------------------------|
| ruta_origen| Cadena| Camino| La ruta de origen del archivo que se va a mover.|
| ruta de destino| Cadena| Consulta| La ruta de destino donde se moverá el archivo.|
| nombreDeAlmacenamientoOrigen| Cadena| Consulta| El nombre del almacenamiento de origen, si corresponde.|
| nombreDeAlmacenamientoDeDestino| Cadena| Consulta|El nombre del almacenamiento de destino, si corresponde.|
| ID de versión| Cadena| Consulta| El ID de la versión del archivo, si corresponde.|

### **Descripción de la respuesta**

```json
{
Void
}
```

## Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FileController/MoveFile) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

## Excel API SDK

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

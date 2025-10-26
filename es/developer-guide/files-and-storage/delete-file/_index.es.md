---
title: Eliminar archivo - Excel AP
second_title: Documen
linktitle: Eliminar archivo
type: docs
url: /es/delete-file/
keywords: Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usag
description: Aprenda a eliminar archivos en Excel con Aspose.Cells API. Esta guía proporciona información detallada sobre el punto final deleteFile API, los parámetros de solicitud y la estructura de respuesta.
weight: 100
kwords: Eliminar archivo, Excel API, REST API, Office Nube, Gestión de hojas de cálculo, Eliminación de archivos, Almacenamiento en la nube, API usag
---
## **Excel API : Eliminar archivo**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Descripción de la función**

 El**eliminarArchivo** API permite a los usuarios eliminar archivos específicos del almacenamiento en la nube, lo que garantiza una gestión eficiente de los recursos y los datos.

###  Los parámetros de solicitud para el**eliminarArchivo** API son

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|camino|Cadena|Camino|La ruta al archivo que necesita eliminarse.|
|nombreDeAlmacenamiento|Cadena|Consulta|El nombre del almacenamiento donde se encuentra el archivo. Opcional si se utiliza el almacenamiento predeterminado.|
|ID de versión|Cadena|Consulta|El ID de la versión del archivo a eliminar, si corresponde.|

### **Descripción de la respuesta**

```json
{
Void
}
```

## Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

## Excel API SDK

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

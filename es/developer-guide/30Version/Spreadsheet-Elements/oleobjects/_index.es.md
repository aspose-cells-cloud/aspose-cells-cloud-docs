---
---
title: "Trabajar con objetos OLE de Excel"
second_title: "Documento"
linktitle: "OleObjects"
type: docs
url: /oleobjects/
aliases: [/working-with-oleobjects/]
keywords: "OLE, Excel, Aspose.Cells, API, Cloud"
description: "Utilice la API REST de Aspose.Cells Cloud para recuperar, agregar, actualizar, eliminar y convertir objetos OLE en hojas de cálculo de Excel. Los SDK están disponibles para Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift y Android."
weight: 100
ArticleTitle: "Trabajar con objetos OLE de Excel – Guía para recuperar, agregar, actualizar, eliminar y convertir objetos OLE"
---

**Cómo trabajar con objetos OLE en una hoja de cálculo de Excel**

La API REST de Aspose.Cells Cloud proporciona un conjunto completo de operaciones para gestionar objetos OLE de forma programática. A continuación se presenta una referencia concisa para cada operación, incluyendo el método HTTP, el patrón de punto final, los parámetros requeridos y un ejemplo breve de respuesta.

- [Cómo obtener un objeto OLE de una hoja de cálculo de Excel](/cells/oleobjects/get/)
  - **Método:** `GET`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parámetros:** `fileName` (cadena), `sheetName` (cadena), `oleObjectIndex` (entero)  
  - **Ejemplo de respuesta:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [Cómo agregar un objeto OLE en una hoja de cálculo de Excel](/cells/oleobjects/add/)
  - **Método:** `POST`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parámetros:** `fileName`, `sheetName`, `oleObject` (binario o en base64), `imageFormat` (opcional)  
  - **Ejemplo de cuerpo de solicitud:** multipart/form-data con el flujo del archivo.  
  - **Ejemplo de respuesta:** `201 Created` con el encabezado de ubicación del nuevo objeto OLE.

- [Cómo actualizar un objeto OLE específico en una hoja de cálculo de Excel](/cells/oleobjects/update/)
  - **Método:** `PUT`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parámetros:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (contenido actualizado)  
  - **Ejemplo de respuesta:** `200 OK` con metadatos actualizados del objeto.

- [Cómo convertir un objeto OLE en una imagen en una hoja de cálculo de Excel](/cells/oleobjects/convert/)
  - **Método:** `GET`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **Parámetros:** `fileName`, `sheetName`, `oleObjectIndex`, `format` (por ejemplo, `png`, `jpeg`)  
  - **Ejemplo de respuesta:** Flujo binario de imagen del objeto OLE convertido.

- [Cómo eliminar todos los objetos OLE en una hoja de cálculo de Excel](/cells/oleobjects/clear/)
  - **Método:** `DELETE`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parámetros:** `fileName`, `sheetName`  
  - **Ejemplo de respuesta:** `204 No Content` que indica que se eliminaron todos los objetos OLE.

- [Cómo eliminar un objeto OLE específico en una hoja de cálculo de Excel](/cells/oleobjects/delete/)
  - **Método:** `DELETE`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parámetros:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Ejemplo de respuesta:** `204 No Content` que confirma que se eliminó el objeto.
---
---
title: Aspose.Cells SDK de nube para Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells La nube admite Excel para crear, convertir, fusionar, dividir, proteger, operaciones de objetos internos, etc.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Nodo
---
 El SDK es de código abierto y tiene la licencia MIT. Puede acceder al código fuente de la biblioteca Node para Aspose.Cells Cloud[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).


# **Cómo utilizar la biblioteca de nodos de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK para Node es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft Excel utilizando el lenguaje de programación Node. Con este SDK, puede crear, editar y convertir Excel documentos en la nube, sin instalar software adicional ni dependencias en su máquina local.


En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK para Node para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de poder comenzar a utilizar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Referirse a[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y su secreto de cliente.

## Cómo instalar el paquete Node para Aspose.Cells Cloud

Puede instalar Aspose.Cells Cloud SDK para Node usando npm. A continuación se detallan los pasos para npm:


```Powershell

npm install asposecellscloud

```

## Cómo agregar dependencias en la configuración del paquete para Aspose.Cells Cloud

archivo de configuración de nodo: paquete.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## Cómo utilizar el paquete Node para convertir Xlsx a PDF

- Importar Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario desde el SDK de Cloud NodeJS Aspose.Cells a su proyecto.
- Configurar el cliente API con credenciales
 Autentique su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo fuente, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

```javascript
var fs = require('fs');
var path = require('path');
const _ = require('asposecellscloud');

const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret,"v3.0",process.env.CellsCloudApiBaseUrl);

var remoteFolder = "TestData/In"
  
var localName = "Book1.xlsx"
var remoteName = "Book1.xlsx"

var localNameRequest = new  model.UploadFileRequest();
localNameRequest.uploadFiles ={localName:fs.createReadStream(localPath  + localName)};
localNameRequest.path = remoteFolder + "/" + remoteName ;
localNameRequest.storageName ="";
cellsApi.uploadFile(localNameRequest );
 
var format = "csv"

var mapFiles = {};           

 mapFiles[localName]= fs.createReadStream(localPath  +localName) ;

var request = new model.PutConvertWorkbookRequest();
request.file =  mapFiles;
request.format =  format;
return cellsApi.putConvertWorkbook(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});
```

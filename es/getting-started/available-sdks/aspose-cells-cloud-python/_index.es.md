---
title: Aspose.Cells SDK de nube para Python
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-python/
description: Aspose.Cells La nube admite Excel para crear, convertir, fusionar, dividir, proteger, operaciones de objetos internos, etc.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Python
---
 El SDK es de código abierto y tiene la licencia MIT. Puede acceder al código fuente de la biblioteca Python para Aspose.Cells Cloud[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python).

# **Cómo utilizar Aspose.Cells Cloud SDK para Python**

Aspose.Cells Cloud SDK para Python es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft Excel utilizando el lenguaje de programación Python. Con este SDK, puede crear, editar y convertir Excel documentos en la nube, sin instalar software adicional ni dependencias en su máquina local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK para Python para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de poder comenzar a utilizar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Referirse a[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y su secreto de cliente.

## Cómo instalar el paquete Python para Aspose.Cells Cloud

Puede instalar Aspose.Cells Cloud SDK para Python con el siguiente comando:

```bash

    pip3 install AsposeCellsCloud
  
 ```

## Cómo utilizar el paquete Python para convertir Xlsx a PDF

- Importar Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario del SDK Aspose.Cells Cloud Python a su proyecto.
- Configurar el cliente API con credenciales
 Autentique su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo fuente, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

```python
import os
import sys
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import *
from asposecellscloud.requests import *

api  = CellsApi(os.getenv('CellsCloudClientId'),os.getenv('CellsCloudClientSecret'),"v3.0",os.getenv('CellsCloudApiBaseUrl'))
remote_folder = 'TestData/In'

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'

format = 'csv'

mapFiles = { 
    local_name: os.path.dirname(os.path.realpath(__file__)) + "/../TestData/" +local_name             
}
mapFiles = { 
    local_name:  local_name             
}
request =  UploadFileRequest( mapFiles, remote_folder + '/' + remote_name,storage_name= '')
api.upload_file(request)
 
request =  PutConvertWorkbookRequest( mapFiles,format= format)
api.put_convert_workbook(request)

```

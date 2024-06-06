---
title: Aspose.Cells SDK de nube para PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells La nube admite Excel para crear, convertir, fusionar, dividir, proteger, operaciones de objetos internos, etc.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, PHP
---
 El SDK es de código abierto y tiene la licencia MIT. Puede acceder al código fuente de la biblioteca PHP para Aspose.Cells Cloud[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Cómo utilizar Aspose.Cells Cloud SDK para PHP**

Aspose.Cells Cloud SDK para PHP es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft Excel utilizando el lenguaje de programación Go. Con este SDK, puede crear, editar y convertir Excel documentos en la nube, sin instalar software adicional ni dependencias en su máquina local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK para PHP para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de poder comenzar a utilizar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Referirse a[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y su secreto de cliente.

## Cómo instalar el paquete PHP para Aspose.Cells Cloud

Puede instalar Aspose.Cells Cloud SDK para PHP. A continuación se detallan los pasos:

- Agregue Aspose.Cells Cloud como dependencia a su archivo `composer.json`:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Ejecute la actualización de Composer para instalar el SDK:

   ```bash

   composer install

   ```

- Incluya el cargador automático de Composer en su código PHP:

   ```php

   require 'vendor/autoload.php';

   ```

## Cómo utilizar el paquete PHP para convertir Xlsx a PDF

- Importar Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario del SDK Aspose.Cells Cloud PHP a su proyecto.
- Configurar el cliente API con credenciales
 Autentique su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo fuente, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```

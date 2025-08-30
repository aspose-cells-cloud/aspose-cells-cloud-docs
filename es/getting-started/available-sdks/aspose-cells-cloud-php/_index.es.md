---
title: Aspose.Cells SDK de nube para PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Cloud admite Excel para crear, convertir, fusionar, dividir, proteger, realizar operaciones con objetos internos, etc.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, PHP
---
El SDK es de código abierto y está licenciado bajo la licencia MIT. Puede acceder al código fuente de la biblioteca PHP para Aspose.Cells Cloud.[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Cómo utilizar el SDK de nube Aspose.Cells para PHP**

El SDK en la nube Aspose.Cells para PHP es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft y Excel mediante el lenguaje de programación Go. Con este SDK, puede crear, editar y convertir documentos Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su equipo local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK para PHP para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de empezar a usar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y secreto de cliente.

## Cómo instalar el paquete PHP para Aspose.Cells Cloud

Puede instalar el SDK de nube Aspose.Cells para PHP. A continuación, se detallan los pasos:

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

- Incluya el autocargador de Composer en su código PHP:

   ```php

   require 'vendor/autoload.php';

   ```

## Cómo usar el paquete PHP para convertir XLSX a otros formatos

- Importación Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario del SDK Aspose.Cells Cloud PHP a su proyecto.
- Configurar el cliente API con credenciales
 Autentique a su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo de origen, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

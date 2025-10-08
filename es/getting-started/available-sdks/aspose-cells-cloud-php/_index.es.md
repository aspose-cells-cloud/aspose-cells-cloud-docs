---
title: "Aspose.Cells SDK en la nube para PHP: convertir, fusionar, dividir, proteger, buscar, reemplazar y más"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for PHP: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells SDK de nube para PH
type: docs
url: /es/available-sdks/aspose-cells-cloud-php/
description: "Aspose.Cells Cloud SDK para PHP ofrece un verdadero poder multiplataforma: una importación proporciona a los desarrolladores de Windows, Linux y macOS la misma fluidez API para crear, convertir, fusionar, dividir, proteger y manipular cada Excel objeto; no se requiere instalación Office y no se necesitan ajustes específicos de la plataforma"
weight: 30
kwords: SDK PHP, SDK Excel para PHP, SDK de la nube para PHP, REST, Gráfico, Tabla dinámica, Objeto de tabla/lista, Convertir hoja de cálculo, PDF, CSV, JSON, Markdown, Combinar, Dividir, Proteger, Buscar, Reemplazar
---
El SDK es de código abierto y está licenciado bajo la licencia MIT. Puedes acceder a él.[el código fuente de la biblioteca PHP para Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

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

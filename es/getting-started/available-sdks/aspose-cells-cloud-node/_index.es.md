---
title: Aspose.Cells SDK de nube para Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Cloud admite Excel para crear, convertir, fusionar, dividir, proteger, realizar operaciones con objetos internos, etc.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Node
---
 El SDK es de código abierto y está licenciado bajo la licencia MIT. Puede acceder al código fuente de la biblioteca Node para Aspose.Cells Cloud.[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Cómo utilizar la biblioteca Node de Aspose.Cells Cloud**

El SDK de nube Aspose.Cells para Node es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft y Excel mediante el lenguaje de programación Node. Con este SDK, puede crear, editar y convertir documentos Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su equipo local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK para Node para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de empezar a usar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y secreto de cliente.

## Cómo instalar el paquete Node para Aspose.Cells Cloud

Puedes instalar el SDK de Cloud Aspose.Cells para Node con npm. A continuación, se detallan los pasos para npm:

```Powershell

npm install asposecellscloud

```

## Cómo agregar dependencias en la configuración del paquete para Aspose.Cells Cloud

archivo de configuración del nodo: package.json

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

## Cómo usar el paquete Node para convertir XLSX a otros formatos

- Importación Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario del SDK Cloud NodeJS Aspose.Cells a su proyecto.
- Configurar el cliente API con credenciales
 Autentique a su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo de origen, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}

---
title: "Aspose.Cells SDK en la nube para Node.js: convertir, fusionar, dividir, proteger, buscar, reemplazar y más"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells SDK de nube para Node.j
type: docs
url: /es/available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK para Node.js ofrece un verdadero poder multiplataforma: una importación proporciona a los desarrolladores de Linux y macOS la misma fluidez para crear, convertir, fusionar, dividir, proteger y manipular cada objeto; no se requiere instalación ni ajustes específicos de la plataforma."
weight: 30
kwords: Node.js, SDK de Node.js, SDK Excel para Node.js, SDK en la nube para Node.js, REST, Gráfico, Tabla dinámica, Objeto de tabla/lista, Convertir hoja de cálculo, PDF, CSV, JSON, Markdown, Combinar, Dividir, Proteger, Buscar, Reemplazar
---
El SDK es de código abierto y está licenciado bajo la licencia MIT. Puedes acceder a él.[El código fuente de la biblioteca Node para Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

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

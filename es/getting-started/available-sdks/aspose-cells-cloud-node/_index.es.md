---
title: "Aspose.Cells Cloud SDK para Node.js: convertir, fusionar, dividir, proteger, buscar, reemplazar y más."
second_title: "Documento"
ArticleTitle: "Aspose.Cells Cloud SDK para Node.js: convertir, fusionar, dividir, proteger, buscar, reemplazar y más."
linktype: "Aspose.Cells Cloud SDK para Node.js"
type: docs
url: /es/available-sdks/aspose-cells-cloud-node/
description: "El SDK de Aspose.Cells Cloud para Node.js ofrece una verdadera potencia multiplataforma: una única importación proporciona a los desarrolladores de Windows, Linux y macOS la misma API fluida para crear, convertir, fusionar, dividir, proteger y manipular todos los objetos de Excel, sin necesidad de instalar Office y sin requerir ajustes específicos por plataforma."
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK para Node.js, Cloud SDK para Node.js, REST, Gráfico, Tabla dinámica, Objeto tabla/lista, Convertir hoja de cálculo, PDF, CSV, JSON, Markdown, Fusionar, Dividir, Proteger, Buscar, Reemplazar
---

El SDK es de código abierto y está licenciado bajo la Licencia MIT. Puede acceder al código fuente de la biblioteca Node de Aspose.Cells Cloud [aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Cómo usar la biblioteca Node de Aspose.Cells Cloud**

El SDK de Aspose.Cells Cloud para Node es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos de Microsoft Excel utilizando el lenguaje de programación Node. Con este SDK, puede crear, editar y convertir documentos de Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su máquina local.

En este artículo, exploraremos cómo utilizar el SDK de Aspose.Cells Cloud para Node para realizar tareas comunes, como crear un nuevo libro de Excel, insertar datos en celdas y guardar el libro modificado en la nube.

## Primeros pasos

Antes de comenzar a utilizar el SDK de Aspose.Cells Cloud para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte [este artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web de Aspose para obtener su ID de cliente y su secreto de cliente.

## Cómo instalar el paquete Node para Aspose.Cells Cloud

Puede instalar el SDK de Aspose.Cells Cloud para Node mediante npm. A continuación se muestran los pasos para npm:

```Powershell

npm install asposecellscloud

```

## Cómo agregar dependencias en la configuración del paquete para Aspose.Cells Cloud

archivo de configuración de Node: package.json

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

## Cómo usar el paquete Node para convertir Xlsx a otros formatos

- Importar la biblioteca Aspose.Cells Cloud  
  Comience importando el paquete necesario del SDK de Aspose.Cells Cloud NodeJS en su proyecto.
- Configurar el cliente de la API con credenciales  
  Autentique su cliente de API con su ID de cliente y secreto de cliente únicos.
- Preparar los parámetros de conversión  
  Defina los parámetros para la tarea de conversión, incluyendo el nombre del archivo de origen, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar la conversión del libro de trabajo  
  invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
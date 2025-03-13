---
title: Aspose.Cells SDK de nube para Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells La nube admite Excel para crear, convertir, fusionar, dividir, proteger, operaciones de objetos internos, etc.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Net
---
 El SDK es de código abierto y tiene la licencia MIT. Puede acceder al código fuente de la biblioteca Net para Aspose.Cells Cloud[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **Cómo utilizar la biblioteca Net de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK para Net es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft Excel utilizando el lenguaje de programación Net. Con este SDK, puede crear, editar y convertir Excel documentos en la nube, sin instalar software adicional ni dependencias en su máquina local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK for Net para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro modificado en la nube.

## Empezando

 Antes de poder comenzar a utilizar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Referirse a[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y su secreto de cliente.

## Cómo instalar el paquete Net para Aspose.Cells Cloud

Puede instalar Aspose.Cells Cloud SDK para Net usando nuget. A continuación se detallan los pasos para nuget:

```nuget

Install-Package Aspose.Cells-Cloud

```

También puedes instalar Aspose.Cells Cloud SDK para Net usando dotnet. A continuación se detallan los pasos para dotnet:

```powershell

dotnet add package Aspose.Cells-Cloud 

```

## Cómo utilizar el paquete Net para convertir Xlsx a PDF

- Importar Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario desde el SDK de Cloud DotNet Aspose.Cells a su proyecto.
- Configurar el cliente API con credenciales
 Autentique su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo fuente, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

### **Código de muestra**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Convert-Excel-To-PDF.cs" >}}

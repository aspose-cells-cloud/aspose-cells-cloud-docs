---
title: Aspose.Cells SDK de nube para Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells Cloud admite Excel para crear, convertir, fusionar, dividir, proteger, realizar operaciones con objetos internos, etc.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Net
---
 El SDK es de código abierto y está licenciado bajo la licencia MIT. Puede acceder al código fuente de la biblioteca Net para Aspose.Cells Cloud.[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **Cómo utilizar la biblioteca Net de Aspose.Cells Cloud**

El SDK de nube Aspose.Cells para NET es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft y Excel mediante el lenguaje de programación NET. Con este SDK, puede crear, editar y convertir documentos Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su equipo local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK for Net para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de empezar a usar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y secreto de cliente.

## Cómo instalar el paquete Net para Aspose.Cells Cloud

Puede instalar el SDK de nube Aspose.Cells para Net con el código nuget. A continuación, se detallan los pasos para el código nuget:

```nuget

Install-Package Aspose.Cells-Cloud

```

También puedes instalar el SDK de Cloud Aspose.Cells para Net con dotnet. A continuación, se detallan los pasos para dotnet:

```powershell

dotnet add package Aspose.Cells-Cloud

```

## Cómo usar el paquete .NET para convertir XLSX a PDF

- Importación Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario del SDK Cloud DotNet Aspose.Cells a su proyecto.
- Configurar el cliente API con credenciales
 Autentique a su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo de origen, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

### **Código de muestra**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_AvailableSDKs.cs" >}}

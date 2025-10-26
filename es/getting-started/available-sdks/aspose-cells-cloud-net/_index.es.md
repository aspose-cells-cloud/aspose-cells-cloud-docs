---
title: "Aspose.Cells SDK en la nube para C#: convertir, fusionar, dividir, proteger, buscar, reemplazar y más"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for C#: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells SDK de nube para .Ne
type: docs
url: /es/available-sdks/aspose-cells-cloud-net/
description: "Aspose.Cells Cloud SDK para .Net ofrece un verdadero poder multiplataforma: una importación proporciona a los desarrolladores de Linux y macOS la misma fluidez para crear, convertir, fusionar, dividir, proteger y manipular cada objeto; no se requiere instalación ni ajustes específicos de la plataforma."
weight: 30
kwords: REST SDK para .Net, Excel SDK para .Net, Cloud SDK para .Net, compatibilidad con conversión, fusión, división, protección, búsqueda, reemplazo y más
---
El SDK es de código abierto y está licenciado bajo la licencia MIT. Puedes acceder a él.[El código fuente de la biblioteca Net para Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **Cómo utilizar la biblioteca Net de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK para NET es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft y Excel mediante el lenguaje de programación NET. Con este SDK, puede crear, editar y convertir documentos Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su equipo local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK for Net para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de empezar a usar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y secreto de cliente.

## Cómo instalar el paquete Net para Aspose.Cells Cloud

Puede instalar el SDK de nube Aspose.Cells para Net con el código nuget. A continuación, se muestran los pasos para el código nuget:

```nuget

Install-Package Aspose.Cells-Cloud

```

También puedes instalar el SDK de nube Aspose.Cells para Net con dotnet. A continuación, se indican los pasos para dotnet:

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

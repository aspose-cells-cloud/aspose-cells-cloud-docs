---
title: "Aspose.Cells SDK en la nube para Perl: convertir, fusionar, dividir, proteger, buscar, reemplazar y más"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Perl: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells SDK en la nube para Per
type: docs
url: /es/available-sdks/aspose-cells-cloud-perl/
description: "Aspose.Cells Cloud SDK para Perl ofrece un verdadero poder multiplataforma: una importación proporciona a los desarrolladores de Windows, Linux y macOS la misma fluidez API para crear, convertir, fusionar, dividir, proteger y manipular cada Excel objeto; no se requiere instalación Office y no se necesitan ajustes específicos de la plataforma"
weight: 30
kwords: Perl, Perl SDK, Excel SDK para Perl, SDK de la nube para Perl, REST, Gráfico, Tabla dinámica, Objeto de tabla/lista, Convertir hoja de cálculo, PDF, CSV, JSON, Markdown, Combinar, Dividir, Proteger, Buscar, Reemplazar
---
El SDK es de código abierto y está licenciado bajo la licencia MIT. Puedes acceder a él.[el código fuente de la biblioteca Perl para Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).

# **Cómo utilizar la biblioteca Perl de Aspose.Cells Cloud**

El SDK en la nube Aspose.Cells para Perl es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft y Excel mediante el lenguaje de programación Perl. Con este SDK, puede crear, editar y convertir documentos Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su equipo local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK para Perl para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de empezar a usar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y secreto de cliente.

## Cómo instalar el paquete Perl para Aspose.Cells Cloud

Puede instalar Aspose.Cells Cloud SDK para Perl con el siguiente comando:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## Cómo usar el paquete Perl para convertir XLSX a otros formatos

- Importación Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario del SDK Aspose.Cells Cloud Perl a su proyecto.
- Configurar el cliente API con credenciales
 Autentique a su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo de origen, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}

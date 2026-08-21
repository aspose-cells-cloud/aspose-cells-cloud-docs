---
title: "Cómo fusionar múltiples archivos de hojas de cálculo con Aspose.Cells Cloud"
linktitle: "Cómo fusionar múltiples archivos de hojas de cálculo"
type: docs
url: /es/how-to-merge-multiple-files
description: "Cómo fusionar múltiples archivos de hojas de cálculo con Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, hoja de cálculo, PDF, CSV, JSON, Markdown, cómo fusionar múltiples archivos mediante Aspose.Cells Cloud
---

## Introducción

La API de Aspose.Cells Cloud es una solución potente basada en la nube diseñada para crear, editar y convertir archivos de hojas de cálculo. En este artículo, le guiaremos paso a paso en el proceso de utilizar la API de Aspose.Cells Cloud para fusionar formatos de archivos, incluyendo casos de uso típicos y código de ejemplo.

## Visión general

La API de Aspose.Cells Cloud proporciona APIs robustas para fusionar múltiples archivos de hojas de cálculo en un único archivo en diversos formatos. Los formatos admitidos incluyen **Excel** (XLS, XLSX), **CSV**, **HTML**, **PDF**, entre otros. Al aprovechar la API de Aspose.Cells Cloud, puede fusionar sin esfuerzo múltiples archivos de hojas de cálculo en un único archivo en formatos ampliamente utilizados, satisfaciendo así diversas necesidades.

Existen múltiples APIs disponibles para la fusión de archivos, generalmente compatibles con diversos entornos en línea. A continuación se describe con detalle cada una de estas APIs:

| Función | Descripción | Referencia de la API |
| :------------------------- | :------------------------- | :------------------------- |
| **[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | Fusiona archivos locales de hojas de cálculo en un archivo de formato especificado. | [MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
| **[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Fusiona archivos de hojas de cálculo almacenados en una carpeta de almacenamiento en la nube en un archivo de formato especificado. | [Merge Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
| **[Merge Spreadsheets In Remote Folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Fusiona archivos de hojas de cálculo almacenados en una carpeta de almacenamiento en la nube en un archivo de formato especificado. | [Merge Spreadsheets In Remote Folder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Cómo fusionar múltiples archivos en uno mediante Aspose.Cells Cloud

La API de Aspose.Cells Cloud proporciona [múltiples SDK](https://github.com/aspose-cells-cloud) para distintos lenguajes de programación. Seleccione el SDK que coincida con su lenguaje de programación preferido y siga la documentación adjunta para su instalación e inicialización. Alternativamente, puede crear su propio SDK siguiendo la [referencia de la API](https://reference.aspose.cloud/cells/). En esta sección, utilizaremos C# como ejemplo para detallar el proceso de fusión de archivos.

## Registro y obtención de la clave de API

Antes de comenzar, debe [registrar una cuenta en Aspose Cloud](https://id.containerize.com/signup) y [obtener una clave de API para la autenticación](https://dashboard.aspose.cloud/applications). Al iniciar sesión en el sitio web oficial de Aspose Cloud, puede crear una cuenta gratuita y obtener una clave de API con fines de autenticación.

Para operaciones más avanzadas, consulte los siguientes documentos: [Inicio rápido con Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Instalación e inicialización del SDK de Aspose.Cells Cloud

Instale el paquete NuGet Aspose.Cells-Cloud en su proyecto .NET; puede utilizar la Consola del Administrador de paquetes NuGet o el Administrador de paquetes NuGet en Visual Studio.
A continuación se muestra cómo instalar el paquete mediante la Consola del Administrador de paquetes:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Cree una nueva instancia de la clase `CellsApi`, inicializándola con su ID de cliente y su secreto de cliente. A continuación se detallan los componentes del fragmento de código anterior:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Asegúrese de reemplazar `YOUR_API_KEY`, `YOUR_APP_SID` y `YOUR_APP_KEY` con su clave de API real, el SID de su aplicación y la clave de su aplicación, respectivamente.

## Construcción de la solicitud a la API y llamada a la API

### Utilizar servicios en la nube para fusionar hojas de cálculo locales y entregar los archivos consolidados ya sea como salidas locales o como flujos en memoria, en cualquier formato requerido

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Construir solicitud de fusión de hojas de cálculo
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Establecer archivos que deben fusionarse.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Establecer formato de salida
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Fusionar en la nube hojas de cálculo almacenadas en la nube y entregar el archivo consolidado localmente o devolverlo al almacenamiento en la nube, en cualquier formato requerido

```C#
// Obtenga su ID de cliente y su Secreto de cliente en https://dashboard.aspose.cloud (se requiere registro gratuito).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Construir parámetros de solicitud de fusión
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Establecer archivo principal en la nube
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Establecer archivo a fusionar en la nube
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Fusionar automáticamente los archivos coincidentes en un directorio de la nube, exportar el resultado consolidado en el formato especificado y entregarlo localmente o devolverlo al almacenamiento en la nube

```csharp
// Obtenga su ID de cliente y su Secreto de cliente en https://dashboard.aspose.cloud (se requiere registro gratuito).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Construir parámetros de solicitud de fusión
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Directorio de almacenamiento que necesita fusionar archivos
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Casos de uso

La función de **fusión de múltiples archivos** de la API de Aspose.Cells Cloud es útil en diversos casos prácticos. A continuación se presentan algunos escenarios comunes:

- **Fusionar múltiples archivos de Excel en un archivo de Excel** para análisis y almacenamiento de datos.
- **Fusionar archivos de datos en un archivo de Excel** para análisis de datos.
- **Fusionar múltiples archivos de imágenes en un archivo PDF** para facilitar su compartir.
- **Fusionar múltiples archivos en un archivo HTML** para su visualización e incrustación en páginas web.

## Conclusión

Con la API de Aspose.Cells Cloud, puede realizar fácilmente la fusión en un solo archivo de múltiples archivos de hojas de cálculo. Al realizar llamadas sencillas a la API y configurar opciones de fusión adecuadas, puede satisfacer eficientemente diversas necesidades de fusión de archivos. Integre la API de Aspose.Cells Cloud en sus aplicaciones para mejorar la productividad y ahorrar tiempo de desarrollo.

Tenga en cuenta que el código de ejemplo anterior tiene fines únicamente ilustrativos; deberá reemplazarlo con credenciales válidas de autenticación y rutas de archivo reales al utilizarlo en la práctica. Además, la API de Aspose.Cells Cloud ofrece muchas otras funcionalidades, como creación, edición, manipulación y procesamiento de datos en hojas de cálculo. La documentación detallada de la API y el código de ejemplo están disponibles en la [guía para desarrolladores del sitio web oficial de Aspose](/developer-guide/).

Esperamos que este artículo le ayude a comprender cómo utilizar la API de Aspose.Cells Cloud para fusionar archivos. ¡Mucha suerte con su implementación!
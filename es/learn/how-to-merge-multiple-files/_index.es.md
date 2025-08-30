---
title: Cómo fusionar varios archivos de hojas de cálculo con Aspose.Cells Clou
linktitle: Cómo fusionar varios archivos de hojas de cálculo
type: docs
url: /es/how-to-merge-multiple-files
description: Cómo fusionar varios archivos de hojas de cálculo con Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Cómo fusionar varios archivos a través de Aspose.Cells Cloud
---
## Introducción

Aspose.Cells Cloud API es una potente solución en la nube diseñada para la creación, edición y conversión de archivos de hojas de cálculo. En este artículo, le guiaremos a través del proceso de uso de Aspose.Cells Cloud API para la fusión de formatos de archivo, incluyendo casos de uso típicos y código de ejemplo.

## Descripción general

 La nube Aspose.Cells API proporciona API robustas para combinar varias hojas de cálculo en un solo archivo con diversos formatos. Los formatos compatibles incluyen:**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**Y más. Al aprovechar la nube Aspose.Cells API, puede combinar fácilmente varias hojas de cálculo en un solo archivo con formatos comunes, que satisface diversas necesidades.

Existen numerosas API para la fusión de archivos, generalmente compatibles con diversos entornos en línea. A continuación, se detallan estas API:

| Función| Descripción| API Referencia|
|:------------------------- |:------------------------- |:------------------------- |
|**[Combinar hojas de cálculo](https://docs.aspose.cloud/cells/merge-spreadsheets/)** |Fusionar archivos de hojas de cálculo locales en un archivo con formato específico.|[Fusionar hojas de cálculo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[Fusionar hoja de cálculo remota](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Fusionar archivos de hojas de cálculo en una carpeta de almacenamiento en la nube en un archivo con un formato específico.|[Fusionar hoja de cálculo remota](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**Fusionar hojas de cálculo en una carpeta remota** | Fusionar archivos de hojas de cálculo en una carpeta de almacenamiento en la nube en un archivo con un formato específico.|[Fusionar hojas de cálculo en una carpeta remota](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Cómo fusionar varios archivos a través de Aspose.Cells Cloud

 La nube Aspose.Cells API proporciona[múltiples SDK](https://github.com/aspose-cells-cloud) para diferentes lenguajes de programación. Elija el SDK que mejor se adapte a su lenguaje de programación preferido y siga la documentación adjunta para la instalación e inicialización. Alternativamente, puede crear su propio SDK según las[Referencia API](https://reference.aspose.cloud/cells/)En esta sección, utilizaremos el ejemplo C# para detallar el proceso de fusión de archivos.

## Registro y Obtención de Clave API

Antes de comenzar, es necesario:[Registrar una cuenta en la nube Aspose](https://id.containerize.com/signup) y[obtener una clave API para autenticación](https://dashboard.aspose.cloud/applications)Al iniciar sesión en el sitio web oficial de Aspose Cloud, puede crear una cuenta gratuita y obtener una clave API para su autenticación.

 Para operaciones más detalladas, consulte los siguientes documentos:[Inicio rápido con Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Instalación e inicialización del SDK de nube Aspose.Cells

Instale el paquete Aspose.Cells-Cloud NuGet en su proyecto .NET, puede utilizar la consola del administrador de paquetes NuGet o el administrador de paquetes NuGet en Visual Studio.
A continuación se explica cómo puede instalar el paquete utilizando la Consola del Administrador de paquetes:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Crea una nueva instancia de la clase CellsApi, inicializándola con su ID y clave secreta de cliente. A continuación, se detalla el fragmento de código mencionado:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Asegúrese de reemplazar SU_API_CLAVE, TUYA_APLICACIÓN_SID y TU_APLICACIÓN_CLAVE con su clave real API, SID de la aplicación y clave de la aplicación.

## Construya la Solicitud API y Llame al API

### Aproveche los servicios en la nube para fusionar hojas de cálculo locales y entregar los archivos consolidados, ya sea como salidas locales o transmisiones en memoria, en cualquier formato requerido.

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Suild merged spreadsheet request
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Set need merged files.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Set output format
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Fusionar hojas de cálculo almacenadas en la nube y entregar el archivo consolidado (localmente o en el almacenamiento en la nube) en cualquier formato requerido

```C#
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Set cloud main file
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Set cloud merged file
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Fusionar automáticamente los archivos coincidentes en un directorio en la nube, exportar el resultado consolidado en el formato especificado y enviarlo localmente o al almacenamiento en la nube.

```csharp
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Storage directory that needs to merge files
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Casos de uso

 Los archivos múltiples**fusionado**La función Aspose.Cells Cloud API es útil en diversos casos prácticos. A continuación, se presentan algunos escenarios comunes:

- **Fusionar varios archivos Excel en un archivo Excel** para análisis y almacenamiento de datos.
- **Fusionar archivos de datos en un archivo Excel** para el análisis de datos.
- **Fusionar varios archivos de imágenes en un archivo PDF** Para compartir fácilmente.
- **Fusionar varios archivos en un archivo html** para visualizar e incrustar en páginas web.

## Conclusión

Con Aspose.Cells Cloud API, puede fusionar fácilmente varias hojas de cálculo en un solo archivo. Con simples llamadas a API y configurando las opciones de fusión adecuadas, puede satisfacer eficientemente diversas necesidades de fusión de archivos. Integre Aspose.Cells Cloud API en sus aplicaciones para mejorar la productividad y ahorrar tiempo de desarrollo.

Tenga en cuenta que el código de ejemplo anterior es solo para fines de demostración y deberá reemplazarlo con credenciales de autenticación y rutas de archivo válidas al usarlo en la práctica. Además, Aspose.Cells Cloud API ofrece muchas otras funciones, como la creación, edición, manipulación y procesamiento de datos de hojas de cálculo. Puede encontrar documentación detallada de API y el código de ejemplo en[Guía para desarrolladores del sitio web oficial Aspose](/developer-guide/).

Esperamos que este artículo te ayude a comprender cómo usar Aspose.Cells Cloud API para la fusión de archivos. ¡Mucha suerte con tu implementación!

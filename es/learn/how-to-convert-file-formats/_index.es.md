---
title: Cómo convertir formatos de archivos de hojas de cálculo con Aspose.Cells Clou
linktitle: Cómo convertir el formato de archivo de una hoja de cálculo
type: docs
url: /es/how-to-convert-file-formats
description: Cómo convertir formatos de archivos con Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Cómo convertir formatos de archivo a través de Aspose.Cells Cloud
---
## Introducción

Aspose.Cells Cloud Spreadsheet API ofrece un conjunto de interfaces de doble canal para convertir archivos de hojas de cálculo locales y en la nube. Admite formatos como Excel (XLS, XLSX), CSV, HTML y PDF, lo que facilita la conversión para satisfacer diversas necesidades.

### Tres modos de conversión · Modelo de objetos unificado · Cobertura de formato completa

![Modos de conversión](image.png)

## **Matriz de conversión de núcleos**

| Tipo de conversión| Nivel de objeto| Típico API| Formatos de salida|
|-----------------|-------------|---------------------------|--------------------------|
|**Conversión local**  | Libro de trabajo|`ConvertSpreadsheet`            | PDF/XLSX/JSON/.... más de 30 formatos|
|| Hoja de trabajo|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         | PDF|
|| Mesa|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             | PDF|
|||`ConvertTableToCsv`             | Cvc|
|||`ConvertTableToHtml`            | HTML|
|||`ConvertTableToJson`            | HTML|
|| Rango|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             | PDF|
|||`ConvertRangeToCsv`             | Cvc|
|||`ConvertRangeToHtml`            | HTML|
|||`ConvertRangeToJson`            | JSON|
||Cuadro|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**Conversión a la nube**  | Libro de trabajo|`ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... más de 30 formatos|
|| Hoja de trabajo|`ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... más de 30 formatos|
|| Mesa|`ExportTableAsFormat`           | PDF/XLSX/JSON/.... más de 30 formatos|
|| Rango|`ExportRangeAsFormat`           | PDF/XLSX/JSON/.... más de 30 formatos|
||Cuadro|`ExportChartAsFormat`           | PDF/XLSX/JSON/.... más de 30 formatos|
|**Guardar como en la nube**     | Libro de trabajo|`SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... más de 30 formatos|

### **Conversión de archivos locales**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Conversión de archivos**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Convertir el gráfico Excel al archivo SVG**

```c#
// Convert local Excel Chart to Svg
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **Convertir tabla a archivo CSV**

```C#
# Convert the sale logs table of the Sales worksheet to csv
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Conversión de archivos en la nube**

También es necesario obtener el cliente Cloud Aspose Cells API.

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Convertir Excel a PDF**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Convertir la hoja de cálculo Excel a PDF**

```csharp
// Convert cloud Excel worksheet to PDF, Save to local file
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Convert cloud Excel worksheet to PDF, Save to local file
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

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

## **Casos de uso de conversión de formatos de archivo**

 Aspose Cells La nube API ofrece un nivel empresarial**conversión de hojas de cálculo** Capacidades para escenarios empresariales críticos:

1. **Excel → PDF**  
 Genere informes listos para imprimir con formato conservado
2. **Hojas de cálculo → HTML**  
 Incrustar tablas interactivas en aplicaciones web
3. **CSV → Excel (XLSX)**  
 Transformar datos sin procesar en libros de trabajo analizables
4. **Transcodificación de formato personalizado**  
 Convierte entre más de 20 formatos (XLS, XLSB, ODS, FODS, TSV)
![Conversión de formatos de entrada a formatos de salida](image-1.png)

## **Conclusión: Optimice las conversiones con una sola llamada al API**

---
title: "Cómo convertir formatos de archivos de hojas de cálculo con Aspose.Cells Cloud"
linktitle: "Cómo convertir formatos de archivos de hojas de cálculo"
type: docs
url: /how-to-convert-file-formats
description: "Cómo convertir formatos de archivos con Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Cómo convertir formatos de archivos mediante Aspose.Cells Cloud
---

## Introducción

La API de hojas de cálculo de Aspose.Cells Cloud proporciona un conjunto de interfaces en dos canales para convertir archivos de hojas de cálculo locales y en la nube. Admite formatos como Excel (XLS, XLSX), CSV, HTML y PDF, facilitando la conversión para satisfacer diversas necesidades.

### Tres modos de conversión · Modelo de objeto unificado · Cobertura completa de formatos

![Modos de conversión](image.png)

## **Matriz de conversión principal**

| Tipo de conversión    | Nivel de objeto   | API típica                      | Formatos de salida             |
|-----------------------|-------------------|---------------------------------|--------------------------------|
| **Conversión local**  | Libro de trabajo  | `ConvertSpreadsheet`            | PDF/XLSX/JSON/… +30 formatos   |
|                       | Hoja de cálculo   | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                   |
|                       |                   | `ConvertWorksheetToPdf`         | PDF                            |
|                       | Tabla             | `ConvertTableToImage`           | PNG/JPEG/SVG/…                 |
|                       |                   | `ConvertTableToPdf`             | PDF                            |
|                       |                   | `ConvertTableToCsv`             | CSV                            |
|                       |                   | `ConvertTableToHtml`            | HTML                           |
|                       |                   | `ConvertTableToJson`            | JSON                           |
|                       | Rango             | `ConvertRangeToImage`           | PNG/JPEG/SVG/…                 |
|                       |                   | `ConvertRangeToPdf`             | PDF                            |
|                       |                   | `ConvertRangeToCsv`             | CSV                            |
|                       |                   | `ConvertRangeToHtml`            | HTML                           |
|                       |                   | `ConvertRangeToJson`            | JSON                           |
|                       | Gráfico           | `ConvertChartToImage`           | PNG/JPEG/SVG/…                 |
|                       |                   | `ConvertChartToPdf`             | PDF                            |
| **Conversión en la nube** | Libro de trabajo  | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/… +30 formatos   |
|                       | Hoja de cálculo   | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/… +30 formatos   |
|                       | Tabla             | `ExportTableAsFormat`           | PDF/XLSX/JSON/… +30 formatos   |
|                       | Rango             | `ExportRangeAsFormat`           | PDF/XLSX/JSON/… +30 formatos   |
|                       | Gráfico           | `ExportChartAsFormat`           | PDF/XLSX/JSON/… +30 formatos   |
| **Guardar como en la nube** | Libro de trabajo  | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/… +30 formatos   |

### **Conversión de archivos locales**

```csharp
// Obtener el cliente de la API de Aspose.Cells Cloud
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Conversión de archivos de Excel**

```c#
// Convertir un archivo de Excel local a PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Convertir un gráfico de Excel a un archivo SVG**

```c#
// Convertir un gráfico de Excel local a SVG
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **Convertir una tabla a un archivo CSV**

```C#
# Convertir la tabla de registros de ventas de la hoja "Sales" a CSV
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Conversión de archivos en la nube**

También es necesario obtener el cliente de la API de Aspose.Cells Cloud.

```csharp
// Obtener el cliente de la API de Aspose.Cells Cloud
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Convertir Excel a PDF**

```csharp
// Convertir un archivo de Excel en la nube a PDF y guardarlo localmente
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Convertir una hoja de cálculo de Excel en la nube a PDF**

```csharp
// Convertir una hoja de cálculo de Excel en la nube a PDF y guardarla localmente
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Convertir una hoja de cálculo de Excel en la nube a PDF y guardarla localmente
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## Instalación e inicialización del SDK de Aspose.Cells Cloud

Instale el paquete NuGet Aspose.Cells-Cloud en su proyecto .NET, ya sea mediante la Consola del Administrador de paquetes NuGet o el Administrador de paquetes NuGet en Visual Studio.
A continuación se muestra cómo instalar el paquete mediante la Consola del Administrador de paquetes:

```powershell

Install-Package Aspose.Cells-Cloud

```

Cree una nueva instancia de la clase CellsApi, inicializándola con su ID de cliente y secreto de cliente. A continuación se detallan los componentes del fragmento de código anterior:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Asegúrese de reemplazar YOUR_API_KEY, YOUR_APP_SID y YOUR_APP_KEY con su clave API real, el SID de su aplicación y la clave de su aplicación.

## **Casos de uso de conversión de formatos de archivo**

La API de Aspose.Cells Cloud ofrece capacidades de **conversión de hojas de cálculo** de nivel empresarial para escenarios críticos de negocio:

1. **Excel → PDF**  
   Genere informes listos para impresión con formato preservado  
2. **Hojas de cálculo → HTML**  
   Incruste tablas interactivas en aplicaciones web  
3. **CSV → Excel (XLSX)**  
   Transforme datos sin procesar en libros de trabajo analizables  
4. **Transcodificación de formatos personalizados**  
   Convierta entre más de 20 formatos (XLS, XLSB, ODS, FODS, TSV)  
![Conversión desde formatos de entrada a formatos de salida](image-1.png)

## **Conclusión: Simplifique las conversiones con una sola llamada a la API**  

---
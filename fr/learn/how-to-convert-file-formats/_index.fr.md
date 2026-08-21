---
title: "Comment convertir des formats de fichiers de feuilles de calcul avec Aspose.Cells Cloud"
linktitle: "Comment convertir des formats de fichiers de feuilles de calcul"
type: docs
url: /how-to-convert-file-formats
description: "Comment convertir des formats de fichiers avec Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, feuille de calcul, PDF, CSV, JSON, Markdown, comment convertir des formats de fichiers via Aspose.Cells Cloud
---

## Introduction

L’API Aspose.Cells Cloud pour les feuilles de calcul fournit un ensemble d’interfaces bidirectionnelles permettant de convertir des fichiers de feuilles de calcul locaux ou hébergés dans le cloud. Elle prend en charge divers formats tels qu’Excel (XLS, XLSX), CSV, HTML et PDF, rendant la conversion aisée afin de répondre à divers besoins.

### Trois modes de conversion · Modèle d’objet unifié · Couverture complète des formats

![Modes de conversion](image.png)

## **Matrice de conversion principale**

| Type de conversion    | Niveau d’objet              | API typique                        | Formats de sortie                              |
|-----------------------|-----------------------------|------------------------------------|------------------------------------------------|
| **Conversion locale** | Classeur                    | `ConvertSpreadsheet`               | PDF/XLSX/JSON/… plus de 30 formats            |
|                       | Feuille de calcul           | `ConvertWorksheetToImage`          | PNG/JPEG/SVG                                   |
|                       |                             | `ConvertWorksheetToPdf`            | PDF                                            |
|                       | Tableau                     | `ConvertTableToImage`              | PNG/JPEG/SVG/…                                 |
|                       |                             | `ConvertTableToPdf`                | PDF                                            |
|                       |                             | `ConvertTableToCsv`                | CSV                                            |
|                       |                             | `ConvertTableToHtml`               | HTML                                           |
|                       |                             | `ConvertTableToJson`               | JSON                                           |
|                       | Plage de cellules           | `ConvertRangeToImage`              | PNG/JPEG/SVG/…                                 |
|                       |                             | `ConvertRangeToPdf`                | PDF                                            |
|                       |                             | `ConvertRangeToCsv`                | CSV                                            |
|                       |                             | `ConvertRangeToHtml`               | HTML                                           |
|                       |                             | `ConvertRangeToJson`               | JSON                                           |
|                       | Graphique                   | `ConvertChartToImage`              | PNG/JPEG/SVG/…                                 |
|                       |                             | `ConvertChartToPdf`                | PDF                                            |
| **Conversion cloud**  | Classeur                    | `ExportSpreadsheetAsFormat`        | PDF/XLSX/JSON/… plus de 30 formats            |
|                       | Feuille de calcul           | `ExportWorksheetAsFormat`          | PDF/XLSX/JSON/… plus de 30 formats            |
|                       | Tableau                     | `ExportTableAsFormat`              | PDF/XLSX/JSON/… plus de 30 formats            |
|                       | Plage de cellules           | `ExportRangeAsFormat`              | PDF/XLSX/JSON/… plus de 30 formats            |
|                       | Graphique                   | `ExportChartAsFormat`              | PDF/XLSX/JSON/… plus de 30 formats            |
| **Enregistrement cloud (Save As)** | Classeur         | `SaveSpreadsheetAs`                | PDF/XLSX/JSON/… plus de 30 formats            |

### **Conversion de fichiers locaux**

```csharp
// Obtenir le client de l’API Aspose.Cells Cloud
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Conversion de fichier Excel**

```c#
// Convertir un fichier Excel local en PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Conversion d’un graphique Excel en fichier SVG**

```c#
// Convertir un graphique Excel local en SVG
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **Conversion d’un tableau en fichier CSV**

```C#
// Convertir le tableau des journaux de ventes de la feuille de calcul « Sales » en CSV
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Conversion de fichiers cloud**

Il est également nécessaire d’obtenir le client de l’API Aspose.Cells Cloud.

```csharp
// Obtenir le client de l’API Aspose.Cells Cloud
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Conversion d’Excel en PDF**

```csharp
// Convertir un fichier Excel hébergé dans le cloud en PDF, puis l’enregistrer localement
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Conversion d’une feuille de calcul Excel en PDF**

```csharp
// Convertir une feuille de calcul Excel hébergée dans le cloud en PDF, puis l’enregistrer localement
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Convertir une feuille de calcul Excel hébergée dans le cloud en PDF, puis l’enregistrer localement
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## Installation et initialisation du SDK Aspose.Cells Cloud

Installez le package NuGet Aspose.Cells-Cloud dans votre projet .NET, à l’aide soit de la console du Gestionnaire de packages NuGet, soit du Gestionnaire de packages NuGet intégré à Visual Studio.
Voici comment installer le package à l’aide de la console du Gestionnaire de packages :

```powershell

Install-Package Aspose.Cells-Cloud

```

Créez une nouvelle instance de la classe `CellsApi`, en l’initialisant avec votre ID client et votre secret client. Voici les détails du fragment de code mentionné précédemment :

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Veillez à remplacer YOUR_API_KEY, YOUR_APP_SID et YOUR_APP_KEY par votre clé API réelle, votre SID d’application et votre clé d’application.

## **Cas d’usage de conversion de formats de fichiers**

L’API Aspose.Cells Cloud offre des capacités de **conversion de feuilles de calcul** de qualité entreprise pour des scénarios métier critiques :

1. **Excel → PDF**  
   Générez des rapports prêts à l’impression avec conservation de la mise en forme
2. **Feuilles de calcul → HTML**  
   Intégrez des tableaux interactifs dans des applications web
3. **CSV → Excel (XLSX)**  
   Transformez des données brutes en classeurs exploitables
4. **Transcodage personnalisé de formats**  
   Convertissez entre plus de 20 formats (XLS, XLSB, ODS, FODS, TSV)
![Conversion des formats d’entrée vers les formats de sortie](image-1.png)

## **Conclusion : Simplifiez les conversions en une seule requête API**

---
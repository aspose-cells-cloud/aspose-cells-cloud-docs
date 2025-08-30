---
title: Comment convertir les formats de fichiers de feuille de calcul avec Aspose.Cells Clou
linktitle: Comment convertir un fichier au format tableur
type: docs
url: /fr/how-to-convert-file-formats
description: Comment convertir des formats de fichiers avec Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Comment convertir des formats de fichiers via Aspose.Cells Cloud
---
## Introduction

Aspose.Cells Cloud Spreadsheet API propose un ensemble d'interfaces double canal pour la conversion de fichiers tableurs locaux et cloud. Il prend en charge des formats tels que Excel (XLS, XLSX), CSV, HTML et PDF, facilitant ainsi la conversion et répondant à divers besoins.

### Trois modes de conversion · Modèle d'objet unifié · Couverture complète du format

![Modes de conversion](image.png)

## **Matrice de conversion de base**

| Type de conversion| Niveau de l'objet| Typique API| Formats de sortie|
|-----------------|-------------|---------------------------|--------------------------|
|**Conversion locale**  | Cahier d'exercices|`ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30+ formats|
|| Feuille de travail|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         | PDF|
|| Tableau|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             | PDF|
|||`ConvertTableToCsv`             | CSV|
|||`ConvertTableToHtml`            | HTML|
|||`ConvertTableToJson`            | HTML|
|| Gamme|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             | PDF|
|||`ConvertRangeToCsv`             | CSV|
|||`ConvertRangeToHtml`            | HTML|
|||`ConvertRangeToJson`            | JSON|
||Graphique|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**Conversion du cloud**  | Cahier d'exercices|`ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30+ formats|
|| Feuille de travail|`ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30+ formats|
|| Tableau|`ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30+ formats|
|| Gamme|`ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30+ formats|
||Graphique|`ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30+ formats|
|**Enregistrer sous dans le cloud**     | Cahier d'exercices|`SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30+ formats|

### **Conversion de fichiers locaux**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Conversion de fichiers**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Convertir le graphique Excel en fichier SVG**

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

- **Convertir un tableau en fichier CSV**

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

### **Conversion de fichiers dans le cloud**

Il faut également obtenir le client Cloud Aspose Cells API.

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Convertir Excel en PDF**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Convertir la feuille de calcul Excel en PDF**

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

## Installation et initialisation du SDK Cloud Aspose.Cells

Installez le package Aspose.Cells-Cloud NuGet dans votre projet .NET, vous pouvez utiliser la console du gestionnaire de packages NuGet ou le gestionnaire de packages NuGet dans Visual Studio.
Voici comment vous pouvez installer le package à l’aide de la console du gestionnaire de packages :

```Powershell

Install-Package Aspose.Cells-Cloud

```

Crée une nouvelle instance de la classe CellsApi, en l'initialisant avec votre ID client et votre secret client. Voici les détails de l'extrait de code mentionné ci-dessus :

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Assurez-vous de remplacer VOTRE_API_CLÉ, VOTRE_APPLICATION_SID et VOTRE_APPLICATION_CLÉ avec votre clé API réelle, votre SID d'application et votre clé d'application.

## **Cas d'utilisation de la conversion de format de fichier**

 Aspose Cells Cloud API offre une qualité professionnelle**conversion de feuille de calcul** capacités pour les scénarios commerciaux critiques :

1. **Excel → PDF**  
 Générez des rapports prêts à imprimer avec une mise en forme préservée
2. **Tableurs → HTML**  
 Intégrer des tableaux interactifs dans des applications Web
3. **CSV → Excel (XLSX)**  
 Transformez les données brutes en classeurs analysables
4. **Transcodage de format personnalisé**  
 Convertissez entre plus de 20 formats (XLS, XLSB, ODS, FODS, TSV)
![Conversion des formats d'entrée aux formats de sortie](image-1.png)

## **Conclusion : optimisez vos conversions avec un seul appel au API**

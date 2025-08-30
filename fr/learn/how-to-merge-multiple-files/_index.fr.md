---
title: Comment fusionner plusieurs fichiers de feuille de calcul avec Aspose.Cells Clou
linktitle: Comment fusionner plusieurs fichiers de feuille de calcul
type: docs
url: /fr/how-to-merge-multiple-files
description: Comment fusionner plusieurs fichiers de feuille de calcul avec Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Comment fusionner plusieurs fichiers via Aspose.Cells Cloud
---
## Introduction

Aspose.Cells Cloud API est une solution cloud performante conçue pour la création, l'édition et la conversion de feuilles de calcul. Dans cet article, nous vous expliquerons comment utiliser Aspose.Cells Cloud API pour la fusion de formats de fichiers, avec des cas d'utilisation typiques et des exemples de code.

## Aperçu

 Le Cloud Aspose.Cells et le Cloud API fournissent des API robustes pour fusionner plusieurs feuilles de calcul en un seul fichier, quel que soit le format. Les formats pris en charge sont les suivants :**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**, et bien plus encore. Grâce au Cloud Aspose.Cells API, vous pouvez facilement fusionner plusieurs feuilles de calcul en un seul fichier aux formats courants, répondant à des besoins variés.

De nombreuses API sont disponibles pour la fusion de fichiers, généralement compatibles avec divers environnements en ligne. Vous trouverez ci-dessous une description détaillée de ces API :

| Fonction| Description| Référence API|
|:------------------------- |:------------------------- |:------------------------- |
|**[Fusionner les feuilles de calcul](https://docs.aspose.cloud/cells/merge-spreadsheets/)** |Fusionner les fichiers de feuille de calcul locaux dans un fichier de format spécifié.|[Fusionner les feuilles de calcul](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[Feuille de calcul MergeRemote](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Fusionnez les fichiers de feuille de calcul dans le dossier de stockage cloud dans un fichier au format spécifié.|[Fusionner une feuille de calcul distante](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**[Fusionner les feuilles de calcul dans un dossier distant](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Fusionnez les fichiers de feuille de calcul dans le dossier de stockage cloud dans un fichier au format spécifié.|[Fusionner des feuilles de calcul dans un dossier distant](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Comment fusionner plusieurs fichiers via Aspose.Cells Cloud

 Le Cloud Aspose.Cells API fournit[plusieurs SDK](https://github.com/aspose-cells-cloud) pour différents langages de programmation. Choisissez le SDK adapté à votre langage de programmation préféré et suivez la documentation fournie pour l'installation et l'initialisation. Vous pouvez également créer votre propre SDK en fonction des[référence API](https://reference.aspose.cloud/cells/)Dans cette section, nous utiliserons C# comme exemple pour détailler le processus de fusion de fichiers.

## Enregistrement et obtention de la clé API

Avant de commencer, vous devez[enregistrer un compte Cloud Aspose](https://id.containerize.com/signup) et[obtenir une clé API pour l'authentification](https://dashboard.aspose.cloud/applications)En vous connectant au site officiel Aspose Cloud, vous pouvez créer un compte gratuit et obtenir une clé API à des fins d'authentification.

 Pour des opérations plus approfondies, veuillez vous référer aux documents suivants :[Démarrage rapide avec Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

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

## Construisez la demande API et appelez le API

### Tirez parti des services cloud pour fusionner des feuilles de calcul locales et fournir les fichiers consolidés, soit sous forme de sorties locales, soit sous forme de flux en mémoire, dans n'importe quel format requis

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

### Fusionnez les feuilles de calcul stockées dans le cloud et livrez le fichier consolidé, localement ou vers le stockage cloud, dans n'importe quel format requis

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

### Fusionnez automatiquement les fichiers correspondants dans un répertoire cloud, exportez le résultat consolidé dans le format spécifié et livrez-le localement ou vers le stockage cloud

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

## Cas d'utilisation

 Les fichiers multiples**fusionné**La fonctionnalité Aspose.Cells du Cloud API est utile dans divers cas d'utilisation. Voici quelques exemples courants :

- **Fusionner plusieurs fichiers Excel dans un fichier Excel** pour l'analyse et le stockage des données.
- **Fusionner les fichiers de données dans un fichier Excel** pour l'analyse des données.
- **Fusionner plusieurs fichiers images dans un fichier PDF** pour un partage facile.
- **Fusionner plusieurs fichiers dans un fichier HTML** pour l'affichage et l'intégration dans les pages Web.

## Conclusion

Avec Aspose.Cells Cloud API, fusionnez facilement plusieurs feuilles de calcul dans un même fichier. En effectuant de simples appels à API et en définissant les options de fusion appropriées, vous pouvez répondre efficacement à divers besoins de fusion de fichiers. Intégrez Aspose.Cells Cloud API à vos applications pour améliorer votre productivité et gagner du temps de développement.

Veuillez noter que l'exemple de code ci-dessus est fourni à titre de démonstration uniquement. Vous devrez le remplacer par des identifiants d'authentification et des chemins de fichiers valides lors de son utilisation pratique. De plus, Aspose.Cells Cloud API offre de nombreuses autres fonctionnalités, telles que la création, l'édition, la manipulation et le traitement de données de feuilles de calcul. La documentation détaillée de API et un exemple de code sont disponibles sur[guide du développeur du site officiel Aspose](/developer-guide/).

Nous espérons que cet article vous aidera à comprendre comment utiliser Aspose.Cells Cloud API pour la fusion de fichiers. Bonne chance pour votre implémentation !

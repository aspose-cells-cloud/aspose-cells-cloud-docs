---
title: "Aspose.Cells Cloud API – Convertir, fusionner, diviser & protéger des fichiers Excel"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud API – Convertir, fusionner, diviser & protéger des fichiers Excel"
linktype: "Developer Center"
type: docs
url: /fr/
description: "L’API REST Aspose.Cells Cloud permet de convertir, fusionner, diviser, protéger et traiter de manière complète les classeurs Excel. Offre gratuite : 150 appels par mois, SDK pour 8 langages."
weight: 10
keywords: "Aspose.Cells Cloud, API Excel, conversion de feuille de calcul, fusion Excel, division Excel, protection Excel, SDK de feuille de calcul cloud, API REST, traitement Excel"
---

## Qu’est-ce que les API Aspose.Cells Cloud ?

Les API Aspose.Cells Cloud sont une collection de services cloud dédiés aux feuilles de calcul/Excel. Aucune installation d’Office ni configuration serveur n’est nécessaire : il suffit d’envoyer une requête HTTP pour créer, modifier, convertir, nettoyer des données, générer des graphiques, construire des tableaux croisés dynamiques, chiffrer, diviser, fusionner, ajouter des filigranes, appliquer des signatures numériques, et bien plus encore, depuis n’importe quel langage de programmation.

## Pourquoi utiliser les API Aspose.Cells Cloud ?

- Créer, modifier, convertir et analyser des feuilles de calcul dans un stockage cloud à l’aide des services API Web Aspose.Cells Cloud.  
- Créer, modifier, convertir et analyser des fichiers de feuilles de calcul locaux à l’aide des services API Web Aspose.Cells Cloud.  
- Les formats de fichiers pris en charge incluent 30 formats, notamment **xlsx**, **csv**, **ods**, **xlsb**, etc.  
- Manipuler directement les feuilles de calcul via l’API Web Aspose.Cells Cloud, sans dépendre de Microsoft Excel.  
- Le forfait gratuit inclut jusqu’à 150 appels d’API par mois.  
- Tarification à l’usage (pay-as-you-go).  
- **Exemples courts** : Opérations réalisables en une seule phrase.  
  - **Convertir XLSX en PDF** → ConvertSpreadsheetToPdf  
  - **Supprimer les espaces superflus dans le fichier entier** → TrimSpreadsheetContent  
  - **Fusionner plus de 10 fichiers en un seul rapport** → MergeSpreadsheets  

## **Comment utiliser les API Aspose.Cells Cloud ?**

### Étape 1 : **Obtenir les identifiants API**

- **[Créer un compte Aspose Cloud](https://dashboard.aspose.cloud/signup)**  
- **[Obtenir les identifiants client](https://dashboard.aspose.cloud/#/applications)**  

### Étape 2 : **Appeler les API Web de feuille de calcul via un SDK (recommandé)**

Il est recommandé d’utiliser le SDK officiel afin de simplifier l’authentification et la gestion des requêtes. Le SDK gère automatiquement l’acquisition et le renouvellement des jetons d’accès.

#### **[Installer le SDK .NET (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### Exemple : **Convertir Excel en PDF à l’aide du SDK**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### Description

- **Spreadsheet** : Nom du fichier Excel situé dans le stockage local.  
- **Format** : Format cible (par exemple, pdf, png, csv, json).  
- **Fichier de sortie** : Le fichier généré sera enregistré localement sous le nom spécifié.  

## **Fonctionnalités principales**

Aspose.Cells Cloud propose les fonctionnalités clés suivantes pour répondre aux besoins d’automatisation des feuilles de calcul au niveau entreprise :

### **Conversion de feuille de calcul**

- **[Convertir une feuille de calcul en fichier PDF](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[Convertir un graphique de feuille de calcul en image](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[Enregistrer une feuille de calcul sous un autre format](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **Traitement des données**

- **[Fusionner des feuilles de calcul](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[Diviser des feuilles de calcul](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[Supprimer les lignes vides d’une feuille de calcul](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[Supprimer les colonnes vides d’une feuille de calcul](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[Remplacer le contenu d’une feuille de calcul](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **Remarque** : Les schémas détaillés de requête/réponse, les méthodes HTTP, les paramètres de requête et les réponses d’exemple pour chaque point de terminaison sont disponibles dans la **Référence de l’API Web Aspose.Cells Cloud pour feuilles de calcul**, indiquée ci-dessous.

**Référence rapide des points de terminaison**

| Opération | Méthode HTTP | Chemin | Paramètres obligatoires | Réponse d’exemple |
|-----------|-------------|------|-----------------------|------------------|
| Convertir une feuille de calcul | POST | `/cells/convert` | `Spreadsheet` (fichier), `format` (chaîne) | Fichier binaire (par exemple, PDF) |
| Fusionner des feuilles de calcul | POST | `/cells/worksheets/merge` | `files` (liste de fichiers) | Classeur fusionné |
| Diviser une feuille de calcul | POST | `/cells/worksheets/split` | `Spreadsheet` (fichier), `format` (chaîne) | Archive contenant les fichiers divisés |
| Supprimer les lignes vides | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (fichier) | Classeur mis à jour |
| Remplacer le contenu | POST | `/cells/replace` | `Spreadsheet` (fichier), `oldValue`, `newValue` | Classeur mis à jour |

## SDK pris en charge (**SDK disponibles**)

- Aspose.Cells Cloud propose des [SDK](https://github.com/aspose-cells-cloud) prêts à l’emploi dans tous les langages majeurs : récupérez, codez et déploiez :

| Langage | Méthode d’installation | Dépôt GitHub |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Dépôt GitHub du SDK Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [Dépôt GitHub du SDK .NET](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Dépôt GitHub du SDK Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Dépôt GitHub du SDK Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [Dépôt GitHub du SDK PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Modules Go](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [Dépôt GitHub du SDK Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Dépôt GitHub du SDK Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Dépôt GitHub du SDK Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **Point de terminaison API** | [Référence de l’API Web Aspose.Cells Cloud pour feuilles de calcul](https://reference.aspose.cloud/cells/) |  |

## **Exemples de code et projets open source**

Tous les SDK sont open source et incluent de nombreux exemples :

- [Exemples du SDK Java sur GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [Exemples du SDK .NET sur GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Exemples du SDK Python sur GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Exemples du SDK Node.js sur GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [Exemples du SDK PHP sur GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Exemples du SDK Go sur GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Exemples du SDK Ruby sur GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Exemples du SDK Perl sur GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)
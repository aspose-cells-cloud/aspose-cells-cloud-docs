---
title: "Aspose.Cells Cloud Web : stockage dans le cloud, conversion de feuilles de calcul, fusion, division, protection, traitement de données, etc."
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and mor"
linktitle: Centre de développement
type: docs
url: /fr/
description: Les API Web Cloud Aspose.Cells prennent en charge Spreadsheet/Excel pour créer, convertir, fusionner, diviser, protéger et effectuer des opérations d'objets internes, entre autres fonctions. Aspose.Cells Cloud fournit un document complet, prend en charge les interfaces RESTful et des exemples de code pour aider les développeurs à intégrer rapidement
weight: 10
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdown, Aspose.Cells Document Cloud
---
## Qu'est-ce que Aspose.Cells Cloud APIs ?

Les API Cloud Aspose.Cells sont un ensemble de services cloud Spreadsheet/Excel - pas besoin d'installer Office, pas besoin de configurer les serveurs, envoyez simplement une requête HTTP et vous pouvez effectuer toutes les opérations courantes telles que la création, l'édition, la conversion de format, le nettoyage des données, les graphiques, les tableaux croisés dynamiques, le cryptage, le fractionnement, la fusion, les filigranes, les signatures numériques, etc., n'importe où et dans n'importe quelle langue.

## Pourquoi utiliser les API Cloud Aspose.Cells ?

- Création, édition, conversion et analyse de feuilles de calcul dans le stockage cloud basé sur les services Aspose.Cells Cloud Web API.
- Créez, modifiez, convertissez et analysez des fichiers de feuille de calcul locaux basés sur les services Aspose.Cells Cloud Web API.
- Les formats de fichiers pris en charge sont 30, tels que xlsx, csv, ods, xlsb, etc.
- Exécutez des feuilles de calcul directement via le Cloud Web Aspose.Cells API sans avoir besoin de dépendances Microsoft Excel.
- 150 appels gratuits par mois au API.
- Facturation par étapes, combien les utilisateurs utilisent, combien ils facturent, plus ils utilisent, plus ils offrent de remises.
- **Code court**:Choses qui peuvent être faites en une phrase.
  - **Convertir XLSX en PDF** → Convertir une feuille de calcul en PDF
  - **Supprimer les espaces supplémentaires dans l'ensemble du fichier** → TrimSpreadsheetContent
  - **Combinez plus de 10 fichiers dans un seul rapport** → Fusionner les feuilles de calcul

## **Comment utiliser les API Cloud Aspose.Cells ?**

###  Étape 1 :**Obtenez les identifiants API**

- **[Enregistrer un compte Cloud Aspose](https://dashboard.aspose.cloud/signup)**
- **[Obtenir les informations d'identification du client](https://dashboard.aspose.cloud/#/applications)**

###  Étape 2 :**Appeler les API Web de feuilles de calcul avec le SDK (recommandé)**

Il est recommandé d'utiliser le SDK officiel pour simplifier le processus d'authentification et de demande.

#### **[Installer le SDK (en utilisant .NET comme exemple)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell

dotnet add package Aspose.Cells-Cloud --version 25.8.0

```

####  Exemple:**Convertir Excel en PDF avec SDK**

```C#
    CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
    cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

#### Description

- **Tableur**: Le nom du fichier Excel qui doit se trouver dans le stockage local.
- **Format**Format cible. Par exemple pdf, png, csv, json, etc.
- **Fichier de sortie** sera enregistré localement. « EmployeeSalesSummary.pdf » est le nom du fichier de sortie.

## **Fonctions principales**

Aspose.Cells Cloud offre les fonctionnalités clés suivantes pour répondre aux besoins d'automatisation des feuilles de calcul au niveau de l'entreprise :

### **Conversion de feuilles de calcul**

- **[Convertir une feuille de calcul en fichier PDF](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**
- **[Convertir un graphique de feuille de calcul en image](https://docs.aspose.cloud/cells/convert-chart-to-image/)**
- **[Enregistrer la feuille de calcul sous](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**

### **Informatique**

- **[Fusionner les feuilles de calcul](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Feuilles de calcul fractionnées](https://docs.aspose.cloud/cells/split-spreadsheet/)**
- **[Supprimer les lignes vides de la feuille de calcul](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**
- **[Supprimer les colonnes vides de la feuille de calcul](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**
- **[Remplacer le contenu de la feuille de calcul](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**

## Prise en charge des SDK (**SDK disponibles**)

-  Aspose.Cells Offres Cloud[SDK](https://github.com/aspose-cells-cloud)** en plusieurs langues, prêt à l'emploi :

| Langue| Méthode d'installation| Dépôt GitHub|
||----|-------|
|[Java](https://www.oracle.com/java/) |[Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) |[Java Référentiel GitHub du SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
|[.NET](https://dotnet.microsoft.com/) |[NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) |[.NET Référentiel GitHub du SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
|[Python](https://www.python.org/) |[pépin](https://pypi.org/project/asposecellscloud/) |[Python Référentiel GitHub du SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
|[Node.js](https://nodejs.org/en) |[npm](https://www.npmjs.com/package/asposecellscloud) |[Référentiel GitHub du SDK Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
|[PHP](https://www.php.net/) |[Compositeur](https://packagist.org/packages/aspose/cells-sdk-php) |[PHP Référentiel GitHub du SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
|[GoLang](https://go.dev/) |[Modules Go](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) |[Référentiel GitHub du SDK GoLang](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
|[Rubis](https://www.ruby-lang.org/) |[Gemmes rubis](https://rubygems.org/gems/aspose_cells_cloud) |[Référentiel GitHub du SDK Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
|[Perl](https://www.perl.org/) |[CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) |[Perl Référentiel GitHub du SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |

- **API Point final**: [Aspose.Cells Cloud Spreadsheet Web API Référence](https://reference.aspose.cloud/cells/)

## **Exemples de code et projets open source**

Tous les SDK sont open source et incluent de riches exemples :

- [Java Exemples de SDK sur Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)
- [.NET Exemples de SDK sur Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)
- [Python Exemples de SDK sur Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)
- [Exemples de SDK Node.js sur Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)
- [PHP Exemples de SDK sur Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)
- [Exemples de Go SDK sur Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)
- [Exemples de SDK Ruby sur Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)
- [Perl Exemples de SDK sur Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)

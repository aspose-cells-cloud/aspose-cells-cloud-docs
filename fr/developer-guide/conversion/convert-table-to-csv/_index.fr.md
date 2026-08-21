---
title: "Aspose.Cells Cloud Web API - Convertir les données d'un tableau de feuille de calcul en fichier CSV - Outil en ligne gratuit"
second_title: "Document"
ArticleTitle: "Comment convertir les données d'un tableau de feuille de calcul en fichier CSV : guide pas à pas"
linktitle: "Convertir un tableau en CSV"
type: docs
url: /convert-table-to-csv/
keywords: "Aspose.Cells Cloud, tableau vers CSV, conversion de feuille de calcul, Excel vers CSV, API, REST, exportation de données"
description: "Convertissez rapidement un tableau d'une feuille de calcul Excel en fichier CSV à l'aide de l'API Aspose.Cells Cloud."
weight: 100
---

Exportez les données d’un tableau à partir d’un fichier Excel local vers un fichier CSV à l’aide de l’API Cloud.

## **Convertir un tableau en CSV via l’API**

### API Web

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                      |
| ---------------- | ------ | ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                              | Télécharger le fichier de feuille de calcul.                                                                                                                     |
| worksheet        | Chaîne  | Chaîne de requête                                      | Nom de la feuille de calcul dans le classeur.                                                                                                                   |
| tableName        | Chaîne  | Chaîne de requête                                      | Nom du tableau à convertir.                                                                                                                                      |
| outPath          | Chaîne  | Chaîne de requête                                      | (Facultatif) Chemin du dossier où le classeur est stocké ; valeur par défaut : null.                                                                            |
| outStorageName   | Chaîne  | Chaîne de requête                                      | Nom du stockage pour le fichier de sortie.                                                                                                                      |
| fontsLocation    | Chaîne  | Chaîne de requête                                      | Chemin pour utiliser des polices personnalisées.                                                                                                                 |
| region           | Chaîne  | Chaîne de requête                                      | Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                      | Mot de passe pour ouvrir le fichier de feuille de calcul.                                                                                                       |

### **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Codes de statut HTTP**

| Code | Signification         | Description                                                     |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.              |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                     |

## **Dans quels cas utiliser l’API Convert Table to CSV ?**

- **Migration de base de données** : Convertir des tableaux Excel en CSV pour les importations en masse dans des bases de données SQL (MySQL, PostgreSQL, SQL Server).
- **Chargement dans un entrepôt de données** : Transformer des tableaux de rapports basés sur Excel en CSV pour les charger dans Snowflake, Redshift ou BigQuery.
- **Payloads d’API en lots** : Convertir les données de tableaux Excel en CSV pour les téléversements en masse vers des services REST.
- **Communication entre services** : Utiliser CSV comme format léger d’échange de données entre microservices.
- **Préparation des données pour le machine learning** : Convertir les tableaux de caractéristiques depuis Excel en CSV pour les bibliothèques Python/R de machine learning.
- **Analyse statistique** : Transformer les tableaux de données de recherche en CSV pour les importer dans SPSS, SAS ou Stata.
- **Migration de contenu** : Déplacer du contenu structuré depuis Excel vers des systèmes de gestion de contenu (CMS) via CSV.

## Pourquoi utiliser l’API Convert Table to CSV ?

- **Adaptée aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, ce qui permet un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions personnalisées, cela réduit considérablement la charge de développement.
- **Économique** : Vous pouvez convertir les données des tableaux sans avoir à télécharger d’abord le classeur, ce qui économise de l’espace de stockage et réduit les coûts.
- **Extraction pure des données sans mise en forme**.
- **Le format CSV est pris en charge par quasiment tous les systèmes** :
  - Bases de données (tous les SGBD majeurs)
  - Langages de programmation (analyseurs natifs inclus dans tous)
  - Outils de business intelligence (Tableau, Power BI, Looker)
  - Logiciels de feuilles de calcul (Excel, Google Sheets, LibreOffice)
  - Outils en ligne de commande (awk, sed, grep)

## Comment utiliser l’API Convert Table to CSV avec les SDK ?

### Spécification de l’API Convert Table to CSV

La [Spécification de l’API Convert Table to CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) fournit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.
Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier optionnel"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet de convertir les données d’un tableau de feuille de calcul en fichier CSV avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}
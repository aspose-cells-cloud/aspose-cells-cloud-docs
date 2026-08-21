---
title: "Aspose.Cells Cloud Web API - Exporter une feuille de calcul Excel distante vers d'autres formats - Outil gratuit en ligne"
second_title: "Document"
ArticleTitle: "Comment exporter une feuille de calcul de classeur distant vers d'autres formats : guide pas à pas"
linktitle: "Exporter le classeur vers un format"
type: docs
url: /export-spreadsheet-as-format/
keywords: "Aspose.Cells, conversion de feuille de calcul, API, export, PDF, CSV, JSON, XLSX"
description: "Convertir des classeurs Excel stockés dans Aspose Cloud en PDF, XLSX, CSV, JSON ou HTML via un seul point de terminaison REST. Apprenez la syntaxe des requêtes, les paramètres, et découvrez des exemples de SDK en C#, Java, Python, et plus encore."
weight: 100
---

Exporter une feuille de calcul cloud (Excel) vers un autre format de fichier.

## **API d'exportation de feuille de calcul vers un format**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                        |
| :--------------- | :----- | :----------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Chemin                                                 | (Obligatoire) Le nom du fichier de classeur à récupérer.                                                                                          |
| format           | String | Chaîne de requête                                       | (Obligatoire) Le format de sortie souhaité (par ex. « Xlsx », « PDF », « CSV »).                                                                  |
| folder           | String | Chaîne de requête                                       | (Facultatif) Le chemin du dossier dans lequel le classeur est stocké. La valeur par défaut est null.                                             |
| storageName      | String | Chaîne de requête                                       | (Facultatif) Le nom du stockage si vous utilisez un stockage cloud personnalisé. Utilisez le stockage par défaut si ce paramètre est omis.       |
| outPath          | String | Chaîne de requête                                       | (Facultatif) Le chemin du dossier dans lequel le classeur sera stocké. La valeur par défaut est null.                                             |
| outStorageName   | String | Chaîne de requête                                       | (Facultatif) Nom du stockage de destination.                                                                                                      |
| fontsLocation    | String | Chaîne de requête                                       | (Facultatif) Emplacement personnalisé des polices.                                                                                                 |
| region           | String | Chaîne de requête                                       | (Facultatif) Paramètre de région/langue de la feuille de calcul (par ex. `fr-FR`, `en-US`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | String | Chaîne de requête                                       | (Facultatif) Le mot de passe pour ouvrir le fichier de feuille de calcul.                                                                         |

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

La réponse contient un seul objet représentant le flux du fichier converti.

**Codes de statut HTTP**

| Code | Signification          | Description                                                     |
| ---- | ---------------------- | --------------------------------------------------------------- |
| 200  | OK                     | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte     | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé           | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.             |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                      |

## Où utiliser l’API d’exportation de feuille de calcul vers un autre format ?

- **Migration de systèmes hérités** : Convertir des milliers de fichiers XLS hérités en XLSX pour les systèmes modernes.
- **Standardisation des archives** : Normaliser divers formats de feuilles de calcul (XLS, XLSM, ODS, CSV) vers un seul format pour l’archivage.
- **Interopérabilité avec des suites bureautiques** : Convertir des fichiers Excel vers des formats compatibles avec LibreOffice, Google Sheets ou Apple Numbers.
- **Normalisation des sources de données** : Convertir divers formats de feuilles de calcul en CSV ou JSON pour une ingestion dans des bases de données.
- **Publication web** : Convertir des modèles financiers en HTML pour une diffusion sur le web.

## Pourquoi utiliser l’API d’exportation de feuille de calcul vers un autre format ?

- **Facile à utiliser pour les développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, ce qui permet un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de travail de développement.
- **Réduction des coûts de main-d’œuvre** : Diminue la nécessité d’affecter du personnel à la consolidation de documents.
- **Paiement à l’usage** : Aucun investissement préalable ; vous ne payez que pour les appels API effectivement utilisés.
- **Aucune maintenance côté serveur requise** : Pas besoin de maintenir des serveurs, mettre à jour des logiciels ou gérer des problèmes de compatibilité.
- **Support complet des formats** : Convertir entre plus de 20 formats de feuilles de calcul.
- **Préservation de la fidélité des données et du formatage** : Maintient la mise en page, les formules et le style originaux pendant la conversion.

## Comment utiliser l’API d’exportation de feuille de calcul vers un format avec les SDK ?

### Spécification de l’API d’exportation de feuille de calcul vers un format

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">spécification de l’API d’exportation de feuille de calcul vers un format</a> fournit une interface de programmation publiquement accessible pour effectuer des interactions REST de manière transparente.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant d’exporter une feuille de calcul vers un fichier dans un format spécifique à l’aide d’un code court.  
Avant d’appeler l’API, obtenez un jeton d’accès OAuth 2.0 et incluez-le dans l’en-tête `Authorization: Bearer <token>`.

Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment interagir avec les services web Aspose.Cells via divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
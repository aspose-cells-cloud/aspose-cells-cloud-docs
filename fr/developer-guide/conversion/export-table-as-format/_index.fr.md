---
title: "Exporter un tableau – API Aspose.Cells Cloud | Convertir Excel en PDF, PNG, CSV"
second_title: "Document"
ArticleTitle: "Comment exporter un tableau de feuille de calcul distante vers un autre format : guide étape par étape"
linktype: "Exporter le tableau au format spécifié"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells, exporter un tableau, Excel vers PDF, API cloud, REST"
description: "Exportez un tableau Excel stocké dans le cloud au format PDF, PNG, CSV, JSON ou autre à l’aide de l’API Aspose.Cells Cloud. Endpoint HTTPS sécurisé avec authentification JWT et exemples de SDK."
weight: 100
---

Exportez un tableau de feuille de calcul (Excel) stocké dans le cloud vers un fichier d’un autre format.

## **API d’exportation de tableau vers un format**

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Chemin / Chaîne de requête / Corps HTTP | Description                                                                                                                                                     |
| :--------------- | :----- | :--------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Chemin                                   | **Obligatoire.** Nom du fichier classeur à récupérer.                                                                                                           |
| worksheet        | String | Chemin                                   | Nom de la feuille de calcul.                                                                                                                                    |
| tableName        | String | Chemin                                   | Nom du tableau.                                                                                                                                                 |
| format           | String | Chaîne de requête                         | **Obligatoire.** Format de sortie souhaité (par exemple, « png », « pdf », « svg »).                                                                           |
| folder           | String | Chaîne de requête                         | Facultatif. Chemin du dossier où le classeur est stocké. La valeur par défaut est `null`.                                                                     |
| storageName      | String | Chaîne de requête                         | Facultatif. Nom du stockage utilisé si un stockage cloud personnalisé est employé. Utilise le stockage par défaut si omis.                                   |
| outPath          | String | Chaîne de requête                         | Facultatif. Chemin du dossier de destination pour le stockage de la sortie. La valeur par défaut est `null`.                                                  |
| outStorageName   | String | Chaîne de requête                         | Facultatif. Nom du stockage pour le fichier de sortie.                                                                                                         |
| fontsLocation    | String | Chaîne de requête                         | Facultatif. Emplacement des polices personnalisées.                                                                                                             |
| region           | String | Chaîne de requête                         | Facultatif. Paramètre régional/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement lié à la localisation. |
| password         | String | Chaîne de requête                         | Facultatif. Mot de passe pour ouvrir le fichier de feuille de calcul.                                                                                          |

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

**Codes d’état HTTP**

| Code | Signification         | Description                                                                 |
| ---- | --------------------- | --------------------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                              |
| 413  | Charge utile trop volumineuse | Le fichier envoyé dépasse la taille limite.                                |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                               |

## **Dans quels cas utiliser l’API d’exportation de tableau vers un autre format ?**

- **Migration des systèmes hérités** : Convertir des milliers de fichiers XLS hérités en XLSX pour les systèmes modernes.
- **Standardisation des archives** : Normaliser divers formats de feuilles de calcul (XLS, XLSM, ODS, CSV) vers un seul format pour l’archivage.
- **Interopérabilité avec les suites bureautiques** : Convertir des fichiers Excel vers des formats compatibles avec LibreOffice, Google Sheets ou Apple Numbers.
- **Normalisation des sources de données** : Convertir divers formats de feuilles de calcul en CSV ou JSON pour l’ingestion dans des bases de données.
- **Publication web** : Convertir des modèles financiers en HTML pour affichage sur le web.

## Pourquoi utiliser l’API d’exportation de tableau vers un autre format ?

- **Facile à utiliser pour les développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide, et est accompagné d’une documentation complète. Comparé à la mise en œuvre de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de travail de développement.
- **Réduction des coûts de main-d’œuvre** : Diminue le besoin de consacrer des postes à la consolidation de documents.
- **Paiement à l’usage** : Aucun investissement initial ; vous ne payez que pour les appels d’API effectivement utilisés.
- **Coûts de maintenance nuls** : Aucune maintenance de serveurs, mise à jour de logiciels ou gestion des problèmes de compatibilité.
- **L’API renvoie uniquement les données brutes du tableau, sans mise en forme du classeur.**

## Comment utiliser l’API d’exportation de tableau de feuille de calcul vers un format à l’aide des SDK ?

### Spécification de l’API Export Table as Format

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">spécification de l’API Export Table as Format</a> définit une interface de programmation publiquement accessible et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
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
  "fileDownloadName": "nom de fichier facultatif"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant ainsi d’exporter un tableau de feuille de calcul vers un fichier d’un format donné à l’aide d’un code concis. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
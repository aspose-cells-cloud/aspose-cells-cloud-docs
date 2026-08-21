---
title: "API d’importation de données Aspose.Cells Cloud – Une solution cloud permettant d’importer automatiquement des données CSV, JSON et XML dans des classeurs Excel."
second_title: "Document"
ArticleTitle: "Plateforme d’intégration multi-source de données Excel – API Aspose.Cells Cloud d’importation et de transformation automatisée des données."
linktitle: "Importer des données dans un classeur"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Aspose Cells, API d’importation de données, CSV vers Excel, JSON vers Excel, XML vers Excel, classeur cloud, API REST"
description: "Importez des données CSV, JSON ou XML dans des classeurs Excel à l’aide de l’API REST Aspose.Cells Cloud. Découvrez le format des requêtes, les paramètres, des exemples de code avec les SDK et la gestion des erreurs."
weight: 100
---

## Fonctionnalités principales

### Prise en charge des données en plusieurs formats

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">Importation de données CSV</a>** : prend en charge divers délimiteurs et détecte automatiquement l’encodage.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">Traitement des données JSON</a>** : aplatie les structures JSON complexes dans des tableaux Excel.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Conversion de fichiers XML</a>** : mappe les données de nœuds vers la structure lignes et colonnes d’Excel.

## **Description de l’API d’importation de données dans un classeur**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre   | Type   | Emplacement        | Description                                                                 |
|--------------------|--------|--------------------|-----------------------------------------------------------------------------|
| datafile           | Fichier| FormData           | Le fichier de données (CSV, JSON ou XML) à importer.                       |
| spreadsheet        | Fichier| FormData           | Le classeur cible qui recevra les données importées.                      |
| worksheet          | chaîne | Query              | Nom de la feuille de calcul où les données seront placées.                |
| startCell          | chaîne | Query              | Cellule en haut à gauche (par ex. `A1`) marquant la position de départ.   |
| insert             | booléen| Query              | `true` pour insérer des lignes ; `false` pour écraser les données existantes. |
| convertNumericData | booléen| Query              | `true` pour convertir les chaînes numériques en nombres durant l’import.  |
| splitter           | chaîne | Query              | Délimiteur CSV à un seul caractère (valeur par défaut : `,`).              |
| outPath            | chaîne | Query (facultatif) | Chemin du dossier où le classeur mis à jour sera stocké.                 |
| outStorageName     | chaîne | Query (facultatif) | Nom de l’emplacement de stockage pour le fichier de sortie.               |
| fontsLocation      | chaîne | Query (facultatif) | Chemin vers un dossier de polices personnalisé, le cas échéant.           |
| region             | chaîne | Query (facultatif) | Configuration régionale du classeur (par ex. `fr-FR`).                    |
| password           | chaîne | Query (facultatif) | Mot de passe pour ouvrir un classeur protégé.                             |

### Réponse

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

| Code | Signification          | Description                                                       |
|------|------------------------|-------------------------------------------------------------------|
| 200  | OK                     | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête       | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé           | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.              |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                      |

## Pourquoi utiliser cette API ?

- **Chargement efficace des données** : permet l’importation en masse de grands jeux de données directement dans un classeur, sans créer de fichiers intermédiaires.
- **Large prise en charge des SDK** : fournit des bibliothèques clientes pour .NET, Java, PHP, Ruby, Node.js, Python, Go et Perl, facilitant l’intégration.
- **Traitement en mémoire** : exécute les transformations en mémoire, réduisant ainsi les exigences de stockage temporaire.

## Comment utiliser l’API d’importation de données dans un classeur à l’aide des SDK

**Notes / Limites** : L’API prend en charge jusqu’à 1 000 000 de lignes par importation. Seule la virgule est le délimiteur CSV par défaut ; d’autres délimiteurs à un seul caractère peuvent être spécifiés via le paramètre `splitter`. Les fichiers XML volumineux peuvent augmenter le temps de traitement.

Pour des opérations connexes telles que l’exportation de données ou la conversion de formats de classeur, consultez la documentation **Exportation de données** et **Conversion de classeur**.

### Spécification de l’API d’importation de données dans un classeur

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">spécification de l’API d’importation de données dans un classeur</a> fournit une interface de programmation accessible publiquement, permettant des interactions REST directement depuis votre navigateur web.
Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Feuil1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {jeton_d'accès}" \
  -F "datafile=@/chemin/vers/données.csv" \
  -F "spreadsheet=@/chemin/vers/classeur.xlsx"
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

L’utilisation des SDK constitue la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant d’importer des données dans une feuille de calcul avec un code concis. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

---
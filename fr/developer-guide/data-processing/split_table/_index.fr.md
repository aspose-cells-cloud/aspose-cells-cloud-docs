---
title: "Découper un tableau"
ArticleTitle: "Découper un tableau – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Découper un tableau"
type: docs
url: /cells/split/table
aliases: []
keywords: "Aspose.Cells, Découper un tableau, API"
description: "API permettant de découper un tableau dans une feuille de calcul selon les valeurs d’une colonne."
weight: 1
---

## La méthode SplitTable des services Web Aspose.Cells Cloud

Cette méthode réalise une opération de découpe sur le tableau source en regroupant les lignes selon les valeurs distinctes de la colonne spécifiée. Chaque groupe de données (correspondant à chaque valeur unique de découpe) est ensuite traité comme une unité de données distincte. La destination de l’export est contrôlée par deux paramètres booléens clés :
- Détermine la structure du classeur : si `true`, chaque unité découpée est enregistrée dans un fichier de classeur distinct ; si `false`, chaque unité devient une nouvelle feuille de calcul au sein du classeur actuel.
- Détermine la manière dont les fichiers sont empaquetés : si `true` et combiné à `toNewWorkbook` = `true`, la méthode génère plusieurs fichiers individuels et les renvoie sous forme d’une archive ZIP ; si `false`, toutes les données sont consolidées dans un seul fichier (soit un classeur multi-feuilles, soit un fichier unique selon les autres paramètres).

### Point de terminaison de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (Chemin / Chaîne de requête / Corps HTTP) | Description                                                                                                                                                                   |
|------------------|---------|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fichier | FormData                                               | Téléchargement du fichier de feuille de calcul.                                                                                                                              |
| worksheet        | Chaîne  | Chaîne de requête                                      | Feuille de calcul contenant le tableau.                                                                                                                                      |
| tableName        | Chaîne  | Chaîne de requête                                      | Tableau de données à découper.                                                                                                                                                |
| splitColumnName  | Chaîne  | Chaîne de requête                                      | Nom de la colonne selon laquelle effectuer le découpage.                                                                                                                     |
| saveSplitColumn  | Booléen | Chaîne de requête                                      | Indique s’il faut conserver les données de la colonne utilisée pour le découpage.                                                                                             |
| splitRowNumber   | Entier  | Chaîne de requête                                      | [À définir]                                                                                                                                                                    |
| toNewWorkbook    | Booléen | Chaîne de requête                                      | Contrôle de la destination d’export : `true` – Crée des fichiers de classeur contenant les données découpées ; `false` – Ajoute une nouvelle feuille au classeur actuel.      |
| toMultipleFiles  | Booléen | Chaîne de requête                                      | `true` – Exporte les données du tableau sous la forme de **plusieurs fichiers distincts** (renvoyés sous forme d’une archive ZIP) ; `false` – Stocke toutes les données dans un **fichier unique** contenant plusieurs feuilles. Valeur par défaut : `false`. |
| outPath          | Chaîne  | Chaîne de requête                                      | (Facultatif) Le chemin du dossier où le classeur sera enregistré. La valeur par défaut est `null`.                                                                          |
| outStorageName   | Chaîne  | Chaîne de requête                                      | Nom du stockage pour le fichier de sortie.                                                                                                                                   |
| fontsLocation    | Chaîne  | Chaîne de requête                                      | Utiliser des polices personnalisées.                                                                                                                                          |
| region           | Chaîne  | Chaîne de requête                                      | Paramètre de région/langue de la feuille de calcul (par exemple, `fr-FR`, `en-US`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                      | Mot de passe nécessaire pour ouvrir le fichier de feuille de calcul.                                                                                                         |

### Paramètre du corps de la requête

| Nom du paramètre | Type   | Description                      |
| ---------------- | ------ | -------------------------------- |
| Spreadsheet      | Fichier | Téléchargement du fichier de feuille de calcul. |

### **Réponse**

```json
{
  "file": "flux binaire (archive ZIP ou classeur selon les paramètres)"
}
```

**Codes d’état de la réponse**

| Code | Signification           | Description                                                                                             |
|------|-------------------------|---------------------------------------------------------------------------------------------------------|
| 200  | OK                      | L’opération de découpe s’est déroulée avec succès. La réponse contient le fichier généré (archive ZIP ou classeur). |
| 400  | Requête incorrecte      | URL ou paramètres de requête non valides.                                                               |
| 401  | Non autorisé            | L’authentification a échoué ou aucune information d’identification n’a été fournie.                    |
| 404  | Introuvable             | Le fichier source n’est pas accessible.                                                                 |
| 413  | Charge utile trop volumineuse | La taille du corps de la requête dépasse la limite autorisée.                                          |
| 500  | Erreur interne du serveur | Une anomaly est survenue lors de la récupération des données dans la feuille de calcul.                 |

## Comment utiliser SplitTable avec les SDK

### Spécification de SplitTable

La [spécification de l’API SplitTable](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=fr-FR&password=SecretPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "Spreadsheet=@exemple.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "file": "flux binaire (archive ZIP ou classeur selon les paramètres)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[À définir]`
---
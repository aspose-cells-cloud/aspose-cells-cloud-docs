---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "SearchAllTextItemsInRemoteSpreadsheet"
type: docs
url: /fr/cells/{name}/search/content/all-textitems
aliases: []
keywords: "recherche, éléments texte, Aspose.Cells"
description: "Rechercher tous les éléments texte dans une feuille de calcul distante à l’aide d’Aspose.Cells Cloud."
weight: 100
---

## La méthode SearchAllTextItemsInRemoteSpreadsheet des services web Aspose.Cells Cloud

Cette méthode recherche tous les éléments texte présents dans un fichier de feuille de calcul distant. Elle prend en charge la recherche dans toutes les feuilles et cellules du classeur, en identifiant les occurrences du terme recherché. L’opération est effectuée dans le cloud, sans nécessiter de stockage local. Assurez-vous de disposer des autorisations nécessaires pour lire le fichier source. Si le fichier source est inaccessible ou si une erreur survient pendant le processus de recherche (par exemple, un format de fichier non pris en charge), une exception appropriée sera levée. Selon les détails d’implémentation, la méthode peut renvoyer les emplacements des correspondances (par exemple, nom de la feuille, coordonnées de la cellule).

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|-------------------------------------------------------|-------------|
| name             | string | Chemin                                                | Nom du fichier du classeur. |
| folder           | string | Chaîne de requête                                     | Chemin du dossier dans lequel le classeur est stocké. |
| storageName      | string | Chaîne de requête                                     | (Facultatif) Nom du stockage lors de l’utilisation d’un stockage cloud personnalisé. Utilise le stockage par défaut si omis. |
| region           | string | Chaîne de requête                                     | Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | string | Chaîne de requête                                     | Mot de passe requis pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [TBD]            |      | [TBD]       |

### **Réponse**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | La requête a abouti et la réponse contient tous les éléments texte trouvés dans la feuille de calcul. |
| 400  | Requête incorrecte | URL ou paramètres de requête non valides. |
| 401  | Non autorisé  | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 404  | Non trouvé    | Le fichier source est inaccessible. |
| 413  | Charge utile trop grande | La charge utile de la requête dépasse la taille autorisée. |
| 500  | Erreur interne du serveur | La feuille de calcul a rencontré une anomalie lors de l’extraction des données. |

## Comment utiliser SearchAllTextItemsInRemoteSpreadsheet à l’aide des SDK

### Spécification de SearchAllTextItemsInRemoteSpreadsheet

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet" rel="noopener noreferrer">spécification de l’API SearchAllTextItemsInRemoteSpreadsheet</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels vers l’API Cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Feuil1",
      "CellAddress": "A1",
      "Text": "Texte d’exemple"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[TBD]`
---
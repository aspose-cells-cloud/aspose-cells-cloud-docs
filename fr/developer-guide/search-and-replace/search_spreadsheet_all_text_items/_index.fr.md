---
title: "Rechercher tous les éléments textuels d'une feuille de calcul"
ArticleTitle: "Rechercher tous les éléments textuels d'une feuille de calcul – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Rechercher tous les éléments textuels d'une feuille de calcul"
type: docs
url: /fr/cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, Recherche, Éléments textuels, API"
description: "Rechercher tous les éléments textuels dans un fichier de feuille de calcul à l’aide de l’API Aspose.Cells Cloud."
weight: 100
---

## La recherche de tous les éléments textuels d'une feuille de calcul via les services web Aspose.Cells Cloud

Cette méthode recherche tous les éléments textuels présents dans un fichier de feuille de calcul local. Elle permet d’effectuer la recherche dans toutes les feuilles et cellules du classeur, identifiant ainsi les occurrences du terme recherché. L’opération est exécutée côté serveur cloud, sans nécessiter de stockage cloud. Assurez-vous de disposer des autorisations nécessaires pour lire le fichier source. Si le fichier source est inaccessible ou si une erreur survient pendant le processus de recherche (par exemple, un format de fichier non pris en charge), une exception appropriée sera levée. Selon les détails d’implémentation, la méthode peut renvoyer les emplacements des correspondances trouvées (par exemple, le nom de la feuille, les coordonnées de la cellule).

### Endpoint de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type | Emplacement (Chemin / Chaîne de requête / Corps HTTP) | Description |
|------------------|------|--------------------------------------------------------|-------------|
| Spreadsheet | Fichier | FormData | Télécharger le fichier de feuille de calcul. |
| region | Chaîne | Chaîne de requête | Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement propre à la locale. |
| password | Chaîne | Chaîne de requête | Mot de passe permettant d’ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [À déterminer] | [À déterminer] | [À déterminer] |

### **Réponse**

```json
{
  "SearchResults": [
    {
      "SheetName": "Feuille1",
      "CellName": "A1",
      "Text": "Exemple de texte"
    }
    // ... autres éléments
  ],
  "TotalCount": 42
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | La requête a abouti et la réponse contient tous les éléments textuels trouvés. |
| 400 | Requête incorrecte | URL invalide ou paramètres de requête mal formés. |
| 401 | Non autorisé | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 404 | Non trouvé | Le fichier source est inaccessible. |
| 413 | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite autorisée. |
| 500 | Erreur interne du serveur | Une anomaly est survenue lors de l’extraction des données dans la feuille de calcul. |

## Comment utiliser la recherche de tous les éléments textuels d'une feuille de calcul avec les SDK

### Spécification de la recherche de tous les éléments textuels d'une feuille de calcul

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems}" rel="noopener noreferrer">Spécification de l’API Recherche de tous les éléments textuels d'une feuille de calcul</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=fr-FR&password=monMotDePasse" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>" \
  -F "Spreadsheet=@exemple.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "SearchResults": [
    {
      "SheetName": "Feuille1",
      "CellName": "A1",
      "Text": "Exemple de texte"
    }
    // ... autres éléments
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
 `[À déterminer]`
---
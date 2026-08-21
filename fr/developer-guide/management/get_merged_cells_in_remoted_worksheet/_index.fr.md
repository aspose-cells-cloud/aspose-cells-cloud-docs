---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Obtenir les cellules fusionnées dans une feuille de calcul distante – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, obtenir les cellules fusionnées, feuille de calcul distante, API"
description: "Récupère toutes les zones de cellules fusionnées d'une feuille de calcul distante dans un fichier de calcul."
weight: 10
---

## La méthode GetMergedCellsInRemotedWorksheet des services web Aspose.Cells Cloud

Récupère toutes les zones de cellules fusionnées à partir d'une feuille de calcul distante.

### Point de terminaison de l'API web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type | Emplacement (chemin/chaîne de requête Corps HTTP) | Description |
|------------------|------|---------------------------------------------------|-------------|
| name | string | Chemin | Nom du fichier de calcul |
| worksheet | string | Chemin | Nom de la feuille de calcul |
| folder | string | Chaîne de requête | Chemin du fichier de calcul dans le stockage cloud |
| storageName | string | Chaîne de requête | (Facultatif) Nom du stockage personnalisé à utiliser. Utilise le stockage par défaut si omis. |
| region | string | Chaîne de requête | Paramètres régionaux/langue du fichier de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password | string | Chaîne de requête | Mot de passe nécessaire pour ouvrir le fichier de calcul |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| — | — | *Aucun* |

### **Réponse**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | La requête a abouti et la liste des zones de cellules fusionnées est renvoyée. |
| 400 | Mauvaise requête | URL invalide ou paramètres de requête mal formés. |
| 401 | Non autorisé | L'authentification a échoué, ou aucune information d'identification n’a été fournie. |
| 413 | Charge utile trop volumineuse | La taille de la charge utile de la requête dépasse la limite autorisée. |
| 500 | Erreur interne du serveur | Une anomaly est survenue lors de la récupération des données dans le fichier de calcul. |

## Comment utiliser GetMergedCellsInRemotedWorksheet avec les SDK

### Spécification de GetMergedCellsInRemotedWorksheet

La [spécification de l’API GetMergedCellsInRemotedWorksheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels vers l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/Exemple.xlsx/worksheets/Feuil1/mergedcells?folder=MonDossier&storageName=MonStockage&region=fr-FR&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
`[TBD]`
---
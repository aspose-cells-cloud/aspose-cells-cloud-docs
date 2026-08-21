---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "Obtenir les cellules fusionnées dans une feuille de calcul – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "GetMergedCellsInWorksheet"
type: docs
url: /cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, cellules fusionnées, feuille de calcul, API"
description: "Récupérer toutes les zones de cellules fusionnées d'une feuille de calcul locale."
weight: 1000
---

## Le service web Aspose.Cells Cloud Get Merged Cells In Worksheet

Récupérer toutes les zones de cellules fusionnées d'une feuille de calcul locale.

### Point de terminaison de l'API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|------|--------------------------------------------------------|-------------|
| Spreadsheet | Fichier | FormData | Télécharger le fichier de feuille de calcul. |
| worksheet | Chaîne | Chaîne de requête | Nom de la feuille de calcul. |
| region | Chaîne | Chaîne de requête | Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la localisation. |
| password | Chaîne | Chaîne de requête | Mot de passe pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| N/A | N/A | Cette opération n’accepte pas de corps JSON ; le fichier de feuille de calcul est envoyé via `multipart/form-data`. |

### **Réponse**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Les zones de cellules fusionnées ont été récupérées avec succès. |
| 400 | Requête incorrecte | Un ou plusieurs paramètres de requête sont invalides ou manquants. |
| 401 | Non autorisé | L’authentification a échoué – jeton JWT invalide ou manquant. |
| 413 | Charge utile trop volumineuse | Le fichier de feuille de calcul téléchargé dépasse la taille limite autorisée. |
| 500 | Erreur interne du serveur | Une erreur inattendue s’est produite côté serveur. |

## Comment utiliser le service Get Merged Cells In Worksheet avec les SDK

### Spécification du service Get Merged Cells In Worksheet

La [spécification de l’API Get Merged Cells In Worksheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'Spreadsheet=@exemple.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
 `[À compléter]`
---
---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "GetSpreadsheetStructure"
type: docs
url: /fr/cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, Structure de feuille de calcul, API"
description: "Convertit de manière structurée les métadonnées essentielles, les feuilles de calcul, les tableaux, les tableaux croisés dynamiques, les graphiques, les formes et autres informations d’un classeur Excel en un objet JSON de type JObject."
weight: 1000
---

## La méthode GetSpreadsheetStructure des services web Aspose.Cells Cloud

Convertit de manière structurée les métadonnées essentielles, les feuilles de calcul, les tableaux, les tableaux croisés dynamiques, les graphiques, les formes et autres informations d’un classeur Excel en un objet JSON de type JObject, pour des scénarios tels que l’exportation de données, les réponses d’API et l’enregistrement de journaux.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|--------------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData (corps)                                       | Télécharge le fichier de feuille de calcul. |
| region           | Chaîne  | Chaîne de requête                                      | Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Influence le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                      | Le mot de passe nécessaire pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type   | Description |
|------------------|--------|-------------|
| Spreadsheet      | Fichier | Télécharge le fichier de feuille de calcul. |

### **Réponse**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | La structure de la feuille de calcul a été récupérée avec succès. |
| 400 | Requête incorrecte | Paramètres de requête invalides ou format de fichier non valide. |
| 401 | Non autorisé | Échec de l’authentification ou absence de jeton JWT. |
| 413 | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille autorisée. |
| 500 | Erreur interne du serveur | Une erreur inattendue s’est produite côté serveur. |

## Comment utiliser GetSpreadsheetStructure avec les SDK

### Spécification de GetSpreadsheetStructure

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure" rel="noopener noreferrer">spécification de l’API GetSpreadsheetStructure</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose Cells Cloud. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>" \
  -F 'Spreadsheet=@exemple.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
`[TBD]`
---
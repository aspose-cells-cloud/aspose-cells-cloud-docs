---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Get Structure In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "GetStructureInRemoteSpreadsheet"
type: docs
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, spreadsheet, structure"
description: "Récupérer les métadonnées structurelles d’un classeur Excel distant, y compris les feuilles de calcul, les tableaux, les tableaux croisés dynamiques, les graphiques, les formes et d’autres informations essentielles."
weight: 100
---

## La fonction Get Structure In Remote Spreadsheet des services web Aspose.Cells Cloud

Convertir structurellement les métadonnées essentielles, les feuilles de calcul, les tableaux, les tableaux croisés dynamiques, les graphiques, les formes et autres informations d’un classeur Excel en un objet JSON de type JObject, pour des scénarios tels que l’exportation de données, les réponses d’API et l’enregistrement de journaux.

### Point de terminaison de l’API web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|------|--------------------------------------------------------|-------------|
| name | string | Chemin | Nom du fichier de feuille de calcul. |
| folder | string | Chaîne de requête | Dossier dans lequel le fichier est situé. (Optionnel) |
| storageName | string | Chaîne de requête | (Optionnel) Nom du stockage à utiliser si vous utilisez un stockage cloud personnalisé. Utilise le stockage par défaut si omis. |
| region | string | Chaîne de requête | Paramètre régional/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password | string | Chaîne de requête | Mot de passe nécessaire pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

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
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Structure du classeur récupérée avec succès. |
| 400 | Requête incorrecte | Paramètres de requête non valides. |
| 401 | Non autorisé | Échec de l’authentification ou jeton manquant. |
| 413 | Charge utile trop volumineuse | La charge utile de la requête dépasse la taille autorisée. |
| 500 | Erreur interne du serveur | Erreur inattendue du serveur. |

## Comment utiliser Get Structure In Remote Spreadsheet avec les SDK

### Spécification de Get Structure In Remote Spreadsheet

La [spécification de l’API Get Structure In Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[TBD]`
---
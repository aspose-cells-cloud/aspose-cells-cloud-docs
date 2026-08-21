---
title: "Obtenir les feuilles de calcul avec un classeur local"
ArticleTitle: "Obtenir les feuilles de calcul avec un classeur local – Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /fr/cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, feuilles de calcul, classeur local, API"
description: "Récupère la liste complète des feuilles de calcul à partir du classeur local actuellement actif."
weight: 1000
---

## L'API Get Worksheets With Local Spreadsheet des services web Aspose.Cells Cloud

Ce point de terminaison accède à l'application de classeur locale (par exemple, Excel) via l'interopérabilité ou une API locale, collecte le nom et le type (par exemple, standard, graphique, macro) de chaque feuille de calcul, puis renvoie cette collection sous forme de tableau JSON structuré. Elle est généralement utilisée pour alimenter une interface utilisateur de sélection de feuille de calcul ou pour auditer le contenu d'un classeur.

### Point de terminaison de l'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|--------------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData (corps HTTP)                                  | Télécharger le fichier de classeur. |
| region           | Chaîne  | Chaîne de requête                                       | Paramètre de région/langue du classeur (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l'analyse des dates et le comportement spécifique à la locale. *(facultatif)* |
| password         | Chaîne  | Chaîne de requête                                       | Mot de passe pour ouvrir le fichier de classeur. *(facultatif)* |

### Paramètre du corps de la requête

| Nom du paramètre | Type   | Description |
|------------------|--------|-------------|
| Spreadsheet      | Fichier | Télécharger le fichier de classeur. |

### **Réponse**

```json
{
  "Worksheets": [
    {
      "Name": "Feuil1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Graphique1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... feuilles de calcul supplémentaires
  ]
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | La liste des feuilles de calcul a été récupérée avec succès. |
| 400 | Requête incorrecte | Requête invalide (par exemple, URL mal formée ou données obligatoires manquantes). |
| 401 | Non autorisé | L'authentification a échoué ou aucune information d'identification n'a été fournie. |
| 404 | Non trouvé | Le fichier source n'est pas accessible. |
| 413 | Payload trop volumineux | Le fichier téléversé dépasse la limite de taille autorisée. |
| 500 | Erreur interne du serveur | Une anomalie s'est produite lors de la récupération des données à partir du classeur. |

## Comment utiliser Get Worksheets With Local Spreadsheet avec les SDK

### Spécification de Get Worksheets With Local Spreadsheet

La [spécification de l'API Get Worksheets With Local Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=fr-FR&password=votreMotDePasse" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
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
      "Name": "Feuil1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Graphique1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... feuilles de calcul supplémentaires
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

Utiliser un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK abstracte les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[À définir]`
---
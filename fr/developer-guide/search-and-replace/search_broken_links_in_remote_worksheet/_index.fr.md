---
title: "Rechercher les liens rompus dans une feuille de calcul distante"
ArticleTitle: "Rechercher les liens rompus dans une feuille de calcul distante – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /fr/cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, Rechercher les liens rompus, Feuille de calcul distante"
description: "Recherche les liens rompus dans la feuille de calcul d’un classeur distant."
weight: 100
---

## La recherche de liens rompus dans une feuille de calcul distante des services web Aspose.Cells Cloud

Cette méthode recherche les liens rompus dans une feuille de calcul d’un fichier de classeur stocké dans un stockage cloud distant. Elle analyse toutes les feuilles et cellules afin d’identifier les hyperliens qui ne pointent plus vers des destinations valides, tels que des URL inaccessibles ou des références externes manquantes. L’opération est exécutée à distance dans l’environnement cloud, sans nécessiter le téléchargement du fichier sur la machine locale.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type | Emplacement (chemin/chaîne de requête Corps HTTP) | Description |
|------------------|------|----------------------------------------------------|-------------|
| name | string | Chemin | Le nom du fichier de classeur dans lequel effectuer la recherche. |
| worksheet | string | Chemin | Spécifie la feuille de calcul concernée par la recherche. |
| folder | string | Chaîne de requête | Le chemin du dossier dans lequel le classeur est stocké. (facultatif) |
| storageName | string | Chaîne de requête | (Facultatif) Le nom du stockage lorsqu’un stockage cloud personnalisé est utilisé. Le stockage par défaut est utilisé si ce paramètre est omis. |
| region | string | Chaîne de requête | Paramètre régional/langue du classeur (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password | string | Chaîne de requête | Le mot de passe nécessaire pour ouvrir le fichier de classeur. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| — | — | Aucun corps de requête n’est requis pour cette opération. |

### **Réponse**

```json
{
  "Links": [
    {
      "SheetName": "Feuil1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | La liste des liens rompus a été récupérée avec succès. |
| 400 | Mauvaise requête | Paramètres de requête invalides ou URL mal formée. |
| 401 | Non autorisé | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 404 | Non trouvé | Le fichier source n’est pas accessible. |
| 413 | Entité de requête trop grande | La taille de l’entité de la requête dépasse la limite autorisée. |
| 500 | Erreur interne du serveur | Une anomalie s’est produite lors de la récupération des données du classeur. |

## Comment utiliser la recherche de liens rompus dans une feuille de calcul distante à l’aide des SDK

### Spécification de la recherche de liens rompus dans une feuille de calcul distante

La [spécification de l’API Rechercher les liens rompus dans une feuille de calcul distante](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Feuil1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[TBD]`
---
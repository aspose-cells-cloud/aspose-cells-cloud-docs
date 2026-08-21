---
title: "Supprimer des caractères dans une feuille de calcul distante"
ArticleTitle: "Supprimer des caractères dans une feuille de calcul distante – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Supprimer des caractères dans une feuille de calcul distante"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, supprimer des caractères, traitement de texte"
description: "Supprime des caractères définis par l'utilisateur, des ensembles de symboles prédéfinis ou toute sous-chaîne de chaque cellule de la plage sélectionnée, tout en conservant les formules, le formatage et la validation des données pour une feuille de calcul distante."
weight: 100
---

## La fonctionnalité Supprimer des caractères dans une feuille de calcul distante des services web Aspose.Cells Cloud

Supprime des caractères définis par l'utilisateur, des ensembles de symboles prédéfinis ou toute sous-chaîne de chaque cellule de la plage sélectionnée, tout en conservant les formules, le formatage et la validation des données pour une feuille de calcul distante.

### Point de terminaison de l'API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre    | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                                       |
|---------------------|---------|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                | string  | Chemin                                                 | (Requis) Le nom du fichier classeur à récupérer.                                                                                                                                 |
| worksheet           | string  | Chemin                                                 | Spécifie la feuille de calcul de la feuille de calcul.                                                                                                                           |
| range               | string  | Chemin                                                 | Spécifie la plage de la feuille de calcul.                                                                                                                                       |
| removeTextMethod    | string  | Chaîne de requête                                      | Spécifie le type de méthode de suppression de texte.                                                                                                                             |
| characterSets       | string  | Chaîne de requête                                      | Spécifie les jeux de caractères.                                                                                                                                                 |
| removeCustomValue   | string  | Chaîne de requête                                      | Spécifie la valeur personnalisée à supprimer.                                                                                                                                    |
| caseSensitive       | boolean | Chaîne de requête                                      | Affecte le mode `Substring` et `CustomChars` lorsqu'il est activé.                                                                                                               |
| folder              | string  | Chaîne de requête                                      | (Facultatif) Le chemin du dossier où le classeur est stocké. La valeur par défaut est null.                                                                                    |
| storageName         | string  | Chaîne de requête                                      | (Facultatif) Le nom du stockage si vous utilisez un stockage cloud personnalisé. Utilise le stockage par défaut s'il est omis.                                                 |
| region              | string  | Chaîne de requête                                      | Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Influence le formatage des nombres, l'analyse des dates et le comportement spécifique à la locale. |
| password            | string  | Chaîne de requête                                      | Le mot de passe pour ouvrir le fichier de feuille de calcul.                                                                                                                     |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| *Aucun*          | *Aucun* | Cette opération ne nécessite pas de corps de requête. |

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Les caractères ont été supprimés avec succès.",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Les caractères ont été supprimés avec succès et le classeur a été mis à jour. |
| 400 | Requête incorrecte | Un ou plusieurs paramètres sont manquants ou non valides. |
| 401 | Non autorisé | L'authentification a échoué : jeton JWT manquant ou non valide. |
| 413 | Charge utile trop volumineuse | La taille de la requête dépasse la limite autorisée. |
| 500 | Erreur interne du serveur | Une erreur inattendue s'est produite côté serveur. |

## Comment utiliser la fonction Supprimer des caractères dans une feuille de calcul distante avec les SDK

### Spécification de la fonction Supprimer des caractères dans une feuille de calcul distante

La [spécification de l'API Supprimer des caractères dans une feuille de calcul distante](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) définit une interface de programmation accessible publiquement et permet d'effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l'outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L'exemple suivant montre comment effectuer des appels à l'API cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Les caractères ont été supprimés avec succès.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Exemple.xlsx",
      "Path": "/documents/Exemple.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L'utilisation d'un SDK est le moyen le plus rapide d'accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
`[À compléter]`
---

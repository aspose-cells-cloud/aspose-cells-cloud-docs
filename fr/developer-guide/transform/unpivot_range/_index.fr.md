---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "UnpivotRange"
type: docs
url: /fr/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "Inverser les lignes et les colonnes dans la feuille de calcul."
weight: 10
---

## L'UnpivotRange des services Web Aspose.Cells Cloud

Inversez les lignes et les colonnes dans la feuille de calcul.

### Point de terminaison de l'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|------|--------------------------------------------------------|-------------|
| Spreadsheet | Fichier | FormData | Télécharger le fichier de feuille de calcul. |
| worksheet | chaîne | Chaîne de requête | Le nom de la feuille de calcul. |
| cellArea | chaîne | Chaîne de requête | Une plage de données spécifiée. |
| skipEmptyValue | booléen | Chaîne de requête | Si la valeur est true, les valeurs vides sont ignorées. Valeur par défaut : true. |
| outPath | chaîne | Chaîne de requête | (Facultatif) Le chemin du dossier dans lequel le classeur est stocké. La valeur par défaut est null. |
| outStorageName | chaîne | Chaîne de requête | Nom du stockage pour le fichier de sortie. |
| region | chaîne | Chaîne de requête | Paramètre régional/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement propre à la locale. |
| password | chaîne | Chaîne de requête | Le mot de passe permettant d’ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
|------------------|------|-------------|
| — | — | — |

### **Réponse**

```json
{
  "File": "flux binaire"
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Le fichier de feuille de calcul non croisé (unpivoted) est renvoyé. |
| 400 | Mauvaise requête | Paramètres de requête non valides. |
| 401 | Non autorisé | Échec de l’authentification. |
| 413 | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite. |
| 500 | Erreur interne du serveur | Le serveur a rencontré une condition inattendue. |

## Comment utiliser UnpivotRange avec les SDK

### Spécification de UnpivotRange

La [spécification de l’API UnpivotRange](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jeton jwt>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
 `[À compléter]`
---
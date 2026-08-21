---
title: "Dépivoter un tableau"
ArticleTitle: "Dépivoter un tableau – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "Dépivoter un tableau"
type: docs
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, dépivoter, transformer"
description: "Permuter les lignes et les colonnes dans la feuille de calcul."
weight: 1
---

## Le dépivoteur de tableau des services web Aspose.Cells Cloud

Permuter les lignes et les colonnes dans la feuille de calcul.

### Endpoint de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|---------|--------------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData                                               | Télécharger le fichier de feuille de calcul. |
| worksheet        | Chaîne  | Chaîne de requête                                      | Nom de la feuille de calcul. |
| index            | Entier  | Chaîne de requête                                      | Plage de données spécifiée. |
| skipEmptyValue   | Booléen | Chaîne de requête                                      | Ignorer les valeurs vides (par défaut : true). |
| outPath          | Chaîne  | Chaîne de requête                                      | (Facultatif) Chemin du dossier où le classeur est stocké. Par défaut : null. |
| outStorageName   | Chaîne  | Chaîne de requête                                      | Nom du stockage pour le fichier de sortie. |
| region           | Chaîne  | Chaîne de requête                                      | Paramètres régionaux/langue de la feuille de calcul (par ex., `en-US`, `fr-FR`). Influe sur le formatage des nombres, l’analyse des dates et le comportement propre à la localisation. |
| password         | Chaîne  | Chaîne de requête                                      | Mot de passe permettant d’ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| N/A              | N/A  | Aucun paramètre dans le corps de la requête. |

### **Réponse**

```json
{
  "File": "flux binaire de la feuille de calcul dépivrée"
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | Le fichier de feuille de calcul dépivrée est renvoyé. |
| 400  | Requête incorrecte | Paramètres de requête non valides. |
| 401  | Non autorisé | Échec de l’authentification ou jeton JWT manquant/non valide. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille maximale autorisée. |
| 500  | Erreur interne du serveur | Erreur inattendue survenue sur le serveur. |

## Comment utiliser le dépivoteur de tableau avec les SDK

### Spécification du dépivoteur de tableau

La [spécification de l’API Dépivoteur de tableau](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "Spreadsheet=@exemple.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "flux binaire de la feuille de calcul dépivrée"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
 `[À compléter]`
---
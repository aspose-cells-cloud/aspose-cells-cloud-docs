---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "TransposeData"
type: docs
url: /cells/transpose
aliases: ["/cells/transpose"]
keywords: "TransposeData, Aspose.Cells, API cloud, feuille de calcul, transposition"
description: "Échange les lignes et les colonnes dans la feuille de calcul."
weight: 1000
---

## TransposeData des services web Aspose.Cells Cloud

Échange les lignes et les colonnes dans la feuille de calcul.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin/chaîne de requête/ Corps HTTP) | Description                                                                                                                                                   |
|------------------|--------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fichier | FormData                                           | Téléchargement du fichier de feuille de calcul.                                                                                                              |
| worksheet        | Chaîne  | Chaîne de requête                                   | Nom de la feuille de calcul.                                                                                                                                  |
| cellArea         | Chaîne  | Chaîne de requête                                   | Plage de données spécifiée.                                                                                                                                   |
| outPath          | Chaîne  | Chaîne de requête                                   | (Facultatif) Chemin du dossier où le classeur est stocké. La valeur par défaut est null.                                                                    |
| outStorageName   | Chaîne  | Chaîne de requête                                   | Nom du stockage pour le fichier de sortie.                                                                                                                    |
| region           | Chaîne  | Chaîne de requête                                   | Paramètre de région/langue de la feuille de calcul (par ex., `fr-FR`, `en-US`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                   | Mot de passe pour ouvrir le fichier de feuille de calcul.                                                                                                     |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [TBD]            | [TBD] | [TBD]       |

### **Réponse**

```json
{
  "file": "flux binaire de la feuille de calcul transposée"
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Le fichier de feuille de calcul transposée est renvoyé. |
| 400 | Mauvaise requête | Paramètres d’entrée invalides ou requête mal formée. |
| 401 | Non autorisé | Échec de l’authentification ou jeton JWT manquant/invalide. |
| 413 | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite autorisée. |
| 500 | Erreur interne du serveur | Erreur serveur inattendue. |

## Comment utiliser TransposeData avec les SDK

### Spécification de TransposeData

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}" rel="noopener noreferrer">spécification de l’API TransposeData</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Feuil1&cellArea=A1:C10&outPath=output%2Fdossier&outStorageName=MonStockage&region=fr-FR&password=MonMotDePasse" \
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
  "file": "flux binaire de la feuille de calcul transposée"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK abstractise les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
`[TBD]`
---
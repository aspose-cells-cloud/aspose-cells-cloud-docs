---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "FlipData"
type: docs
url: /fr/cells/flip
aliases: []
keywords: "FlipData, Transposition, Aspose.Cells"
description: "Transpose une plage de données spécifiée dans un fichier de feuille de calcul."
weight: 100
---

## Le FlipData des services web Aspose.Cells Cloud

Cette API inverse l'orientation d'une matrice de données donnée. Par exemple, une plage de 3x2 (3 lignes, 2 colonnes) deviendra une plage de 2x3 (2 lignes, 3 colonnes) dans la sortie. Elle est couramment utilisée pour restructurer les données afin de répondre aux exigences d'entrée de différents graphiques, rapports ou modèles de données.

### Point de terminaison de l'API web

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|---------|-------------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData                                              | Télécharger le fichier de feuille de calcul. |
| worksheet        | Chaîne  | Chaîne de requête                                     | Le nom de la feuille de calcul. |
| cellArea         | Chaîne  | Chaîne de requête                                     | Une plage de données spécifiée. |
| Horizontal       | Booléen | Chaîne de requête                                     | Retournement horizontal/vertical. Valeur par défaut : true |
| outPath          | Chaîne  | Chaîne de requête                                     | (Facultatif) Le chemin du dossier où le classeur est stocké. Par défaut : null. |
| outStorageName   | Chaîne  | Chaîne de requête                                     | Nom du stockage pour le fichier de sortie. |
| region           | Chaîne  | Chaîne de requête                                     | Paramètre régional/langue de la feuille de calcul (par exemple, `fr-FR`, `en-US`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                     | Le mot de passe pour ouvrir le fichier de feuille de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| *Aucun*          | *N/A* | *Aucun corps JSON supplémentaire n’est requis ; le fichier est envoyé en tant que multipart/form-data.* |

### **Réponse**

```json
{
  "File": "<flux binaire du classeur transformé>"
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | L’opération s’est terminée avec succès et le fichier de feuille de calcul transformé est renvoyé. |
| 400  | Requête incorrecte | Un ou plusieurs paramètres requis sont manquants ou non valides. |
| 401  | Non autorisé  | Échec de l’authentification – jeton JWT manquant ou non valide. |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille autorisée. |
| 500  | Erreur interne du serveur | Une erreur inattendue s’est produite sur le serveur. |

## Comment utiliser le FlipData avec les SDK

### Spécification du FlipData

La [spécification de l’API FlipData](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=fr-FR&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "Spreadsheet=@exemple.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<flux binaire du classeur transformé>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
 `[À définir]`
---
---
title: "Convertir une feuille de calcul en table HTML"
ArticleTitle: "Convertir une feuille de calcul en table HTML – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /fr/cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, Table HTML, API"
description: "Convertit une feuille de calcul d’un fichier de calcul local en fichier de table HTML à l’aide d’Aspose.Cells Cloud."
weight: 100
---

## La conversion de feuille de calcul en table HTML des services web Aspose.Cells Cloud

Cette opération lit un fichier de calcul à partir du système de fichiers local, convertit sa feuille de calcul spécifiée en table HTML, puis renvoie le résultat converti sous forme de flux binaire. La conversion est effectuée entièrement sur le serveur cloud, donc aucune téléversement intermédiaire vers le stockage cloud n’est nécessaire. Elle prend en charge les paramètres régionaux optionnels et les classeurs protégés par mot de passe.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|-------------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData                                             | Téléverser le fichier de calcul. |
| worksheet        | Chaîne  | Chaîne de requête                                     | Nom de la feuille de calcul à convertir. (obligatoire) |
| region           | Chaîne  | Chaîne de requête                                     | Paramètres régionaux/langue du fichier de calcul (par exemple, `fr-FR`, `en-US`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                     | Mot de passe permettant d’ouvrir le fichier de calcul. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| *Aucun* | *Aucun* | *Aucun corps JSON n’est requis ; le fichier est envoyé en tant que multipart/form-data.* |

### **Réponse**

```json
{
  "File": "flux binaire de la table HTML générée"
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | La feuille de calcul a été convertie avec succès en table HTML et renvoyée sous forme de flux binaire. |
| 400 | Requête incorrecte | URL de requête invalide ou paramètres obligatoires manquants. |
| 401 | Non autorisé | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 404 | Introuvable | Le fichier source n’est pas accessible. |
| 500 | Erreur interne du serveur | Une anomalie s’est produite lors de la récupération des données de conversion à partir du fichier de calcul. |
| 413 | Charge utile trop volumineuse | Le fichier téléversé dépasse la limite de taille autorisée. |

## Comment utiliser la conversion de feuille de calcul en table HTML avec les SDK

### Spécification de la conversion de feuille de calcul en table HTML

La [spécification de l’API Convert Worksheet To Html Table](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) définit une interface de programmation publiquement accessible et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton JWT>" \
  -F "Spreadsheet=@exemplaire.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "flux binaire de la table HTML générée"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[À compléter]`
---
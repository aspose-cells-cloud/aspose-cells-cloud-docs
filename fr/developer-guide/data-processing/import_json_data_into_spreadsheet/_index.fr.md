---
title: "Importer des données JSON dans un classeur"
ArticleTitle: "Importer des données JSON dans un classeur – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /cells/import/data/json
aliases: []
keywords: "import JSON, Aspose.Cells, classeur, API"
description: "Importe un fichier de données JSON dans un classeur local."
weight: 1
---

## Importation de données JSON dans un classeur via les services web Aspose.Cells Cloud

Importe un fichier de données JSON dans un classeur local. Cette méthode analyse le JSON, mappe les données vers la structure des cellules du classeur, puis enregistre le fichier localement. Les formats de classeur pris en charge incluent .xlsx et .ods.

### Endpoint de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|--------|--------------------------------------------------------|-------------|
| datafile         | Fichier| FormData                                               | Téléchargement du fichier de données. |
| Spreadsheet      | Fichier| FormData                                               | Téléchargement du fichier de classeur. |
| worksheet        | Chaîne | Chaîne de requête                                      | Feuille de calcul dans laquelle importer les données JSON. |
| startcell        | Chaîne | Chaîne de requête                                      | Position de départ pour l’importation des données. |
| insert           | Booléen| Chaîne de requête                                      | Contrôle le comportement d’insertion. true : insère les données ; false : remplace les données existantes. (Par défaut : true) |
| outPath          | Chaîne | Chaîne de requête                                      | (Facultatif) Chemin du dossier où le classeur est stocké. Par défaut : null. |
| outStorageName   | Chaîne | Chaîne de requête                                      | Nom du stockage de sortie. |
| fontsLocation    | Chaîne | Chaîne de requête                                      | Utiliser des polices personnalisées. |
| region           | Chaîne | Chaîne de requête                                      | Paramètre de région/langue du classeur (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la localisation. |
| password         | Chaîne | Chaîne de requête                                      | Mot de passe pour ouvrir le fichier de classeur. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [TBD]            | [TBD]| [TBD]       |

### **Réponse**

```json
{
  "file": "flux binaire"
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | Fichier généré et renvoyé avec succès. |
| 400  | Mauvaise requête | URL non valide. |
| 401  | Non autorisé | Échec de l’authentification ou absence de crédentials. |
| 404  | Non trouvé | Fichier source inaccessible. |
| 413  | Charge utile trop grande | [TBD] |
| 500  | Erreur interne du serveur | Une anomalie s’est produite lors de l’extraction des données dans le classeur. |

## Comment utiliser l’importation de données JSON dans un classeur avec les SDK

### Spécification de l’importation de données JSON dans un classeur

La [Spécification de l’API d’importation de données JSON dans un classeur](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}
{< tab tabNum="1" >}
```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "flux binaire"
}
```
{< /tab >}
{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :  
`[TBD]`
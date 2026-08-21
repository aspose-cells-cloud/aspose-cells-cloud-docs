---
title: "Importer des données XML dans une feuille de calcul"
ArticleTitle: "Importer des données XML dans une feuille de calcul – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /fr/cells/import/data/xml
aliases: []
keywords: "Importer XML, Aspose.Cells, API"
description: "Importer un fichier de données XML dans une feuille de calcul locale à l’aide d’Aspose.Cells Cloud."
weight: 1000
---

## L’importation de données XML dans une feuille de calcul des services web Aspose.Cells Cloud

Importer un fichier de données XML dans une feuille de calcul locale. Cette méthode analyse le fichier XML, mappe les données à la structure de cellules de la feuille de calcul, puis enregistre le fichier localement. Les formats de feuille de calcul pris en charge incluent .xlsx et .ods.

### Endpoint de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (Chemin/Chaîne de requête/Corps HTTP) | Description                                                                                                                            |
|------------------|---------|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile         | Fichier | FormData                                          | Télécharger le fichier de données.                                                                                                      |
| Spreadsheet      | Fichier | FormData                                          | Télécharger le fichier de feuille de calcul.                                                                                           |
| worksheet        | Chaîne  | Chaîne de requête                                 | Spécifie la feuille de calcul dans laquelle importer les données XML.                                                                  |
| startcell        | Chaîne  | Chaîne de requête                                 | Position de départ pour l’importation des données.                                                                                     |
| insert           | Booléen | Chaîne de requête                                 | Contrôle le comportement d’insertion. `true` : insère les données ; `false` : remplace les données existantes. Par défaut : **true** |
| outPath          | Chaîne  | Chaîne de requête                                 | (Facultatif) Chemin du dossier où le classeur est stocké. La valeur par défaut est null.                                             |
| outStorageName   | Chaîne  | Chaîne de requête                                 | Nom du stockage pour le fichier de sortie.                                                                                             |
| fontsLocation    | Chaîne  | Chaîne de requête                                 | Utiliser des polices personnalisées.                                                                                                    |
| region           | Chaîne  | Chaîne de requête                                 | Paramètre de région/langue de la feuille de calcul (par ex. `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                 | Mot de passe pour ouvrir le fichier de feuille de calcul.                                                                              |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
|------------------|------|-------------|
| *Aucun*          | -    | -           |

### **Réponse**

```json
{
  "file": "<flux binaire de la feuille de calcul mise à jour>"
}
```

**Codes de statut de réponse**

| Code | Signification             | Description                                                                                           |
|------|---------------------------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                        | Les données XML ont été importées avec succès et le fichier de feuille de calcul mis à jour est renvoyé. |
| 400  | Requête incorrecte        | URL de requête invalide ou paramètres obligatoires manquants.                                        |
| 401  | Non autorisé              | L’authentification a échoué ou aucune information d’identification n’a été fournie.                  |
| 404  | Introuvable               | Le fichier source n’est pas accessible.                                                               |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille autorisée.                                         |
| 500  | Erreur interne du serveur | Une anomalies est survenue lors de la récupération des données dans la feuille de calcul.            |

## Comment utiliser l’importation de données XML dans une feuille de calcul avec les SDK

### Spécification de l’importation de données XML dans une feuille de calcul

La [spécification de l’API Import XML Data Into Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "datafile=@{NomFichierDonnées}" \
  -F "Spreadsheet=@{NomFichierFeuilleCalcul}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<flux binaire de la feuille de calcul mise à jour>"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
`[À définir]`
---
---
title: "Importer des données CSV dans un fichier de calcul"
ArticleTitle: "Importer des données CSV dans un fichier de calcul – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "Importer des données CSV dans un fichier de calcul"
type: docs
url: /cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, import CSV, fichier de calcul, API"
description: "Importer un fichier de données CSV dans un fichier de calcul local à l’aide de l’API Aspose.Cells Cloud."
weight: 100
---

## Importation de données CSV dans un fichier de calcul via les services web Aspose.Cells Cloud

Importe un fichier de données CSV dans un fichier de calcul local. Cette méthode analyse le fichier CSV, mappe les données à la structure de cellules du fichier de calcul, puis enregistre le fichier localement. Les formats de fichiers de calcul pris en charge incluent .xlsx et .ods.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre      | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                          |
|-----------------------|---------|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| datafile              | Fichier | FormData                                               | Téléchargement du fichier de données.                                                                                               |
| Spreadsheet           | Fichier | FormData                                               | Téléchargement du fichier de calcul.                                                                                                |
| worksheet             | Chaîne  | Chaîne de requête                                       | Feuille de calcul dans laquelle importer les données CSV. (obligatoire)                                                             |
| startcell             | Chaîne  | Chaîne de requête                                       | Position de départ pour l’importation des données. (obligatoire)                                                                   |
| insert                | Booléen | Chaîne de requête                                       | Contrôle le comportement d’insertion. true : insère les données ; false : remplace les données existantes. Valeur par défaut : true (facultatif) |
| convertNumericData    | Booléen | Chaîne de requête                                       | Indique si les chaînes du fichier texte doivent être converties en données numériques. Valeur par défaut : true (facultatif)      |
| splitter              | Chaîne  | Chaîne de requête                                       | Délimiteur utilisé pour découper les champs CSV. Valeur par défaut : "," (facultatif)                                              |
| outPath               | Chaîne  | Chaîne de requête                                       | (Facultatif) Chemin du dossier dans lequel le classeur est enregistré. Par défaut : null.                                         |
| outStorageName        | Chaîne  | Chaîne de requête                                       | Nom du stockage de destination. (facultatif)                                                                                        |
| fontsLocation         | Chaîne  | Chaîne de requête                                       | Utilisation de polices personnalisées. (facultatif)                                                                                 |
| region                | Chaîne  | Chaîne de requête                                       | Paramètre régional/langue du fichier de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. (facultatif) |
| password              | Chaîne  | Chaîne de requête                                       | Mot de passe pour ouvrir le fichier de calcul. (facultatif)                                                                        |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Réponse**

```json
{
  "file": "<flux binaire du fichier de calcul résultant>"
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Les données CSV ont été importées avec succès et le fichier de calcul résultant est renvoyé. |
| 400 | Mauvaise requête | Paramètres de requête invalides ou URL mal formée. |
| 401 | Non autorisé | L’authentification a échoué ou aucune information d’identification n’a été fournie. |
| 404 | Non trouvé | Le fichier source n’est pas accessible. |
| 413 | Charge utile trop grande | Les fichiers téléchargés dépassent la limite de taille autorisée. |
| 500 | Erreur interne du serveur | Une anomalie s’est produite lors de l’obtention des données par le fichier de calcul. |

## Comment utiliser l’importation de données CSV dans un fichier de calcul à l’aide des SDK

### Spécification de l’importation de données CSV dans un fichier de calcul

La [spécification de l’API d’importation de données CSV dans un fichier de calcul](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Feuil1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=dossierSortie&outStorageName=MonStockage&fontsLocation=/polices/personnalisees&region=fr-FR&password=MonMotDePasse" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "datafile=@exemple.csv" \
  -F "Spreadsheet=@classeur.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<flux binaire du fichier de calcul résultant>"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
 `[TBD]`
---
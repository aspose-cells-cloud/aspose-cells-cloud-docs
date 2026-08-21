---
title: "Aspose.Cells Cloud – Fusionner, découper & importer des données de feuille de calcul"
second_title: "Document"
ArticleTitle: "Traitement des données de feuille de calcul – Fusionner, découper & importer"
linktitle: "Traitement des données"
type: docs
url: /data-processing/
keywords: "Aspose.Cells Cloud, traitement des données de feuille de calcul, fusion Excel, découpage Excel, import CSV, import JSON, API"
description: "Guide détaillé pour l’importation de données CSV/JSON, la fusion de classeurs Excel distants et le découpage de grandes feuilles de calcul à l’aide de l’API REST Aspose.Cells Cloud, incluant des exemples de requêtes/réponses."
weight: 30
---

**Aspose.Cells Cloud** – un service RESTful permettant la manipulation programmatique de fichiers Excel dans le cloud. Il prend en charge l’importation de données à partir de divers formats, la fusion de classeurs et le découpage de grandes feuilles de calcul.

La section **Traitement des données** de l’API Aspose.Cells Cloud vous permet d’importer, de fusionner et de découper programmatiquement des données de feuilles de calcul. Utilisez les points de terminaison ci-dessous pour gérer les importations CSV/JSON, combiner des classeurs ou découper de grands fichiers en éléments plus petits et gérables.

## Importation et gestion des données

- **[Importer des données CSV, JSON, XML dans des fichiers Excel](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

L’opération d’importation accepte des charges utiles au format CSV, JSON ou XML et crée une nouvelle feuille de calcul (ou met à jour une feuille existante) dans le classeur cible.

**Détails du point de terminaison**

| Méthode HTTP | Point de terminaison | Corps de la requête | Réponse en cas de succès |
|-------------|----------------------|---------------------|--------------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` ou `text/csv` (selon le format) | `200 OK` avec JSON contenant les métadonnées du classeur mis à jour |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *aucun* | Retourne le fichier de classeur traité |

**Exemple de requête cURL (import CSV)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**Exemple de réponse JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **Conditions préalables** : Un jeton d’accès OAuth2 est requis. Le fichier source doit se trouver dans le stockage Aspose Cloud ou être fourni via un téléchargement multipart.

## Opération de fusion de fichiers

- **[Fusionner des fichiers Excel distants dans un classeur spécifié](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[Fusionner plusieurs fichiers Excel dans un seul classeur](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Fusionner des fichiers Excel correspondant à un motif dans un dossier distant](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

La fusion combine deux classeurs ou plus en un seul classeur cible. L’API prend en charge à la fois les listes explicites de fichiers et les fusions basées sur des motifs dans un dossier de stockage.

**Détails du point de terminaison**

| Méthode HTTP | Point de terminaison | Paramètres | Réponse en cas de succès |
|-------------|----------------------|------------|--------------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (tableau de noms de fichiers), `target` (nom optionnel du classeur cible) | `200 OK` avec JSON décrivant le classeur fusionné |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` avec les métadonnées du classeur fusionné |

**Exemple de requête cURL (fusion d’une liste explicite)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**Exemple de réponse JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **Conditions préalables** : Tous les classeurs sources doivent être stockés au même emplacement dans le stockage cloud, et l’appelant doit disposer des autorisations de lecture/écriture.

## Opération de découpage de fichiers

- **[Découper un fichier Excel en plusieurs fichiers selon les feuilles de calcul](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[Découper un fichier Excel selon des règles personnalisées](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

Le découpage extrait des feuilles de calcul individuelles ou des groupes de lignes/colonnes vers des fichiers de classeur distincts.

**Détails du point de terminaison**

| Méthode HTTP | Point de terminaison | Paramètres | Réponse en cas de succès |
|-------------|----------------------|------------|--------------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (ex. `worksheet`), `outputFolder` | `200 OK` avec liste des URL des fichiers générés |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | JSON de règle personnalisée (taille de page, plage de lignes, etc.) | `200 OK` avec détails des fichiers découpés |

**Exemple de requête cURL (découpage selon les feuilles de calcul)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**Exemple de réponse JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **Conditions préalables** : Le classeur source doit être accessible dans le stockage Aspose Cloud, et l’appelant doit disposer des autorisations d’écriture dans le dossier de destination.
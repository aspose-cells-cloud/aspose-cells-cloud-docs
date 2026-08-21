---
title: "Supprimer les colonnes vides d’un fichier Excel avec l’API Aspose.Cells Cloud – Exemple rapide en REST"
second_title: "Document"
ArticleTitle: "Comment supprimer les colonnes vides dans Excel – Automatiser le nettoyage des colonnes"
linktitle: "Supprimer les colonnes vides"
type: docs
url: /delete-spreadsheet-blank-columns/
keywords: "supprimer les colonnes vides API Excel, Aspose.Cells Cloud, API REST, nettoyage Excel, automatisation des feuilles de calcul"
description: "Découvrez comment supprimer les colonnes vides des fichiers Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint, l’authentification, des exemples de requête/réponse et du code SDK en C#, Java, Python, etc."
weight: 100
---

Utilisez l’API Aspose.Cells Cloud pour supprimer automatiquement toutes les colonnes vides des feuilles Excel. Notre API intelligente détecte et supprime les colonnes dont les cellules ne contiennent aucune donnée, formule, commentaire, graphique ni objet. L’API prend en charge le traitement par lots, l’automatisation cloud et une intégration REST transparente pour des flux de travail de nettoyage de feuilles de calcul adaptés aux besoins des entreprises.

**Contexte :**  
Les colonnes vides apparaissent souvent après des importations de données, la génération de modèles ou des migrations de fichiers hérités. Supprimer ces colonnes vides améliore la taille du fichier, les performances d’affichage et la précision du traitement des données en aval. L’API *Delete Spreadsheet Blank Columns* permet de nettoyer rapidement les feuilles de calcul côté serveur, sans intervention manuelle.

## **DeleteSpreadsheetBlankColumns API**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête

| Nom du paramètre   | Type   | Emplacement                  | Description                                                                                                                      |
|--------------------|--------|------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **Spreadsheet**    | Fichier | Données de formulaire (multipart) | Le classeur Excel à traiter.                                                                                                    |
| **outPath**        | Chaîne  | Requête                      | Facultatif. Dossier de destination dans le stockage cloud pour le fichier nettoyé. Si omis, le résultat est renvoyé dans le corps de la réponse. |
| **outStorageName** | Chaîne  | Requête                      | Facultatif. Nom du stockage cloud dans lequel le fichier de sortie doit être enregistré.                                       |
| **region**         | Chaîne  | Requête                      | Facultatif. Identifiant régional (par ex. `en-US`, `de-DE`).                                                                    |
| **password**       | Chaîne  | Requête                      | Facultatif. Mot de passe pour ouvrir un classeur protégé.                                                                       |

### Réponse

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Codes d’erreur

- **400 Bad Request** – Paramètres de requête invalides ou URI mal formé.
- **401 Unauthorized** – Jeton d’accès manquant ou invalide.
- **404 Not Found** – Le classeur spécifié est introuvable.
- **500 Server Error** – Une condition inattendue a empêché l’API de traiter le fichier.

## Quand utiliser l’API Delete Spreadsheet Blank Columns

- **Importation de données et nettoyage** – Supprimer immédiatement les colonnes vides finales ou structurelles après le chargement des données à partir de CSV, de bases de données ou d’API web.
- **Génération de rapports et tableaux de bord** – Garantir une mise en page propre dans les rapports finaux, sans colonnes vides inutiles.
- **Pipelines ETL** – Prétraiter les fichiers Excel avant de les charger dans des entrepôts de données tels que Snowflake ou BigQuery.
- **Intégration système** – Normaliser les fichiers Excel fournis par des partenaires avant leur traitement ultérieur.
- **Automatisation de documents en masse** – Supprimer les colonnes d’exemple des modèles générés par lots.
- **Contenu généré par les utilisateurs** – Nettoyer les fichiers Excel téléchargés via des portails web avant leur stockage ou analyse.
- **Migrations de données héritées** – Simplifier les anciennes archives de feuilles de calcul en supprimant les colonnes historiquement vides.

## Pourquoi utiliser cette API ?

- **Adaptée aux développeurs** – Des SDK sont disponibles pour C#, Java, Python, PHP, Ruby, Node.js, Go, etc., réduisant ainsi l’effort de développement.
- **Économique** – Tarification à l’usage élimine les coûts d’infrastructure initiale.
- **Aucune maintenance** – Aucun serveur à gérer ; le service est régulièrement mis à jour par Aspose.

## Comment utiliser l’API Delete Spreadsheet Blank Columns avec les SDK

### Spécification de l’API

La [Spécification de l’API Delete Spreadsheet Blank Columns](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankColumns) fournit la définition complète OpenAPI et des exemples.

### Utilisation des SDK Aspose.Cells Cloud

Les SDK abstraient les détails HTTP de bas niveau, permettant de supprimer les colonnes vides en quelques lignes seulement de code. Consultez le dépôt GitHub officiel pour une liste complète des langages pris en charge : <https://github.com/aspose-cells-cloud>.

Les exemples de code suivants montrent comment appeler l’API à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{</tab>}}
{{< /tabs >}}
---
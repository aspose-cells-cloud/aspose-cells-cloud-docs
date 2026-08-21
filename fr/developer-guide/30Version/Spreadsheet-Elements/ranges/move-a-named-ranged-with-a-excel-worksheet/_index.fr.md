---
title: "Déplacer une plage nommée dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Déplacer"
type: docs
url: /fr/ranges/move/
aliases: [  /fr/move-a-named-range-with-an-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, déplacer une plage nommée, feuille de calcul Excel, API REST, déplacement de plage, exemples SDK"
description: "Découvrez comment déplacer une plage nommée au sein d’une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud v3.0, avec les détails des points de terminaison, l’authentification, des exemples et des extraits de code SDK."
weight: 20
ArticleTitle: "Déplacer une plage nommée dans une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
---

Déplacer une plage nommée est une tâche courante lorsque vous devez réorganiser des données de manière programmatique. Cette section explique comment relocaliser une plage définie vers une nouvelle position sur la même feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud.

Cette API REST déplace une plage spécifiée vers une plage de destination dans une feuille de calcul Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### Authentification
L’API exige un **jeton JWT Bearer** obtenu via le flux OAuth d’Aspose Cloud. Incluez ce jeton dans l’en-tête `Authorization` :

```
Authorization: Bearer <jeton jwt>
```

Le jeton doit disposer de la portée **Cells**.

### Conditions préalables
- Le classeur doit être stocké dans le stockage Aspose Cloud.  
- Fournissez le nom du stockage (`storageName`) et le chemin du dossier (`folder`) si le fichier n’est pas situé dans le répertoire racine.  
- Utilisez la dernière version du SDK Aspose.Cells Cloud prenant en charge la version d’API **v3.0**.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom            | Type   | Emplacement | Description |
|----------------|--------|-------------|-------------|
| **name**       | string | path        | Nom du fichier du classeur |
| **sheetName**  | string | path        | Nom de la feuille de calcul |
| **destRow**    | integer| query       | Index de ligne de départ de la plage de destination (indexation à 0) |
| **destColumn**| integer| query       | Index de colonne de départ de la plage de destination (indexation à 0) |
| **range**      | object | body        | Définition de la plage source à déplacer |
| **folder**     | string | query       | Chemin du dossier où le classeur est stocké |
| **storageName**| string | query       | Nom du stockage Aspose Cloud |

### Corps de la requête

| Champ           | Type   | Obligatoire | Description |
|-----------------|--------|-------------|-------------|
| **ColumnCount** | integer| Non         | Nombre de colonnes dans la plage source |
| **ColumnWidth** | integer| Non         | Largeur de chaque colonne (en points) |
| **FirstColumn** | integer| Non         | Index de la première colonne (indexation à 0) de la plage source |
| **FirstRow**    | integer| Non         | Index de la première ligne (indexation à 0) de la plage source |
| **Name**        | string | Non         | Nom de la plage (si elle s’agit d’une plage nommée) |
| **RefersTo**    | string | Non         | Référence au style A1 définissant la plage |
| **RowCount**    | integer| Non         | Nombre de lignes dans la plage source |
| **RowHeight**   | integer| Non         | Hauteur de chaque ligne (en points) |
| **Worksheet**   | string | Non         | Feuille de calcul contenant la plage source |

### Déroulement de l’opération

1. **Téléversez** le classeur vers le stockage Aspose Cloud (s’il n’existe pas déjà).  
2. **Générez** un jeton JWT à l’aide du point de terminaison OAuth.  
3. **Constituez** la charge utile JSON décrivant la plage source.  
4. **Appelez** le point de terminaison `moveto` avec les paramètres de chemin, les paramètres de requête et le corps JSON requis.  
5. **Vérifiez** la réponse ; un appel réussi renvoie un code d’état `200 OK`.

### Exemple de requête / réponse

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

En cas d’erreur, la réponse inclut un champ optionnel `ErrorMessage` fournissant des détails supplémentaires sur l’échec.

**Codes d’état HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande     | Le fichier téléversé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |

**Schéma de réponse**

| Champ            | Type   | Description |
|------------------|--------|-------------|
| **Code**         | integer | Code d’état HTTP-like renvoyé par l’API (par exemple, 200) |
| **Status**       | string  | Description textuelle du résultat (par exemple, « OK ») |
| **ErrorMessage** | string (facultatif) | Détails lisibles de l’erreur en cas d’échec de l’appel |

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}
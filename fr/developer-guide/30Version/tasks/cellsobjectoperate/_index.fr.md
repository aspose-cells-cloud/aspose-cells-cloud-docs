---
title: "Aspose.Cells Cloud API – Utilisation de la tâche CellsObjectOperate (REST)"
second_title: "Document"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Découvrez comment utiliser la tâche CellsObjectOperate dans l’API Aspose.Cells Cloud, avec référence aux paramètres, exemples de requête/réponse et conseils pratiques concernant les classeurs, les feuilles de calcul, les graphiques et les tableaux croisés dynamiques."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – Utilisation de la tâche CellsObjectOperate (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "Tâche CellsObjectOperate"
  - "API Aspose.Cells Cloud"
  - "API REST Excel"
  - "Opération sur graphique"
  - "API tableau croisé dynamique"
  - "API saut de page"
---

**Vue d’ensemble**  
La tâche **CellsObjectOperate** permet d’effectuer des opérations de création, lecture, mise à jour et suppression (CRUD) sur des objets Excel tels que classeurs, feuilles de calcul, graphiques, tableaux croisés dynamiques, formes, sauts de page, etc., via un unique appel REST. Spécifiez le type d’objet à manipuler à l’aide de `OperateObjectType`, puis fournissez le bloc de paramètres correspondant (par exemple, `ChartOperateParameter` pour les actions liées aux graphiques).

---

**OperateObject**

| Nom du paramètre        | Type   | Description |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | string | Le type d’objet Excel sur lequel porter l’opération. Valeurs autorisées : `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition   | object | Conteneur identifiant l’emplacement de l’objet cible (par exemple, nom du classeur, nom de la feuille de calcul, index du graphique). Obligatoire pour la plupart des opérations. |

**OperateObjectPosition**

| Nom du paramètre | Type   | Description |
| ---------------- | ------ | ----------- |
| Workbook         | object | Le classeur contenant l’objet cible. Doit inclure soit `FileName` (stockage dans le cloud), soit `FileContent` (contenu encodé en base64). |
| SheetName        | string | Nom de la feuille de calcul sur laquelle l’opération est appliquée. Obligatoire pour les objets au niveau de la feuille (graphiques, formes, etc.). |
| ChartIndex       | integer| Index (à partir de 0) du graphique dans la feuille de calcul (utilisé lorsque `OperateObjectType` vaut `Chart`). |
| ShapeIndex       | integer| Index (à partir de 0) de la forme dans la feuille de calcul (utilisé lorsque `OperateObjectType` vaut `Shape`). |
| CellName         | string | Référence de cellule au format A1 (par exemple, `A1`). Utilisé pour les opérations au niveau des cellules. |
| ListObjectIndex  | integer| Index (à partir de 0) de l’objet liste (utilisé lorsque `OperateObjectType` vaut `ListObject`). |

**ChartOperateParameter**

| Nom du paramètre      | Type    | Description |
| --------------------- | ------- | ----------- |
| ChartIndex            | integer | Index du graphique à modifier. Obligatoire lors de la mise à jour d’un graphique existant. |
| ChartType             | string  | Type de graphique à créer (par exemple, `Bar`, `Line`, `Pie`). |
| UpperLeftRow          | integer | Numéro de ligne (à partir de 0) du coin supérieur gauche du graphique. |
| UpperLeftColumn       | integer | Numéro de colonne (à partir de 0) du coin supérieur gauche du graphique. |
| LowerRightRow         | integer | Numéro de ligne du coin inférieur droit du graphique. |
| LowerRightColumn      | integer | Numéro de colonne du coin inférieur droit du graphique. |
| Area                  | string  | Plage de données pour le graphique (par exemple, `A1:B5`). |
| IsVertical            | string  | `true` si l’orientation du graphique est verticale ; sinon `false`. |
| CategoryData          | string  | Plage fournissant les libellés de l’axe des abscisses (axe X). |
| IsAutoGetSerialName   | string  | `true` pour générer automatiquement les noms des séries ; `false` pour utiliser des noms personnalisés. |
| Title                 | string  | Texte du titre affiché sur le graphique. |

**ListObjectOperateParameter**

| Nom du paramètre | Type   | Description |
| ---------------- | ------ | ----------- |
| ListObject       | object | Objet de configuration pour une opération sur une liste (tableau). Inclut des propriétés telles que `ShowHeader`, `ShowTotal` et `Style`. |

**PageBreakOperateParameter**

| Nom du paramètre | Type    | Description |
| ---------------- | ------- | ----------- |
| PageBreakType    | string  | Type de saut de page (`Horizontal` ou `Vertical`). |
| Index            | integer | Index (à partir de 0) du saut de page à supprimer ou modifier. |
| Row              | integer | Numéro de ligne où placer un saut de page horizontal. |
| Column           | integer | Numéro de colonne où placer un saut de page vertical. |
| StartIndex       | integer | Index de départ pour une opération de saut de page sur une plage. |
| EndIndex         | integer | Index de fin pour une opération de saut de page sur une plage. |

**PageSetupOperateParameter**

| Nom du paramètre | Type   | Description |
| ---------------- | ------ | ----------- |
| PageSetup        | object | Paramètres de mise en page (marges, orientation, taille du papier, etc.). |

**PivotTableOperateParameter**

| Nom du paramètre | Type        | Description |
| ---------------- | ----------- | ----------- |
| DestCellName     | string      | Cellule supérieure gauche de la plage de destination pour le tableau croisé dynamique (par exemple, `C5`). |
| SourceData       | string      | Plage source du tableau croisé dynamique (par exemple, `A1:D100`). |
| TableName        | string      | Nom attribué au tableau croisé dynamique créé. |
| UseSameSource    | string      | `true` pour réutiliser une plage source existante ; `false` pour en créer une nouvelle. |
| PivotTableIndex  | integer     | Index du tableau croisé dynamique à mettre à jour (obligatoire pour les actions de modification/suppression). |
| PivotFieldRows   | integer[]   | Collection d’index de champs à afficher dans la zone des lignes. |
| PivotFieldColumns| integer[]   | Collection d’index de champs à afficher dans la zone des colonnes. |
| PivotFieldData   | integer[]   | Collection d’index de champs à afficher dans la zone des données. |

**ShapeOperateParameter**

| Nom du paramètre | Type   | Description |
| ---------------- | ------ | ----------- |
| Shape            | object | Définition de la forme (type, position, taille, texte, etc.). |

**WorkbookSettingsOperateParameter**

| Nom du paramètre | Type   | Description |
| ---------------- | ------ | ----------- |
| WorkbookSettings | object | Paramètres affectant l’ensemble du classeur (par exemple, mode de calcul, précision). |

**WorksheetOperateParameter**

| Nom du paramètre | Type   | Description |
| ---------------- | ------ | ----------- |
| Name             | string | Nom actuel de la feuille de calcul à manipuler. |
| SheetType        | string | Type de feuille (`Worksheet`, `Chart`, etc.). |
| NewName          | string | Nouveau nom de la feuille de calcul lors d’un renommage. |
| MovingRequest    | object | Paramètres pour déplacer une feuille (par exemple, `FromIndex`, `ToIndex`). |

## API REST

| API                | Type | Description | Lien vers la ressource |
| ------------------ | ---- | ----------- | ---------------------- |
| /cells/task/runtask| POST | Exécuter une tâche | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Conditions préalables
- **Authentification** – Inclure une entête valide `Authorization: Bearer <access_token>`.  
- **Stockage** – Le classeur source doit être stocké dans le stockage Aspose Cloud ou fourni sous forme de contenu encodé en base64 dans le corps de la requête.  
- **Version de l’API** – Cette documentation cible la **v3.0** de l’API Aspose.Cells Cloud.

### Exemple de requête (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

Le corps de la requête suit le schéma **CellsObjectOperateRequest** défini ci-dessous :

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* Définitions supplémentaires omises pour concision */
  }
}
```

### Exemple de réponse (succès – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Graphique créé avec succès."
  }
}
```

La réponse contient les champs suivants :

| Champ   | Type   | Description |
| ------- | ------ | ----------- |
| Code    | integer| Code de statut similaire à HTTP retourné par le moteur de tâches. |
| Status  | string | Statut lisible par l’humain (par exemple, `OK`). |
| TaskId  | string | Identifiant de la tâche asynchrone. |
| Result  | object | Objet contenant les résultats spécifiques à l’opération. |
| Result.ChartId | integer | Identifiant du graphique créé ou modifié. |
| Result.Message | string | Message court décrivant le résultat. |

### Gestion des erreurs

| Statut HTTP | Code d’erreur | Description | Remède suggéré |
| ----------- | ------------- | ----------- | -------------- |
| 400         | InvalidParameter | Un ou plusieurs paramètres de requête sont manquants ou mal formés. | Vérifiez les champs obligatoires et leurs types de données. |
| 401         | Unauthorized | Jeton d’authentification invalide ou manquant. | Actualisez le jeton d’accès et incluez-le dans l’entête `Authorization`. |
| 404         | NotFound | Le classeur, la feuille de calcul ou l’objet spécifié n’existe pas. | Vérifiez `FileName`, `SheetName` et les index d’objets. |
| 500         | ServerError | Une erreur inattendue s’est produite côté serveur. | Réessayez la requête ; si le problème persiste, contactez le support. |

### Cas d’usage courants
- **Ajouter un nouveau graphique** à une feuille de calcul.  
- **Renommer une feuille de calcul** (`OperateObjectType = "Worksheet"` avec `WorksheetOperateParameter.NewName`).  
- **Insérer un saut de page** (`OperateObjectType = "PageBreak"` avec `PageBreakOperateParameter`).  
- **Mettre à jour les données sources d’un tableau croisé dynamique** (`OperateObjectType = "PivotTable"` avec `PivotTableOperateParameter.SourceData`).  
- **Modifier les paramètres du classeur**, comme le mode de calcul (`OperateObjectType = "WorkbookSettings"`).  

---  

*Toutes les descriptions proviennent de la spécification OpenAPI officielle d’Aspose.Cells Cloud.*
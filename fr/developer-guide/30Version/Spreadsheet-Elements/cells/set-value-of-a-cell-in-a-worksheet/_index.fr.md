---
title: "Définir la valeur d'une cellule – Référence de l'API Aspose.Cells Cloud (v3.0)"  
type: docs  
url: /fr/set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "API Aspose Cells définir la valeur d'une cellule, mise à jour d'une cellule Excel via REST, exemple cURL Aspose.Cells Cloud"  
description: "Découvrez comment définir la valeur d'une cellule spécifique dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut la syntaxe de la requête, les paramètres, un exemple cURL en HTTPS et des exemples de code SDK."  
---  

Cette API REST permet de définir la **valeur d'une cellule** dans un fichier Excel.

## API REST  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**Paramètres de la requête**

| Nom             | Type   | Emplacement | Description                                                 |
|-----------------|--------|-------------|-------------------------------------------------------------|
| name            | string | path        | Nom du document Excel (y compris l'extension).             |
| sheetName       | string | path        | Nom de la feuille de calcul (sensible à la casse).         |
| cellName        | string | path        | Adresse au format A1 de la cellule cible (par exemple, `A1`). |
| value           | string | query       | Valeur à affecter à la cellule.                             |
| type            | string | query       | Type de données de la valeur (`int`, `string`, `float`, etc.). |
| formula         | string | query       | Formule à appliquer à la cellule (facultatif).             |
| folder          | string | query       | Dossier contenant le document (facultatif).                 |
| storageName     | string | query       | Nom du stockage où réside le fichier (facultatif).         |

## **Réponse**

Renvoie un objet `CellResponse`.

- **Aperçu des champs de réponse**

| Champ             | Type    | Description                                                     |
| ----------------- | ------- | --------------------------------------------------------------- |
| `Name`            | string  | Adresse de la cellule (par exemple, `F341`).                    |
| `Row`             | integer | Index de ligne (base zéro).                                     |
| `Column`          | integer | Index de colonne (base zéro).                                   |
| `Value`           | string  | Valeur affichée de la cellule.                                  |
| `Type`            | string  | Type de données de la cellule (par exemple, `IsString`).        |
| `Formula`         | string  | Texte de la formule si la cellule contient une formule.         |
| `IsFormula`       | bool    | Indique si la cellule contient une formule.                     |
| `IsMerged`        | bool    | Indique si la cellule fait partie d'une plage fusionnée.        |
| `IsArrayHeader`   | bool    | Indique si la cellule est une entête de tableau matriciel.      |
| `IsInArray`       | bool    | Indique si la cellule appartient à un tableau matriciel.        |
| `IsErrorValue`    | bool    | Indique si la cellule contient une valeur d'erreur.             |
| `IsInTable`       | bool    | Indique si la cellule se trouve à l'intérieur d'un tableau.     |
| `IsStyleSet`      | bool    | Indique si un style est appliqué à la cellule.                  |
| `HtmlString`      | string  | Représentation HTML codée de la valeur de la cellule.           |
| `Style.link`      | object  | Lien hypertexte vers la ressource de style.                     |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                    |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop volumineuse | Le fichier envoyé dépasse la taille maximale autorisée.       |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                              |

## Comment utiliser l'API PostWorksheetCellSetValue avec les SDK

### Spécification de l'API PostWorksheetCellSetValue

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) définit une interface de programmation publiquement accessible, permettant aux développeurs d'invoquer directement les points de terminaison REST depuis un navigateur ou tout client HTTP.

Vous pouvez utiliser l'outil en ligne de commande **cURL** pour appeler les services web Aspose.Cells. L'exemple ci-dessous montre comment définir la valeur d'une cellule à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK accélère le développement en gérant les détails de bas niveau, ce qui vous permet de vous concentrer sur votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
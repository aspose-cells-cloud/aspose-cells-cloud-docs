---
title: "Obtenir les propriétés des cellules"
type: docs
url: /fr/get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, API REST, Excel, Feuille de calcul, Propriétés des cellules, Obtenir les propriétés des cellules"
description: "Découvrez comment utiliser l'API REST Aspose.Cells Cloud pour récupérer les propriétés d'une cellule spécifique ou des méthodes prédéfinies dans une feuille de calcul Excel."
---

Cet exemple REST API montre comment récupérer une cellule spécifique dans un fichier Excel.

## API REST

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## Sécurité et authentification

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de la requête


| Nom du paramètre     | Type   | Emplacement | Description                                                                                                                                                                           |
| -------------------- | ------ | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | string | chemin      | Le nom du fichier Excel.                                                                                                                                                             |
| **sheetName**        | string | chemin      | Le nom de la feuille de calcul contenant la cellule.                                                                                                                                |
| **cellOrMethodName** | string | chemin      | Le nom de la cellule ou le nom d'une méthode prédéfinie (par exemple, `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`). |
| **folder**           | string | requête     | Le dossier dans lequel le document est stocké.                                                                                                                                      |
| **storageName**      | string | requête     | Le nom du service de stockage.                                                                                                                                                       |

## **Réponse**

Retourne un objet `CellResponse`.

- **Aperçu des champs de réponse**

| Champ            | Type    | Description                                           |
| ---------------- | ------- | ----------------------------------------------------- |
| `Name`           | string  | Adresse de la cellule (par exemple, `F341`).         |
| `Row`            | entier  | Index de ligne (à partir de zéro).                   |
| `Column`         | entier  | Index de colonne (à partir de zéro).                 |
| `Value`          | string  | Valeur affichée de la cellule.                       |
| `Type`           | string  | Type de données de la cellule (par exemple, `IsString`). |
| `Formula`        | string  | Texte de la formule, si la cellule en contient une. |
| `IsFormula`      | bool    | Indique si la cellule contient une formule.         |
| `IsMerged`       | bool    | Indique si la cellule fait partie d’un groupe fusionné. |
| `IsArrayHeader`  | bool    | Indique si la cellule est l’en-tête d’un tableau.   |
| `IsInArray`      | bool    | Indique si la cellule appartient à un tableau.      |
| `IsErrorValue`   | bool    | Indique si la cellule contient une valeur d’erreur. |
| `IsInTable`      | bool    | Indique si la cellule se trouve dans un tableau.    |
| `IsStyleSet`     | bool    | Indique si un style est appliqué à la cellule.      |
| `HtmlString`     | string  | Représentation HTML encodée de la valeur de la cellule. |
| `Style.link`     | objet   | Lien hypertexte vers la ressource de style.         |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Payload trop volumineux     | Le fichier envoyé dépasse la taille maximale autorisée.                   |
| 500  | Erreur interne du serveur   | Erreur inattendue survenue côté serveur.                                   |

## Comment utiliser l’API GetWorksheetCell avec les SDK

### Spécification de l’API GetWorksheetCell

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l'outil en ligne de commande `cURL` pour accéder facilement aux services web Aspose.Cells. L'exemple suivant montre comment effectuer un appel vers l'API Cloud avec `cURL`.
{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=VOTRE_ID_CLIENT&client_secret=VOTRE_CLEF_SECRETE" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK est la méthode la plus efficace pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Comment récupérer une cellule spécifique

- [Récupérer les données d’une cellule à partir d’une feuille de calcul](/fr/cells/get-cell-data-from-a-worksheet/)
- [Récupérer la première cellule d’une feuille de calcul Excel](/fr/cells/get-first-cell-from-excel-worksheet/)
- [Récupérer la dernière cellule d’une feuille de calcul Excel](/fr/cells/get-last-cell-of-excel-worksheet/)
- [Récupérer MaxRow à partir d’une feuille de calcul Excel](/fr/cells/get-maxrow-from-excel-worksheet/)
- [Récupérer MaxDataRow à partir d’une feuille de calcul Excel](/fr/cells/get-maxdatarow-from-excel-worksheet/)
- [Récupérer MaxColumn à partir d’une feuille de calcul Excel](/fr/cells/get-maxcolumn-from-excel-worksheet/)
- [Récupérer MaxDataColumn à partir d’une feuille de calcul Excel](/fr/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Récupérer MinRow à partir d’une feuille de calcul Excel](/fr/cells/get-minrow-from-excel-worksheet/)
- [Récupérer MinDataRow à partir d’une feuille de calcul Excel](/fr/cells/get-mindatarow-from-excel-worksheet/)
- [Récupérer MinColumn à partir d’une feuille de calcul Excel](/fr/cells/get-mincolumn-from-excel-worksheet/)
- [Récupérer MinDataColumn à partir d’une feuille de calcul Excel](/fr/cells/get-mindatacolumn-from-excel-worksheet/)
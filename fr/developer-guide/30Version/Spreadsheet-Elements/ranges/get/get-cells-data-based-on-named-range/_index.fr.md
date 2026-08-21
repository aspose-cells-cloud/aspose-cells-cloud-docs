---
title: "Obtenir les données des cellules à partir d’une plage nommée"
second_title: "Document"
linktitle: "Valeurs"
type: docs
url: /fr/ranges/get/values/
aliases: [  /fr/get-cells-data-based-on-named-range/ ]
keywords: "Aspose.Cells, Cloud, API REST, Excel, plage nommée, valeurs de cellule, feuille de calcul"
description: "Récupérez les valeurs de cellules à partir d’une plage nommée dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Ce service est accessible via plusieurs SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) et fonctionne sur une large gamme de plateformes de développement."
weight: 20
ArticleTitle: "Obtenir les données des cellules à partir d’une plage nommée – Aspose.Cells Cloud API"
---

**Conditions préalables**

- Un jeton d’accès JWT valide doté de la portée appropriée.  
- Le classeur doit être téléchargé dans le stockage Aspose Cloud (ou dans un dossier spécifié).  
- Assurez-vous que le nom du magasin cible est fourni si vous utilisez un magasin non par défaut.

Cette API REST renvoie une liste de cellules situées dans une plage identifiée soit par une plage nommée, soit par des index ligne‑colonne.

Cette opération permet aux développeurs de récupérer de manière programmatique les valeurs des cellules appartenant à une plage nommée spécifique dans une feuille de calcul Excel. En fournissant soit l’identifiant `namedRange`, soit des index explicites de ligne et de colonne, l’API renvoie une liste détaillée des cellules, incluant leur adresse, leur ligne, leur colonne, leur valeur, leur type de données et les informations de mise en forme. La réponse peut être utilisée pour alimenter des applications orientées données, générer des rapports ou effectuer d’autres calculs côté serveur. Le service Aspose.Cells Cloud prend en charge de multiples langages de programmation via ses SDK, garantissant une intégration fluide, quelle que soit la plateforme de développement. L’utilisation d’HTTPS garantit la transmission sécurisée des données, et l’API respecte les principes REST, renvoyant des codes d’état HTTP standards pour les cas de succès et d’erreur.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                                                      |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------ |
| name             | string  | path        | Le nom du fichier du classeur.                                                                  |
| sheetName        | string  | path        | Le nom de la feuille de calcul dans le classeur.                                                |
| namedRange       | string  | query       | La plage nommée à récupérer, par ex. `A1:B2` ou `nom_plage1`.                                   |
| firstRow         | integer | query       | Index zéro‑basé de la première ligne de la plage (utilisé lorsque `namedRange` n’est pas fourni). |
| firstColumn      | integer | query       | Index zéro‑basé de la première colonne de la plage (utilisé lorsque `namedRange` n’est pas fourni). |
| rowCount         | integer | query       | Nombre de lignes à inclure dans la plage.                                                       |
| columnCount      | integer | query       | Nombre de colonnes à inclure dans la plage.                                                     |
| folder           | string  | query       | Le dossier contenant le classeur.                                                               |
| storageName      | string  | query       | Le nom du stockage cloud où réside le classeur.                                                 |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler facilement les services web Aspose.Cells. L’exemple ci‑dessous montre comment demander les valeurs des cellules à partir d’une plage nommée.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Note de sécurité :** Utilisez toujours HTTPS lors de l’appel de l’API. Ce service ne prend pas en charge le HTTP en clair ; l’utilisation d’HTTPS garantit que la requête est chiffrée et respecte les bonnes pratiques de sécurité.

**Codes d’état HTTP**

| Code | Signification              | Description                                                    |
|------|----------------------------|----------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                     |

**Exemple de réponse d’erreur (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Le paramètre 'namedRange' est manquant ou invalide."
}
```

> **Conseil :** L’API utilise des index zéro‑basés pour `firstRow` et `firstColumn`. Par exemple, la première ligne de la feuille de calcul est `0`.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue le moyen le plus efficace d’accélérer le développement. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur la logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci‑dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
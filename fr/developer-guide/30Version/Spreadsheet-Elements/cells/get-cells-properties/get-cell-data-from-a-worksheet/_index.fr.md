---
title: "Obtenir les données d'une cellule à partir d'une feuille de calcul"
type: docs
url: /fr/get-cell-data-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells Cloud, obtenir les données d'une cellule, API Excel, API REST, valeur de cellule, API feuille de calcul, exemple Aspose API"
description: "Récupérer la valeur, le type et le style d'une cellule unique à partir d'une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut des exemples cURL et SDK, les paramètres et la gestion des erreurs."
---

Cet API REST récupère une cellule à partir d’une feuille de calcul Excel lorsque le paramètre **`cellOrMethodName`** spécifie un nom de cellule (une adresse au format A1, comme `A3`).

- **Exemple cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Paramètres**

| Paramètre          | Type   | Description                                               | Obligatoire |
|--------------------|--------|-----------------------------------------------------------|-------------|
| `cellOrMethodName` | chaîne | Doit être défini sur `firstcell` pour récupérer la première cellule. | Oui         |
| `fileName`         | chaîne | Nom du fichier du classeur (par exemple, `myWorkbook.xlsx`). | Oui         |
| `worksheet`        | chaîne | Nom de la feuille de calcul (par exemple, `Sheet1`).    | Oui         |
| `Authorization`    | en-tête | Jeton Bearer pour l’authentification.                    | Oui         |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Catégorie",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Catégorie</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

- **Utiliser les SDK Aspose.Cells Cloud**

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

---
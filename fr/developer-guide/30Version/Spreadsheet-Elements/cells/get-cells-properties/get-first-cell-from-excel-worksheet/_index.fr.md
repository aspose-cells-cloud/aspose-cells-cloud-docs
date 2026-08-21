---
title: "Obtenir la première cellule (A1) à partir d'une feuille Excel"
type: docs
url: /get-first-cell-from-excel-worksheet/
weight: 20
keywords: "Aspose.Cells Cloud, Excel, API REST, obtenir la première cellule, feuille de calcul, A1, API v3"
description: "Découvrez comment récupérer la première cellule (A1) d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud v3.0. Inclut une requête cURL, une réponse JSON, des exemples d'erreurs et des exemples de SDK pour C#, Java, PHP, Python et plus encore."
ArticleTitle: "Obtenir la première cellule (A1) à partir d'une feuille Excel à l'aide de l'API Aspose.Cells Cloud"
---

Cette API REST montre comment récupérer la **première cellule** d’un fichier Excel lorsque le paramètre `cellOrMethodName` est défini sur `firstcell`.

**Point de terminaison**  
`GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{worksheet}/cells/firstcell`

- **Exemple cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/firstcell" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Paramètres**

| Paramètre          | Type   | Description                                                  | Obligatoire |
|--------------------|--------|--------------------------------------------------------------|-------------|
| `cellOrMethodName` | string | Doit être défini sur `firstcell` pour récupérer la première cellule. | Oui         |
| `fileName`         | string | Nom du fichier classeur (par exemple, `myWorkbook.xlsx`).    | Oui         |
| `worksheet`        | string | Nom de la feuille de calcul (par exemple, `Sheet1`).        | Oui         |
| `Authorization`    | en-tête | Jeton Bearer utilisé pour l’authentification.               | Oui         |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A1",
    "Row": 0,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
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

**Réponses d’erreur**

- **401 Non autorisé**

```json
{
  "Code": "401",
  "Message": "Jeton d'accès invalide."
}
```

- **404 Non trouvé**

```json
{
  "Code": "404",
  "Message": "Le classeur, la feuille de calcul ou la cellule spécifiée n'existe pas."
}
```

- **500 Erreur interne du serveur**

```json
{
  "Code": "500",
  "Message": "Une erreur inattendue s'est produite sur le serveur."
}
```

**Codes d'état HTTP**

| Code | Signification               | Description                                              |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                          |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.     |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                        |

{{< /tab >}}

{{< /tabs >}}

- **Famille de SDK Cloud**

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

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
---
---
title: "Obtenir une validation de feuille de calcul par index à partir d'une feuille de calcul Excel"
second_title: "Document"
linktitle: "Obtenir"
type: docs
url: /fr/validations/get/
aliases: [  /fr/get-validation-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, API de validation de feuille de calcul, obtenir la validation par index, API REST Excel, SDK Aspose.Cells"
description: "Récupérer une validation de feuille de calcul à partir de son index à base zéro dans un classeur Excel à l'aide de l'API Aspose.Cells Cloud (v3.0). Inclut un exemple cURL, le schéma de réponse, les codes d'erreur et des extraits de code pour SDK en C#, Java, Python, etc."
weight: 10
---

Cette API REST récupère une validation de feuille de calcul à partir de son index dans une feuille de calcul Excel.  
Avant d’appeler le point de terminaison, obtenez un jeton JWT via le point de terminaison `/connect/token` et incluez-le dans l’en-tête `Authorization` sous la forme `Bearer <jeton jwt>`.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                             |
| ---------------- | ------- | ----------- | ------------------------------------------------------- |
| name             | string  | path        | Nom du fichier du classeur.                             |
| sheetName        | string  | path        | Nom de la feuille de calcul.                            |
| validationIndex  | integer | path        | Index à base zéro de la validation à récupérer.         |
| folder           | string  | query       | Dossier contenant le classeur.                          |
| storageName      | string  | query       | Nom du service de stockage.                             |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Schéma de réponse**

| Champ            | Type    | Description                                                                 |
| ---------------- | ------- | --------------------------------------------------------------------------- |
| AlertStyle       | string  | Style de l’alerte affichée à l’utilisateur (Stop, Warning, Information).  |
| AreaList         | array   | Collection des plages de cellules auxquelles la validation s’applique.     |
| IgnoreBlank      | boolean | Si `true`, les cellules vides sont ignorées lors de la validation.         |
| InCellDropDown   | boolean | Si `true`, une liste déroulante est affichée dans la cellule.              |
| Operator         | string  | Opérateur de comparaison utilisé pour la validation (par ex. `None`, `Between`). |
| ShowError        | boolean | Détermine si un message d’erreur est affiché en cas d’échec de validation. |
| ShowInput        | boolean | Détermine si un message d’entrée est affiché lors de la sélection de la cellule. |
| Type             | string  | Type de validation (par ex. `AnyValue`, `WholeNumber`, `Decimal`, etc.).  |
| link.Href        | string  | URL de référence vers la ressource de validation elle-même.                |
| link.Rel         | string  | Type de relation (toujours `self`).                                        |

**Codes d’erreur possibles**

| Status HTTP | Signification                                                               |
| ----------- | --------------------------------------------------------------------------- |
| 200         | Validation récupérée avec succès.                                           |
| 400         | Requête incorrecte – paramètres manquants ou non valides.                  |
| 401         | Non autorisé – jeton JWT invalide ou manquant.                             |
| 404         | Non trouvé – le classeur, la feuille de calcul ou l’index de validation n’existe pas. |
| 500         | Erreur interne du serveur – condition inattendue.                          |

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer avec Aspose.Cells Cloud. Un SDK abstracte les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
title: "Récupérer toutes les validations de feuille de calcul à partir d'une feuille Excel"
second_title: "Document"
linktitle: "Tout récupérer"
type: docs
url: /validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, validations de feuille de calcul, API REST, Récupérer toutes les validations, SDK"
description: "Récupérez toutes les validations de feuille de calcul à partir d'une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud. Prend en charge plusieurs SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) pour une intégration rapide."
weight: 10
---

Les validations de feuille de calcul vous permettent de définir des règles limitant le type ou la plage de données pouvant être saisies dans les cellules. Elles sont couramment utilisées pour garantir l'intégrité des données, par exemple en limitant les entrées à une liste de valeurs, à des dates dans une plage spécifique ou à des limites numériques.

Cette API REST permet de récupérer toutes les validations de feuille de calcul présentes sur une feuille Excel.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                  |
| ---------------- | ------ | ----------- | -------------------------------------------- |
| name             | string | path        | Nom du document Excel.                       |
| sheetName        | string | path        | Nom de la feuille de calcul.                 |
| folder           | string | query       | Chemin du dossier où le document est stocké. |
| storageName      | string | query       | Nom du service de stockage.                  |

**Codes de statut de la réponse**

| Code | Description                                     |
|------|-------------------------------------------------|
| 200  | Requête réussie – liste des validations         |
| 401  | Non autorisé – jeton invalide ou manquant      |
| 404  | Non trouvé – document ou feuille de calcul manquant |
| 500  | Erreur interne du serveur                       |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells Cloud. **Prérequis :** vous devez inclure un jeton JWT valide dans l’en-tête `Authorization`.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "La valeur doit être comprise entre 1 et 100."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "Veuillez sélectionner une valeur dans la liste."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}
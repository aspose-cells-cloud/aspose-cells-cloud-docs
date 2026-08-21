---
title: "Ajouter une validation de feuille de calcul à une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ajouter"
type: docs
url: /fr/validations/add/
keywords: "Ajouter une validation de feuille de calcul, Excel, Aspose.Cells Cloud, API REST, classeur, règle de validation"
description: "Utilisez l’API REST Aspose.Cells Cloud pour ajouter une validation de feuille de calcul à un fichier Excel. Des SDK sont disponibles pour C#, Java, PHP, Ruby, Node.js, Python, Perl, Go et Swift."
weight: 10
---

Cet exemple montre comment l’API REST Aspose.Cells Cloud permet d’ajouter une validation de feuille de calcul à une feuille de calcul Excel.

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                                           |
| ---------------- | ------ | ----------- | --------------------------------------------------------------------- |
| name             | string | path        | Nom du fichier Excel.                                                 |
| sheetName        | string | path        | Nom de la feuille de calcul.                                          |
| range            | string | query       | Plage de cellules à laquelle s’applique la validation (ex. A1:B10).   |
| validation       | object | body        | Définition de la règle de validation.                                 |
| folder           | string | query       | Dossier contenant le document.                                        |
| storageName      | string | query       | Nom du service de stockage.                                           |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/PutWorksheetValidation) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
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

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}
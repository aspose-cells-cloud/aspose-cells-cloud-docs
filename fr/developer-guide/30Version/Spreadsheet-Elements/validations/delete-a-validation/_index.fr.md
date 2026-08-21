---
title: "Supprimer la validation de feuille de calcul – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Supprimer"
type: docs
url: /validations/delete/
keywords: "Supprimer, validation de feuille de calcul, Aspose.Cells Cloud, API Excel"
description: "Découvrez comment supprimer une validation de feuille de calcul à partir d’un fichier Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint, les paramètres, les détails d’authentification, un exemple cURL, la gestion des erreurs et des extraits de code SDK."
weight: 10
---

Cette API REST supprime une validation de feuille de calcul à partir de son index de base zéro sur une feuille de calcul Excel.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                           |
| ---------------- | ------- | ----------- | ----------------------------------------------------- |
| name             | string  | path        | Le nom du fichier Excel.                              |
| sheetName        | string  | path        | Le nom de la feuille de calcul.                       |
| validationIndex  | integer | path        | L’index de base zéro de la validation à supprimer.   |
| folder           | string  | query       | Le dossier contenant le document.                     |
| storageName      | string  | query       | Le nom du service de stockage.                        |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler le service web Aspose.Cells. L’exemple ci-dessous montre comment supprimer une validation à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**Codes de statut HTTP**

| Code | Signification               | Description                                                  |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                              |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.          |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                   |

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer cette opération dans votre application. Les SDK gèrent les détails de bas niveau afin que vous puissiez vous concentrer sur la logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment supprimer une validation de feuille de calcul à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}
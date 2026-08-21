---
title: "Obtenir les sauts de page verticaux"
second_title: "Document"
linktitle: "Obtenir les sauts de page verticaux"
type: docs
url: /fr/page-breaks/get-vertical-page-breaks/
aliases: [  /fr/get-vertical-page-breaks-inside-worksheet/ ]
keywords: "Aspose.Cells, sauts de page verticaux, API Excel, feuille de calcul cloud, API REST"
description: "Récupérer les sauts de page verticaux à partir d’une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’endpoint HTTPS, les paramètres requis, un exemple cURL, les détails de la réponse, la gestion des erreurs et des exemples d’SDK."
weight: 20
---

Cet API REST permet de récupérer les **sauts de page verticaux** à partir d'une feuille de calcul.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                  | Obligatoire |
| ---------------- | ------ | ----------- | ------------------------------------------------------------ | ----------- |
| `name`           | string | path        | Le nom du fichier Excel.                                     | Oui         |
| `sheetName`      | string | path        | Le nom de la feuille de calcul à partir de laquelle lire les sauts. | Oui         |
| `folder`         | string | query       | Le dossier dans le stockage contenant le fichier.            | Non         |
| `storageName`    | string | query       | Le nom du stockage Aspose Cloud à utiliser.                  | Non         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Détails de la réponse

| Champ                     | Type  | Description                                                                                             |
| ------------------------- | ----- | ------------------------------------------------------------------------------------------------------- |
| `VerticalPageBreakList`   | array | Une collection d’objets représentant des sauts de page verticaux.                                      |
| `Column`                  | int   | L’index de colonne (à partir de 0) où le saut de page se produit.                                      |
| `StartRow`                | int   | La première ligne de la plage de saut (à partir de 0).                                                 |
| `EndRow`                  | int   | La dernière ligne de la plage de saut (à partir de 0 ; généralement `1048575` pour la dernière ligne). |
| `link.Href`               | string | URL auto-référencée de la ressource (HTTPS).                                                           |
| `Code`                    | int   | Code de statut HTTP renvoyé par le service.                                                            |
| `Status`                  | string | Description textuelle du statut HTTP.                                                                   |

### Gestion des erreurs

| Code HTTP | Signification        | Cause typique                                           |
| --------- | -------------------- | ------------------------------------------------------- |
| 401       | Non autorisé         | Jeton JWT manquant ou invalide.                         |
| 404       | Non trouvé           | Le fichier ou la feuille de calcul spécifié n’existe pas. |
| 400       | Requête incorrecte   | Paramètres de requête invalides ou mal formés.         |
| 500       | Erreur interne serveur | Condition inattendue côté serveur.                     |

Vérifiez les champs `Code` et `Status` dans la réponse JSON pour plus de détails.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer avec Aspose.Cells Cloud. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}
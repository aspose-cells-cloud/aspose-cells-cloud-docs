---
title: "Ajouter un lien hypertexte à une feuille de calcul"
type: docs
url: /fr/hyperlinks/add/
aliases: [  /fr/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells, ajouter un lien hypertexte, API REST Excel, SDK cloud"
description: "Découvrez comment ajouter un lien hypertexte à une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud v3.0. Inclut l’endpoint, un guide complet des paramètres, un exemple cURL et des extraits de code SDK pour C#, Java, Python, et plus encore."
weight: 20
---

Cette API REST ajoute un lien hypertexte à une feuille de calcul Excel.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                                      |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------ |
| name             | string  | path        | Nom du document.                                                                                 |
| sheetName        | string  | path        | Nom de la feuille de calcul.                                                                     |
| firstRow         | integer | query       | Indice de la première ligne (à base zéro) de la plage à laquelle le lien hypertexte sera appliqué. |
| firstColumn      | integer | query       | Indice de la première colonne (à base zéro) de la plage à laquelle le lien hypertexte sera appliqué. |
| totalRows        | integer | query       | Nombre de lignes couvertes par la plage du lien hypertexte.                                     |
| totalColumns     | integer | query       | Nombre de colonnes couvertes par la plage du lien hypertexte.                                   |
| address          | string  | query       | URL cible pointée par le lien hypertexte (encodée en URL).                                      |
| folder           | string  | query       | Dossier contenant le document.                                                                   |
| storageName      | string  | query       | Nom du stockage.                                                                                 |

La requête peut également inclure un corps JSON contenant les mêmes champs (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). Fournir un corps est utile lorsque vous préférez passer les paramètres dans le corps de la requête plutôt que dans la chaîne de requête.

### Réponses d’erreur

| Code HTTP | Raison                                                     | Corps d’exemple                                                         |
| --------- | ---------------------------------------------------------- | ----------------------------------------------------------------------- |
| **400**   | Requête incorrecte – paramètres manquants ou non valides. | `{ "Code":"400", "Message":"Valeur de paramètre non valide." }`        |
| **401**   | Non autorisé – jeton JWT manquant ou non valide.          | `{ "Code":"401", "Message":"Le jeton d'accès est manquant ou non valide." }` |
| **404**   | Introuvable – classeur ou feuille de calcul inexistante.  | `{ "Code":"404", "Message":"Fichier introuvable." }`                   |
| **500**   | Erreur interne du serveur – défaillance inattendue.       | `{ "Code":"500", "Message":"Une erreur inattendue est survenue." }`    |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

En cas d’échec de la requête, l’API renvoie les codes d’erreur HTTP standards (par exemple, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error), accompagnés d’un payload JSON contenant un message et un code d’erreur.

## Famille de SDK Cloud

Utiliser un SDK est la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau, afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}
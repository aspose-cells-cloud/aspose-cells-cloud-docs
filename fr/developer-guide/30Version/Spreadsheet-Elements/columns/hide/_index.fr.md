---
title: "Masquer des colonnes dans une feuille Excel"
second_title: "Document"
linktitle: "Masquer"
type: docs
url: /fr/columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, API de masquage de colonnes, masquage de colonnes Excel, API REST de masquage de colonnes, SDK Aspose.Cells, automatisation de feuilles de calcul"
description: "Découvrez comment masquer une ou plusieurs colonnes dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’URL du point de terminaison, les paramètres, un exemple cURL, des exemples de code SDK et la gestion des erreurs."
weight: 40
---

Cet API REST masque des colonnes dans une feuille de calcul.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                 |
|------------------|---------|-------------|-----------------------------------------------------------------------------|
| name             | string  | path        | Le nom du fichier classeur.                                                 |
| sheetName        | string  | path        | Le nom de la feuille de calcul dans laquelle les colonnes seront masquées. |
| startColumn      | integer | query       | Index de base zéro de la première colonne à masquer.                       |
| totalColumns       | integer | query       | Nombre de colonnes consécutives à masquer, à partir de **startColumn**.     |
| folder           | string  | query       | Chemin vers le dossier contenant le classeur.                               |
| storageName      | string  | query       | Nom du service de stockage où le fichier est situé.                         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler facilement les services web Aspose.Cells. L’exemple ci-dessous montre comment masquer une colonne à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de réponse possibles**

| Code HTTP | Signification                                | Exemple JSON (erreur)                                  |
|-----------|----------------------------------------------|--------------------------------------------------------|
| 200       | Succès                                       | `{ "Code": 200, "Status": "OK" }`                      |
| 400       | Requête incorrecte (ex. paramètres invalides) | `{ "Code": 400, "Message": "Plage de colonnes invalide." }` |
| 401       | Non autorisé (jeton manquant ou invalide)     | `{ "Code": 401, "Message": "Jeton d'accès invalide." }` |
| 404       | Introuvable (classeur ou feuille de calcul)   | `{ "Code": 404, "Message": "Fichier introuvable." }`   |
| 500       | Erreur interne du serveur                     | `{ "Code": 500, "Message": "Erreur inattendue." }`     |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

Utiliser un SDK est le moyen le plus rapide de développer. Un SDK abstrait les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
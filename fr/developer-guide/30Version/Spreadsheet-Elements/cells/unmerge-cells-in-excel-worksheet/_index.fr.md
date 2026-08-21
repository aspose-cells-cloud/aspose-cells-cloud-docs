---
title: "Désassembler les cellules dans une feuille Excel"
type: docs
url: /fr/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, Désassembler les cellules, API REST, SDK cloud"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour désassembler les cellules dans une feuille Excel, avec des exemples de requête, le format de réponse et des extraits de code SDK pour plusieurs langages de programmation."
ArticleTitle: "Désassembler les cellules dans une feuille Excel"
---

Cet API REST désassemble les cellules dans un fichier Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                             |
|------------------|---------|-------------|---------------------------------------------------------|
| name             | string  | path        | Nom du fichier de classeur.                             |
| sheetName        | string  | path        | Nom de la feuille de calcul.                            |
| startRow         | integer | query       | Index de ligne (à partir de 0) de la première ligne à désassembler. |
| startColumn      | integer | query       | Index de colonne (à partir de 0) de la première colonne à désassembler. |
| totalRows        | integer | query       | Nombre de lignes à inclure dans l’opération de désassemblage. |
| totalColumns     | integer | query       | Nombre de colonnes à inclure dans l’opération de désassemblage. |
| folder           | string  | query       | Chemin du dossier où le classeur est stocké.            |
| storageName      | string  | query       | Nom du service de stockage.                             |

## **Réponse**

Retourne un `CellCloudResponse`.

- **Aperçu des champs de réponse**

| Champ           | Type    | Description                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`        | string  |                                                      |
| `Code`          | integer | 200, 400, 401, 500, ...                              |


```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille limite. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |

## Comment utiliser l’API `PostWorksheetUnmerge` avec les SDK

### Spécification de l’API `PostWorksheetUnmerge`

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande `cURL` pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
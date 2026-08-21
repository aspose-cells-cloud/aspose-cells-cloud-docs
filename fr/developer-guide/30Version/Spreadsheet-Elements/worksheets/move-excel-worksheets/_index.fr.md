---
title: "Déplacer une feuille Excel – API Aspose.Cells Cloud (v3.0)"
second_title: "Document"
linktitle: "Déplacer"
type: docs
url: /fr/worksheets/move/
aliases: [  /fr/move-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, Déplacer une feuille, Excel, API REST, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "Découvrez comment déplacer une feuille Excel vers une nouvelle position à l’aide de l’API Aspose.Cells Cloud (v3.0). Inclut l’endpoint, les paramètres requis, un exemple cURL et du code SDK en C#, Java, Python, etc."
weight: 20
ArticleTitle: "Comment déplacer une feuille Excel avec l’API Aspose.Cells Cloud v3.0"
---

Cette API REST permet de déplacer une feuille dans un classeur Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                                                                           |
| ---------------- | ------ | ----------- | --------------------------------------------------------------------------------------------------------------------- |
| name             | string | path        | Nom du fichier Excel.                                                                                                |
| sheetName        | string | path        | Nom de la feuille à déplacer.                                                                                        |
| moving           | object | body        | Objet JSON spécifiant la feuille de destination (`DestinationWorksheet`) et la position relative (`Position`).     |
| folder           | string | query       | Chemin du dossier où le classeur est stocké.                                                                        |
| storageName      | string | query       | Nom du service de stockage.                                                                                          |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) définit une interface de programmation publiquement accessible et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler les services web Aspose.Cells. L’exemple ci-dessous montre comment déplacer une feuille en une seule requête.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille limite.                            |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                                  |

**Exemple de charge utile d’erreur**

```json
{
  "Code": 400,
  "Status": "Requête incorrecte",
  "Message": "Paramètre requis manquant : 'moving'."
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}
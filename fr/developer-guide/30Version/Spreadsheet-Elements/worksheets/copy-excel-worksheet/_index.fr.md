---
title: "Copier le contenu et les formats d'une autre feuille de calcul."
second_title: "Document"
linktype: "Copier"
type: docs
url: /fr/worksheets/copy/
aliases: [  /fr/copy-excel-worksheet/ ]
keywords: "API Aspose Cells pour copier une feuille de calcul, REST API Excel pour copier une feuille, SDK Aspose Cloud pour copier, copie de feuille de calcul dans un classeur"
description: "Découvrez comment copier une feuille de calcul et ses formats vers une nouvelle feuille à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’URL du point de terminaison, les paramètres, des exemples cURL et des exemples de SDK pour C#, Java, Python, etc."
weight: 20
---

Cet API REST permet de copier une feuille de calcul et ses formats vers une nouvelle feuille au sein du même classeur.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

Les paramètres de la requête sont listés ci-dessous :

| Nom du paramètre | Type   | Emplacement | Description                                                              |
| ---------------- | ------ | ----------- | ------------------------------------------------------------------------ |
| `name`           | string | path        | Le nom du fichier du classeur.                                           |
| `sheetName`      | string | path        | Le nom de la feuille de calcul de destination (la nouvelle feuille).   |
| `sourceSheet`    | string | query       | Le nom de la feuille de calcul à copier.                                |
| `options`        | object | body        | Objet JSON contenant les options de copie (par exemple, largeur des colonnes, formules). |
| `sourceWorkbook` | string | query       | Le nom du classeur source s’il est différent du classeur courant.       |
| `sourceFolder`   | string | query       | Le chemin du dossier où le classeur source est stocké.                  |
| `folder`         | string | query       | Le chemin du dossier où le classeur de destination sera enregistré.    |
| `storageName`    | string | query       | Le nom du service de stockage à utiliser.                               |

### Exemples de requête et réponse

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels vers l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
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

### Gestion des erreurs

L’API renvoie des codes d’état HTTP standard accompagnés d’un corps d’erreur au format JSON. Les réponses typiques incluent :

| Code HTTP | Description                                              | Exemple de corps d’erreur JSON                                |
| --------- | -------------------------------------------------------- | ------------------------------------------------------------- |
| 400       | Requête incorrecte – paramètres manquants ou non valides. | `{ "Code": 400, "Message": "Paramètres de requête invalides." }` |
| 401       | Non autorisé – jeton manquant ou non valide.             | `{ "Code": 401, "Message": "Échec de l’authentification." }`   |
| 404       | Introuvable – le classeur, la feuille de calcul ou le dossier n’existe pas. | `{ "Code": 404, "Message": "Ressource introuvable." }`         |
| 500       | Erreur interne du serveur – condition inattendue.        | `{ "Code": 500, "Message": "Une erreur inattendue s’est produite." }` |

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
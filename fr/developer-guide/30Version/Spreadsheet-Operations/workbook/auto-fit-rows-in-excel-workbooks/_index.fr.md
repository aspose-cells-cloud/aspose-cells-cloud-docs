---
title: "Ajuster automatiquement les lignes dans un classeur Excel"
second_title: "Document"
linktitle: "Lignes"
type: docs
url: /fr/autofit-rows-on-an-excel-file/
aliases: [  /fr/auto-fit-rows-in-excel-workbooks/ , /fr/workbook/autofit/rows/ ]
keywords: "ajuster automatiquement les lignes, classeur Excel, Aspose.Cells Cloud, API REST, options d’ajustement automatique"
description: "Découvrez comment ajuster automatiquement la hauteur des lignes dans un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’URL du point de terminaison, les paramètres, un exemple cURL et des extraits de code pour les SDK C#, Java, Python, etc."
weight: 90
ArticleTitle: "Ajuster automatiquement les lignes dans un classeur Excel – Aspose.Cells Cloud API"
---

**Conditions préalables**  
Avant d’appeler l’API, obtenez un jeton JWT Bearer valide à partir du service d’authentification Aspose, et assurez-vous que le classeur cible est stocké dans un emplacement pris en charge (stockage par défaut ou un stockage personnalisé que vous avez configuré).

Cette API REST vous permet d’**ajuster automatiquement les lignes** dans un classeur Excel, en modifiant automatiquement la hauteur des lignes après l’insertion ou la modification des données.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type              | Emplacement | Description                                                                 |
|------------------|-------------------|-------------|-----------------------------------------------------------------------------|
| name             | string            | path        | Nom du fichier du classeur.                                                 |
| autoFitterOptions| AutoFitterOptions | body        | Options contrôlant le comportement de l’ajustement automatique.            |
| startRow         | integer           | query       | Index de la première ligne à ajuster automatiquement.                       |
| endRow           | integer           | query       | Index de la dernière ligne à ajuster automatiquement.                       |
| firstColumn      | integer           | query       | Index de la première colonne prise en compte pour l’ajustement automatique. |
| lastColumn       | integer           | query       | Index de la dernière colonne prise en compte pour l’ajustement automatique. |
| onlyAuto         | boolean           | query       | Si **true**, seules les lignes marquées avec le drapeau AutoFit sont traitées (par défaut **false**). |
| folder           | string            | query       | Chemin du dossier où le classeur est stocké.                                |
| storageName      | string            | query       | Nom du service de stockage.                                                 |

**AutoFitterOptions** est un objet qui spécifie comment l’opération d’ajustement automatique se comporte (par exemple, `AutoFitMergedCells`, `IgnoreHidden`).

**Codes de statut HTTP**

| Code | Signification              | Description                                                   |
|------|----------------------------|---------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                               |
| 413  | Charge utile trop grande    | Le fichier envoyé dépasse la limite de taille.               |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                 |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler les services web Aspose.Cells. Remplacez `<jwt token>` par un jeton JWT Bearer valide obtenu auprès du service d’authentification Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Exemple de réponse d’erreur (par exemple, classeur manquant) :*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "Le classeur spécifié 'myWorkbook.xlsx' n’existe pas."
}
```

{{< /tab >}}

{{< /tabs >}}

**Remarques**  
- Lorsque `AutoFitMergedCells` est défini à **true**, les cellules fusionnées sont considérées comme une seule entité lors de l’opération d’ajustement automatique.  
- Définir `IgnoreHidden` à **true** ignore les lignes et colonnes masquées, en conservant leurs dimensions actuelles.

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK abstracte les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
title: "Ajuster automatiquement les colonnes dans un fichier Excel"
second_title: "Document"
linktitle: "Colonnes"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "ajuster automatiquement les colonnes, Excel, Aspose.Cells Cloud, API REST, SDK, cURL, API"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour ajuster automatiquement les colonnes dans un classeur Excel. Inclut les détails de la requête, un exemple cURL et des exemples de code SDK pour plusieurs langages."
weight: 90
---

Cette API REST prend en charge l’ajustement automatique des colonnes dans un classeur Excel.

## API PostAutofitWorkbookColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre      | Type    | Emplacement | Description                                            |
| --------------------- | ------- | ----------- | ------------------------------------------------------ |
| **name**              | string  | path        | Nom du fichier de classeur.                            |
| **autoFitterOptions** | object  | body        | Options permettant de contrôler le comportement d’ajustement automatique. |
| **startColumn**       | integer | query       | Index de base zéro de la première colonne à ajuster automatiquement. |
| **endColumn**         | integer | query       | Index de base zéro de la dernière colonne à ajuster automatiquement. |
| **folder**            | string  | query       | Dossier contenant le classeur.                         |
| **storageName**       | string  | query       | Nom du service de stockage.                            |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **Remarque :** Utilisez toujours le point de terminaison HTTPS en production et gardez votre jeton JWT confidentiel.

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

### Prérequis
Avant d’appeler cette opération, assurez-vous d’avoir une clé API Aspose Cloud valide, un jeton JWT généré, et que le classeur cible existe déjà à l’emplacement de stockage spécifié.

**Codes d’état HTTP**

| Code | Signification               | Description                                                      |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                               |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.             |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                       |

L’API peut renvoyer les codes d’état HTTP suivants :

| Code | Description                                    |
|------|------------------------------------------------|
| 200  | Succès – colonnes ajustées automatiquement     |
| 400  | Requête incorrecte – paramètres manquants ou non valides |
| 401  | Non autorisé – JWT non valide ou expiré        |
| 500  | Erreur serveur – échec du traitement interne   |

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus efficace pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur la logique de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
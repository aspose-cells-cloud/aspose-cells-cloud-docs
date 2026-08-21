---
title: "Mettre à jour les propriétés d'une feuille de calcul – Référence de l'API Aspose.Cells Cloud (v3.0)"
second_title: "Document"
linktitle: "Mettre à jour"
type: docs
url: /worksheets/update-properties/
aliases: [/update-excel-worksheet-properties/]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "feuille de calcul",
    "mettre à jour les propriétés",
    "API REST",
    "cloud",
    "v3.0",
  ]
description: "Découvrez comment mettre à jour les propriétés de base d'une feuille de calcul Excel (par exemple, l'affichage des zéros, la visibilité de la règle) à l'aide de l'API REST Aspose.Cells Cloud v3.0. Inclut une requête cURL, des exemples SDK, des paramètres et la gestion des erreurs."
ArticleTitle: "Mettre à jour les propriétés d'une feuille de calcul – Référence de l'API Aspose.Cells Cloud (v3.0)"
---

Cet API REST met à jour les propriétés de base d'une feuille de calcul.

## API REST

**Prérequis :** Vous devez disposer d’un compte Aspose Cloud valide, obtenir un jeton d’accès JWT et vous assurer que le classeur cible est stocké dans un emplacement pris en charge. Toutes les requêtes doivent être effectuées via **HTTPS**.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                         |
| ---------------- | ------ | ----------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| name             | string | path                                                  | Nom du fichier de classeur (avec extension).                                                        |
| sheetName        | string | path                                                  | Nom de la feuille de calcul à mettre à jour.                                                        |
| sheet            | object | body                                                  | Objet JSON contenant des paires clé/valeur de propriétés de feuille de calcul (par exemple, `DisplayZeros`, `IsRulerVisible`). |
| folder           | string | query                                                 | Chemin du dossier dans le stockage où se trouve le classeur.                                       |
| storageName      | string | query                                                 | Nom du stockage à utiliser.                                                                         |

L’objet **sheet** est envoyé dans le corps de la requête au format JSON. Les propriétés modifiables comprennent notamment `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible`, ainsi que d’autres définies dans la spécification de l’API.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

Codes de réponse typiques :

- **200** – Succès. Les propriétés de la feuille de calcul ont été mises à jour.
- **400** – Requête invalide (par exemple, JSON mal formé ou paramètre obligatoire manquant).
- **401** – Non autorisé – jeton JWT manquant ou invalide.
- **404** – Classeur ou feuille de calcul introuvable.
- **500** – Erreur interne du serveur.

| Code | Signification |
|------|---------------|
| 200 | Succès – les propriétés de la feuille de calcul ont été mises à jour. |
| 400 | Requête incorrecte – JSON mal formé ou paramètre obligatoire manquant. |
| 401 | Non autorisé – jeton JWT manquant ou invalide. |
| 404 | Introuvable – le classeur ou la feuille de calcul n’existe pas. |
| 500 | Erreur interne du serveur. |

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}
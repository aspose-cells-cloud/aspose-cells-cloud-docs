---
title: "Exporter une feuille de calcul avec l’API Aspose.Cells Cloud – Formats, exemples cURL et SDK"
second title: "Document"
linktitle: "Exportation de feuille de calcul"
type: docs
url: /fr/worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Get Worksheet, exportation de feuille de calcul, API Excel, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, API cloud"
description: "Découvrez comment exporter une seule feuille de calcul à partir d’un fichier Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut le point de terminaison, les paramètres, un exemple cURL corrigé, les détails d’authentification, la gestion des erreurs et des extraits de code SDK pour C#, Java, Python, etc."
weight: 10
ArticleTitle: "Exporter une feuille de calcul avec l’API Aspose.Cells Cloud – Formats, exemples cURL et SDK"
---

Cette API REST vous permet d’**exporter une feuille de calcul** à partir d’un fichier Excel vers de nombreux formats de fichiers différents.

**Résumé** – Utilisez le point de terminaison **Get Worksheet** (Obtenir une feuille de calcul) pour télécharger une seule feuille de calcul à partir d’un classeur dans le format de votre choix.

Vous pouvez exporter aux formats suivants :

| Format  | Extension | Type MIME                                                         |
| ------- | --------- | ----------------------------------------------------------------- |
| XLS     | .xls      | application/vnd.ms-excel                                          |
| XLSX    | .xlsx     | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb     | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV     | .csv      | text/csv                                                          |
| TSV     | .tsv      | text/tab-separated-values                                         |
| XLSM    | .xlsm     | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS     | .ods      | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT     | .txt      | text/plain                                                        |
| PDF     | .pdf      | application/pdf                                                   |
| OTS     | .ots      | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS     | .xps      | application/vnd.ms-xpsdocument                                    |
| DIF     | .dif      | application/x-dif                                                 |
| PNG     | .png      | image/png                                                         |
| JPEG    | .jpeg     | image/jpeg                                                        |
| GIF     | .gif      | image/gif                                                         |
| BMP     | .bmp      | image/bmp                                                         |
| WMF     | .wmf      | image/wmf                                                         |
| TIFF    | .tiff     | image/tiff                                                        |
| EMF     | .emf      | image/emf                                                         |
| NUMBERS | .numbers  | application/vnd.apple.numbers                                     |
| FODS    | .fods     | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Paramètres de la requête**

| Nom du paramètre         | Type    | Emplacement | Description                                                         |
| ------------------------ | ------- | ----------- | ------------------------------------------------------------------- |
| **name**                 | string  | path        | **Obligatoire.** Nom du fichier Excel.                              |
| **sheetName**            | string  | path        | **Obligatoire.** Nom de la feuille de calcul à exporter.           |
| **format**               | string  | query       | Format cible du fichier de la feuille de calcul exportée (par ex. `pdf`, `png`). |
| **verticalResolution**   | integer | query       | Résolution en DPI pour les formats prenant en charge la résolution (par ex. PNG, JPEG). |
| **horizontalResolution** | integer | query       | Résolution en DPI pour les formats prenant en charge la résolution. |
| **area**                 | string  | query       | Plage de cellules à exporter (par ex. `A1:D10`).                   |
| **pageIndex**            | integer | query       | Index de la page à exporter lorsque la feuille de calcul est paginée. |
| **folder**               | string  | query       | Chemin du dossier dans le stockage où se trouve le fichier source. |
| **storageName**          | string  | query       | Nom du stockage Aspose Cloud.                                      |

La <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<données binaires>
```

{{< /tab >}}

{{< /tabs >}}

## Gestion des erreurs

L’API renvoie des codes d’état HTTP standard. Les réponses courantes incluent :

| Code d’état | Signification                                                    | Corps JSON d’exemple                         |
| ----------- | ---------------------------------------------------------------- | -------------------------------------------- |
| **200**     | Succès – le flux de la feuille de calcul est renvoyé.          | `{ "stream": "..." }`                        |
| **400**     | Requête incorrecte – paramètres manquants ou non valides.       | `{ "error": "Paramètre format invalide." }` |
| **401**     | Non autorisé – jeton JWT invalide ou manquant.                  | `{ "error": "Échec de l’authentification." }`|
| **404**     | Introuvable – le fichier ou la feuille de calcul spécifié n’existe pas. | `{ "error": "Feuille de calcul introuvable." }` |
| **500**     | Erreur interne du serveur – condition inattendue sur le serveur.| `{ "error": "Erreur inattendue." }`          |

Gérez ces réponses dans votre code client afin de fournir un retour approprié aux utilisateurs.

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
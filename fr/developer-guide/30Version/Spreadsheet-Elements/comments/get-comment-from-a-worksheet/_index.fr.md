---
title: "Obtenir un commentaire de feuille de calcul – Documentation de l’API Aspose.Cells Cloud"
type: docs
url: /fr/comments/get/
aliases: [  /fr/get-comment-from-a-worksheet/ ]
keywords: "Aspose.Cells, commentaire de feuille de calcul, API, GET, Excel"
description: "Découvrez comment récupérer un commentaire de feuille de calcul par nom de cellule à l’aide de l’API Aspose.Cells Cloud (v3.0). Inclut l’URL de la requête, les paramètres, un exemple cURL, les détails de la réponse et des extraits de code SDK."
weight: 10
ArticleTitle: "Obtenir un commentaire de feuille de calcul – Documentation de l’API Aspose.Cells Cloud"
---

Cette API REST permet de récupérer un commentaire de feuille de calcul par nom de cellule à l’aide de **Aspose.Cells Cloud**.

**Prérequis :** Pour appeler cette opération, vous devez inclure un jeton d’accès JWT valide dans l’en-tête `Authorization` (`Bearer <jeton jwt>`). Les jetons peuvent être obtenus via le flux d’authentification d’Aspose.Cells Cloud décrit dans le [guide d’authentification](/cells/authentication/).

## API GetWorksheetComment

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin URL / chaîne de requête) | Description                                                      |
|------------------|--------|-----------------------------------------------|------------------------------------------------------------------|
| name             | string | Chemin URL                                    | Le nom du fichier Excel.                                         |
| sheetName        | string | Chemin URL                                    | Le nom de la feuille de calcul contenant le commentaire.        |
| cellName         | string | Chemin URL                                    | L’adresse de la cellule (par exemple, **A1**) dont le commentaire est récupéré. |
| folder           | string | Chaîne de requête                             | Le chemin du dossier dans lequel le document est stocké.       |
| storageName      | string | Chaîne de requête                             | Le nom du service de stockage.                                   |

La <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Réponse :** L’API renvoie un objet JSON contenant un objet `Comment` comportant les champs suivants :

| Champ                          | Type    | Description                                                |
|--------------------------------|---------|------------------------------------------------------------|
| `CellName`                     | string  | Adresse de la cellule (par exemple, **A1**).               |
| `Author`                       | string  | Nom de l’auteur du commentaire.                            |
| `HtmlNote`                     | string  | Contenu du commentaire au format HTML (le cas échéant).   |
| `Note`                         | string  | Version texte brut du commentaire.                         |
| `AutoSize`                     | boolean | Indique si la boîte de commentaire s’ajuste automatiquement. |
| `IsVisible`                    | boolean | Détermine si le commentaire est visible.                  |
| `Width`                        | integer | Largeur de la boîte de commentaire (en caractères).        |
| `Height`                       | integer | Hauteur de la boîte de commentaire (en caractères).        |
| `TextHorizontalAlignment`     | string  | Alignement horizontal du texte (par exemple, **Bottom**).  |
| `TextOrientationType`         | string  | Orientation du texte (par exemple, **TopToBottom**).       |
| `TextVerticalAlignment`       | string  | Alignement vertical du texte (par exemple, **Bottom**).    |

## Erreurs courantes

- **401 Non autorisé** – Vérifiez que le jeton JWT est valide, non expiré et correctement placé dans l’en-tête `Authorization`.
- **404 Non trouvé** – Assurez-vous que le nom du fichier, le nom de la feuille de calcul et l’adresse de la cellule sont corrects, et que le fichier existe dans le dossier/le stockage spécifié.
- **500 Erreur interne du serveur** – Vérifiez la charge utile de la requête pour les données mal formées et confirmez que le service est opérationnel.

**Codes d’état HTTP**

| Code | Signification               | Description                                                |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                          |
| 413  | Charge utile trop grande     | Fichier téléchargé dépassant la limite de taille.         |
| 500  | Erreur interne du serveur    | Erreur inattendue du serveur.                              |

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}
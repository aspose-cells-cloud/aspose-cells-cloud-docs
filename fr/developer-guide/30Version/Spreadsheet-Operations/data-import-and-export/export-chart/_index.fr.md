---
title: "Exporter un graphique Excel"
second_title: "Document"
linktitle: "Graphique"
type: docs
url: /export-excel-chart-to-different-formats/
aliases: [/export/excel-chart-to-different-formats/]
description: "Exportez des objets graphique Excel vers des formats populaires tels que PNG, JPEG, PDF, SVG, TIFF, EMF, WMF, et plus encore à l'aide de l'API REST Aspose.Cells Cloud ou des SDK. Inclut l'authentification, un exemple cURL et des exemples de code pour plusieurs langages."
keywords: "Aspose.Cells, export de graphique, export graphique Excel, API REST, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, formats de graphique, Aspose Cells Cloud"
weight: 20
ArticleTitle: "Exporter un graphique Excel – Document"
---

Exporter des objets graphique à partir d’un classeur Excel vers divers formats d’image et de document est une exigence courante pour la génération de rapports et la publication. Aspose.Cells Cloud fournit un point de terminaison REST simple qui convertit directement les graphiques vers des formats populaires tels que PNG, JPEG, PDF, SVG, TIFF, EMF, WMF, et plus encore.

Vous pouvez exporter des graphiques vers les formats suivants : [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), et [PDF](https://docs.fileformat.com/pdf/).

**Prérequis :**  
- Un compte Aspose.Cells Cloud valide avec un abonnement actif.  
- Un jeton OAuth 2.0 Bearer (JWT) obtenu via le flux d’authentification.  
- Le fichier de classeur à télécharger (taille maximale < 50 Mo).  

## **API REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Obligatoire | Description                                                                                                                     |
|------------------|--------|--------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| file             | fichier | formData                                               | Oui         | Fichier à télécharger                                                                                                           |
| objectType       | string | query                                                  | Oui         | Type d’objet à exporter. Pour l’export d’un graphique, utilisez `chart`. D’autres valeurs possibles sont `worksheet`, `picture`, etc. |
| format           | string | query                                                  | Oui         | Format de sortie souhaité. Valeurs prises en charge : `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.         |

### **Réponse**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                                           |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                               |

## Comment utiliser l’API PostExport avec les SDK

### Spécification de l’API PostExport

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST à partir d’un navigateur web.

Toutes les requêtes doivent inclure un jeton OAuth 2.0 Bearer valide dans l’en-tête `Authorization`. L’exemple ci-dessous montre comment appeler l’API avec **cURL** et télécharger un classeur en utilisant multipart/form‑data.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}
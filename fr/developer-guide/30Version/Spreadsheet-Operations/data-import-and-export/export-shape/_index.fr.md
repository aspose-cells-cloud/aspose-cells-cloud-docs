---
title: "Exporter des formes"
second_title: "Document"
linktitle: "Forme"
type: docs
url: /fr/export-excel-shape-to-different-formats/
aliases: [  /fr/export/excel-shape-to-different-formats/ ]
keywords: "Exporter des formes, Aspose.Cells Cloud, Exportation de formes Excel, Formats d’image, API REST, SDK"
description: "Découvrez comment exporter des formes Excel vers divers formats d’image (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) à l’aide de l’API REST Aspose.Cells Cloud et des SDK."
weight: 20
ArticleTitle: "Exporter des formes – Aspose.Cells Cloud"
---

L’exportation des formes à partir d’Excel permet de réutiliser du contenu diagrammatique sur différentes plateformes et applications. **Conditions préalables :** un jeton d’accès JWT valide et le fichier Excel source à télécharger.

Vous pouvez exporter des formes aux formats suivants : **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## API PostExport

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.


### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Obligatoire | Description |
|------------------|--------|--------------------------------------------------------|-------------|-------------|
| file             | fichier | formData                                               | True        | Fichier à télécharger |
| objectType       | string | query                                                  | True        | Type d’objet à exporter. Pour l’exportation de graphiques, utiliser `chart`. Les valeurs valides comprennent `shape`, `worksheet`, `picture`, etc. |
| format           | string | query                                                  | True        | Format de sortie souhaité. Valeurs prises en charge : `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **Exemple de requête**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Réponse

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... objets de fichiers supplémentaires ...
  ]
}
```

*Les charges utiles de fichiers codées en Base64 varient généralement de quelques centaines d’octets à plusieurs mégaoctets, selon les dimensions et le format de l’image.*

**Codes d’état HTTP**

| Code | Signification              | Description |
|------|----------------------------|-------------|
| 200  | OK                         | Exportation des formes réussie ; la réponse contient la liste des fichiers. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides. |
| 401  | Non autorisé               | Jeton d’accès invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur  | Erreur inattendue sur le serveur. |


## Comment utiliser l’API PostExport avec les SDK

### Spécification de l’API PostExport

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud à l’aide de cURL.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer avec Aspose.Cells Cloud. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur la logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}
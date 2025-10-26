---
title: Aspose.Cells Cloud Web API - Convertir un graphique de feuille de calcul en image
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: Convertir un graphique en image
type: docs
url: /fr/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: Convertir un graphique d'une feuille de calcul locale/fichier Excel en fichier image avec le Cloud Web Aspose.Cells API
weight: 100
kwords: convertir un graphique Excel en image, png, svg, tiff, jpg, bmp, tableur
---
Convertir un graphique d'une feuille de calcul locale/fichier Excel en fichier image. Prise en charge**FORMATS D'IMAGE :** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Convertir un graphique en image API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul contenant le graphique.|
|feuille de travail|Chaîne|Requête|Indiquez le nom de la feuille de calcul si applicable.|
|index des graphiques|Entier|Requête|Index du graphique à convertir.|
|format|Chaîne|Requête|(Obligatoire) Le type d'image souhaité (par exemple, svg, png, jpg).|
|chemin de sortie|Chaîne|Requête|(Facultatif) Le chemin du dossier dans lequel le classeur est stocké ; la valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Nom du stockage pour le fichier de sortie.|
|Emplacement des polices|Chaîne|Requête|Spécifiez des polices personnalisées si nécessaire.|
|région|Chaîne|Requête|Définissez la région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Le mot de passe pour ouvrir le fichier de feuille de calcul.|

## **Réponse**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Codes d'erreur

- **400 Mauvaise requête**: URI Apose.Cells Cloud API non valide.
- **401 Non autorisé**: Jeton d'accès non valide. Ou identifiant client et secret non valides.
- **404 non trouvé**:Le fichier de feuille de calcul n'est pas accessible.
- **Erreur de serveur 500**:La feuille de calcul a rencontré une anomalie lors de l'obtention des données de calcul.

## Où devez-vous utiliser le graphique de conversion en image API ?

- Exportez les graphiques de la feuille de calcul sous forme d’images.

## Pourquoi devriez-vous utiliser le graphique de conversion en image API ?

- Pas besoin de stockage cloud, ce qui réduit la charge sur les ressources cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser le graphique de conversion en image API avec les SDK ?

### Convertir un graphique en image API Spécifications

 Le[Convertir un graphique en image API Spécifications](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de convertir un graphique en image avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}

---
title: Aspose.Cells Cloud Web API - Convertir une plage de données de feuille de calcul en image
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to an Imag
linktitle: Convertir la plage en image
type: docs
url: /fr/convert-range-to-image/
keywords: Aspose.Cells Cloud Web API, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Format
description: Convertir une plage de données d'une feuille de calcul locale/fichier Excel en un fichier image
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, Conversion d'images, PNG, SVG, TIFF, JSON, Markdown
---
Convertir une plage de données d'une feuille de calcul locale/fichier Excel en fichier image. Prise en charge**FORMATS D'IMAGE :** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Convertir la plage en image API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul pour la conversion.|
|feuille de travail|Chaîne|Requête|Le nom de la feuille de calcul Spreadsheet/Excel|
|gamme|Chaîne|Requête|Définissez la zone de cellule à convertir (par exemple, A1:C10).|
|format|Chaîne|Requête|Spécifiez le format du fichier de sortie (par exemple, png, svg, tiff).|
|imprimerTitres|Booléen|Requête|Indiquez si les en-têtes de ligne et de colonne doivent être imprimés.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Le chemin du dossier dans lequel le classeur est stocké ; la valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Nom du stockage du fichier de sortie.|
|Emplacement des polices|Chaîne|Requête|Polices personnalisées à utiliser pour la conversion.|
|revenir|Chaîne|Requête|Définissez le paramètre de région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Mot de passe pour ouvrir le fichier de feuille de calcul s'il est protégé.|

### **Réponse**

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

## Pourquoi devriez-vous utiliser la plage de conversion en image API ?

- Pas besoin de stockage cloud, ce qui réduit la charge sur les ressources cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la plage de conversion en image API avec les SDK ?

### Spécification de conversion de plage en image API

 Le[Spécification de conversion de plage en image API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToImage) fournit une interface de programmation accessible au public, permettant des interactions REST directement depuis votre navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de convertir une plage de données en une image avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}

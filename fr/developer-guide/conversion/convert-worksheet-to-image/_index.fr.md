---
title: "Conversion de feuille de calcul – Documentation de l'API Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Comment convertir des données locales de classeur Excel en fichier image : Guide étape par étape"
linktype: "convertir une feuille de calcul en image"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, conversion feuille de calcul en image, convertir feuille de calcul en image, Excel en PNG, Excel en SVG, Excel en TIFF, Excel en JPEG, Excel en BMP, API de conversion d’image, API REST, exportation d’images de classeur, exemples de SDK"
description: "Guide étape par étape pour convertir une feuille de calcul Excel en formats d’image (PNG, SVG, TIFF, JPEG, BMP, etc.) à l’aide de l’API Aspose.Cells Cloud, incluant les paramètres de requête, les détails de la réponse, les codes d’erreur, les scénarios d’utilisation et les exemples de code SDK."
weight: 100
---

Exportez les données d’une feuille de calcul d’un fichier Excel local vers un fichier [Image](https://docs.fileformat.com/image/) à l’aide de l’API Aspose.Cells Cloud. Cette opération prend en charge plusieurs formats d’image et est idéale pour générer des captures visuelles des données de classeur.

**FORMATS D’IMAGE PRIS EN CHARGE**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API de conversion de feuille de calcul en image**

### **API Web**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de requête**

| Nom du paramètre | Type   | Emplacement (Chemin/Chaîne de requête/Corps HTTP) | Description                                                                          |
| :--------------- | :----- | :----------------------------------------------- | :----------------------------------------------------------------------------------- |
| Spreadsheet      | File   | FormData                                         | Téléchargement du fichier de classeur.                                               |
| worksheet        | String | Query                                            | Nom de la feuille de calcul à convertir.                                             |
| format           | String | Query                                            | Format d’image souhaité (`svg`, `png`, `tiff`, `jpeg`, `bmp`, etc.).                |
| outPath          | String | Query                                            | _(Facultatif)_ Chemin du dossier où l’image de sortie sera stockée ; valeur par défaut : `null`. |
| outStorageName   | String | Query                                            | Nom de l’emplacement de stockage pour le fichier de sortie.                         |
| fontsLocation    | String | Query                                            | Chemin vers un dossier personnalisé de polices, si vous devez utiliser des polices non disponibles sur le serveur. |
| region           | String | Query                                            | Paramètre régional du classeur (par ex., `fr-FR`).                                   |
| password         | String | Query                                            | Mot de passe requis pour ouvrir un fichier de classeur protégé.                     |

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

**Codes de statut HTTP**

| Code | Signification           | Description                                                       |
| ---- | ----------------------- | ----------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.              |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                     |

## **Dans quels cas utiliser l’API de conversion de feuille de calcul en image ?**

- **Captures statiques de rapports** – Convertir des tableaux financiers, des calculs ou d’autres données en images à inclure dans des rapports PDF, des diapositives PowerPoint ou des documents imprimés, là où aucune modification n’est nécessaire.
- **Visualisation des données dans les présentations** – Transformer des tableaux de classeur complexes (y compris le formatage conditionnel ou des graphiques simples) en images intégrables dans des présentations (PPTX, Google Slides).
- **Documentation et supports de formation** – Capturer des exemples de classeurs, des modèles ou des formulaires de saisie de données en images pour les manuels utilisateurs, tutoriels ou articles de bases de connaissances.
- **Aperçus sous forme de vignettes** – Générer de petites vignettes d’images pour des sections clés des classeurs, à afficher dans des navigateurs de fichiers, des bibliothèques de documents ou les résultats de recherche.

## **Pourquoi utiliser l’API de conversion de feuille de calcul en image ?**

- **Adaptée aux développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide, accompagné d’une documentation complète. Comparé à la mise en œuvre d’une solution personnalisée de rendu de graphiques, cela réduit considérablement la charge de développement.
- **Économique** – Vous pouvez convertir les données des tableaux sans avoir à stocker de façon permanente le classeur, ce qui économise de l’espace de stockage et réduit les coûts.
- **Préservation fidèle au pixel près** – Recrée fidèlement l’apparence d’Excel, y compris le formatage des cellules, les formules (affichées sous forme de valeurs), les bordures, les couleurs et le formatage conditionnel dans l’image de sortie.
- **Compatibilité universelle** – Les formats d’image (PNG, JPEG, TIFF, BMP, SVG, etc.) sont visualisables sur n’importe quel appareil ou plateforme, sans logiciel spécialisé, garantissant une accessibilité maximale.

## **Comment utiliser l’API de conversion de feuille de calcul en image avec les SDK ?**

### **Spécification de l’API de conversion de feuille de calcul en image**

La [spécification de l’API de conversion de feuille de calcul en image](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) définit une interface de programmation accessible publiquement et permet des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {jeton_daccès}" \
  -F "Spreadsheet=@monClasseur.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier optionnel"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Utiliser les SDK Aspose.Cells Cloud**

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet de convertir les données d’une feuille de calcul en image avec un code minimal. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}
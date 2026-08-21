---
title: "API Web Aspose.Cells Cloud - Convertir des données de tableau Excel locales en fichier image - Outil gratuit en ligne"
second_title: "Document"
ArticleTitle: "Comment convertir des données de tableau de feuille de calcul locale en fichier image : Guide étape par étape"
linktitle: "Convertir un tableau en image"
type: docs
url: /fr/convert-table-to-image/
keywords: "Aspose.Cells, API Cloud, convertir un tableau en image, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Convertissez rapidement un tableau de feuille de calcul Excel locale en fichier image à l’aide de l’API Aspose.Cells Cloud. Prend en charge les formats PNG, JPEG, TIFF, BMP, SVG et d’autres."
weight: 100
---

Exportez les données d’un tableau à partir d’un fichier Excel local vers un fichier [Image](https://docs.fileformat.com/image/) à l’aide de l’API Cloud.

**FORMATS D’IMAGE SUPPORTÉS :**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API Convertir un tableau en image**

Avant d’utiliser ce point de terminaison, assurez-vous de remplir les conditions préalables suivantes :

- Un jeton d’accès JWT valide obtenu via l’authentification Aspose.Cells Cloud.
- Un compte de stockage accessible si vous souhaitez utiliser les paramètres `outPath` ou `outStorageName`.
- Le classeur source (fichier Excel local) doit être lisible et, s’il est protégé, le mot de passe correct doit être fourni.

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                      |
| :--------------- | :----- | :----------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier| FormData                                               | Télécharger le fichier de feuille de calcul.                                                                                                                     |
| worksheet        | Chaîne | Requête                                                | Nom de la feuille de calcul du classeur/Excel.                                                                                                                  |
| tableName        | Chaîne | Requête                                                | Nom du tableau à convertir.                                                                                                                                      |
| format           | Chaîne | Requête                                                | Format souhaité du fichier image (par ex., png, svg).                                                                                                            |
| outPath          | Chaîne | Requête                                                | (Facultatif) Chemin du dossier dans lequel l’image convertie sera stockée. Par défaut, la valeur est null.                                                     |
| outStorageName   | Chaîne | Requête                                                | Nom du magasin de stockage de sortie.                                                                                                                            |
| fontsLocation    | Chaîne | Requête                                                | Utiliser des polices personnalisées si nécessaire.                                                                                                               |
| region           | Chaîne | Requête                                                | Paramètre régional/langue de la feuille de calcul (par ex., `fr-FR`, `en-US`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la localisation. |
| password         | Chaîne | Requête                                                | Mot de passe requis pour accéder au fichier de feuille de calcul.                                                                                               |

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

| Code | Signification             | Description                                                             |
| ---- | ------------------------- | ----------------------------------------------------------------------- |
| 200  | OK                        | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte        | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé              | Jeton JWT invalide ou manquant.                                         |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.                  |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                              |

## **Dans quel cas utiliser l’API Convertir un tableau en image ?**

- **Captures statiques de rapports** : Convertissez les tableaux financiers, les résultats de calculs ou toute donnée mise en forme en images destinées à être incluses dans des rapports PDF, des diapositives PowerPoint ou des documents imprimés, là où aucune modification n’est requise.
- **Visualisation des données dans les présentations** : Transformez les tableaux complexes de feuilles de calcul — incluant la mise en forme conditionnelle ou des visualisations simples — en images intégrables dans des présentations (PPTX, Google Slides).
- **Documentation et supports de formation** : Capturez des exemples de feuilles de calcul, des modèles ou des formulaires de saisie de données en tant qu’images à utiliser dans des manuels utilisateurs, des tutoriels ou des articles de base de connaissances.
- **Aperçus en miniatures** : Générez de petites images d’aperçu des sections clés des feuilles de calcul, à utiliser dans des navigateurs de fichiers, des bibliothèques de documents ou des résultats de recherche.

## Pourquoi utiliser l’API Convertir un tableau en image ?

- **Adaptée aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, ce qui permet un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions de rendu personnalisées, cela réduit considérablement la charge de travail de développement.
- **Économique** : Vous pouvez convertir des données de tableau sans avoir à télécharger d’abord l’ensemble du classeur, ce qui économise de l’espace de stockage et réduit les coûts.
- **Préservation fidèle au pixel près** : Reproduit fidèlement l’apparence d’Excel — y compris la mise en forme des cellules, les formules (sous forme de valeurs affichées), les bordures, les couleurs et la mise en forme conditionnelle — dans l’image de sortie.
- **Compatibilité universelle** : Les formats d’image (PNG, JPEG, TIFF, BMP, SVG, etc.) sont consultables sur n’importe quel appareil ou plateforme, sans logiciel spécialisé, garantissant une accessibilité maximale.

## Comment utiliser l’API Convertir un tableau en image à l’aide des SDK ?

### Spécification de l’API Convertir un tableau en image

La [Spécification de l’API Convertir un tableau en image](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) fournit une interface de programmation publiquement accessible pour effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
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

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir des données de tableau de feuille de calcul en image avec un nombre minimal de lignes de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}
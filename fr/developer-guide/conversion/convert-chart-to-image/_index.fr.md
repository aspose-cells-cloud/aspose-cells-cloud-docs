---
title: "Aspose.Cells Cloud Web API – Convertir un graphique Excel en image – Outil gratuit en ligne"
second_title: "Document"
articleTitle: "Comment convertir un graphique de feuille de calcul en image : guide étape par étape"
linktype: "convertir-graphique-en-image"
type: docs
url: /fr/convert-chart-to-image/
keywords: "convertir graphique en image, Aspose.Cells, export de graphique Excel, PNG, SVG, JPEG, BMP, TIFF"
description: "Utilisez l’API Web Aspose.Cells Cloud pour convertir directement un graphique Excel en images PNG, SVG, TIFF, JPEG ou BMP à partir d’un fichier de feuille de calcul."
weight: 100
---

Les graphiques Excel sont des représentations visuelles des données intégrées dans des feuilles de calcul. La conversion de ces graphiques en formats d’image facilite leur réutilisation dans des documents, des pages web et des rapports, sans nécessiter Excel.

Convertissez un graphique à partir d’une feuille de calcul locale ou d’un fichier Excel en fichier image. **FORMATS D’IMAGE PRIS EN CHARGE :** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>, <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>, <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>, <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>, <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **Convertir un graphique en image via l’API**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {jeton_daccès}" \
     -F "Spreadsheet=@MonClasseur.xlsx" \
     -o graphique.png
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                      | Obligatoire |
| :--------------- | :------ | :---------------------------------------------------- | :------------------------------------------------------------------------------- | :---------- |
| Spreadsheet      | Fichier | FormData                                              | Télécharger le fichier de feuille de calcul contenant le graphique.            | Oui         |
| worksheet        | Chaîne  | Chaîne de requête                                     | Spécifier le nom de la feuille de calcul le cas échéant.                        | Non         |
| chartIndex       | Entier  | Chaîne de requête                                     | Index du graphique à convertir.                                                  | Oui         |
| format           | Chaîne  | Chaîne de requête                                     | (Obligatoire) Type d’image souhaité (par exemple : svg, png, jpg).              | Oui         |
| outPath          | Chaîne  | Chaîne de requête                                     | (Facultatif) Chemin du dossier où le fichier de sortie sera stocké ; null par défaut. | Non         |
| outStorageName   | Chaîne  | Chaîne de requête                                     | Nom du stockage destiné au fichier de sortie.                                   | Non         |
| fontsLocation    | Chaîne  | Chaîne de requête                                     | Spécifier des polices personnalisées si nécessaire.                             | Non         |
| region           | Chaîne  | Chaîne de requête                                     | Définir la région de la feuille de calcul.                                      | Non         |
| password         | Chaîne  | Chaîne de requête                                     | Mot de passe pour ouvrir le fichier de feuille de calcul.                       | Non         |

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

**Codes de statut HTTP**

| Code | Signification           | Description                                                     |
| ---- | ----------------------- | --------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT non valide ou manquant.                              |
| 413  | Charge utile trop volumineuse | Le fichier téléversé dépasse la limite de taille.         |
| 500  | Erreur interne du serveur | Erreur inattendue sur le serveur.                             |

## Où utiliser l’API Convertir un graphique en image ?

- **Génération de rapports et tableaux de bord** : Convertir automatiquement les graphiques extraits des données Excel en images (PNG, JPEG, etc.) à intégrer dans des rapports PDF, des tableaux de bord web ou des présentations PowerPoint.
- **Applications web / courriel** : Diffuser directement les images de graphiques sur des pages web ou dans des courriels, sans nécessiter que les utilisateurs téléchargent ou ouvrent des fichiers Excel. Utile pour des outils de reporting dynamique, des lettres d’information ou des notifications automatisées.
- **Flux de travail de traitement de documents** : Intégrer à des pipelines automatisés (par exemple, facturation, analyse) où les graphiques Excel doivent être insérés dans d’autres formats (Word, PDF, HTML).
- **Applications mobiles / de bureau** : Afficher les graphiques Excel dans des applications où le rendu complet de la feuille de calcul est inutile ou impraticable.
- **Archivage et visualisation** : Sauvegarder les graphiques en tant qu’images autonomes pour un stockage à long terme, des vignettes ou des aperçus rapides, sans dépendance à Excel.

## Pourquoi utiliser l’API Convertir un graphique en image ?

- **Préservation de la fidélité visuelle** : Préserve le format exact du graphique (couleurs, libellés, échelle) tel qu’il apparaît dans Excel, garantissant une sortie de qualité professionnelle.
- **Indépendance de la plateforme** : Aucune installation d’Excel requise. Fonctionne multiplateforme (Windows, Linux, macOS) via l’API REST, adapté aux applications basées sur le cloud ou côté serveur.
- **Automatisation et évolutivité** : Convertir par lot plusieurs graphiques ou fichiers de manière programmatique, gagnant du temps par rapport à l’export manuel. Gère efficacement de grands volumes dans le cloud.
- **Formats de sortie flexibles** : Prend en charge les formats d’image populaires (PNG, JPG, BMP, SVG, etc.), permettant une intégration avec des systèmes et supports variés.
- **Sécurisé et fiable** : Traite les fichiers dans l’environnement cloud d’Aspose, sans exposer des données sensibles à des outils côté client. Haute disponibilité et performance constante.
- **Adapté aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, facilitant un développement rapide, accompagné d’une documentation complète. Comparé à la construction de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de développement.
- **Économique** : Vous pouvez convertir des graphiques sans téléverser préalablement le classeur, ce qui économise de l’espace de stockage et réduit les coûts.

## Comment utiliser l’API Convertir un graphique en image avec les SDK ?

### Spécification de l’API Convertir un graphique en image

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">spécification de l’API Convertir un graphique en image</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir un graphique en image avec un code minimal.  
Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}

---
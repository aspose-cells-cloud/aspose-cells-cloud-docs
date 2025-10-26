---
title: Aspose.Cells Cloud Web API - Conversion d'un graphique de feuille de calcul en fichier PDF
second_title: Documen
ArticleTitle: Converting a Spreadsheet Chart to a Pdf file
linktitle: Convertir un graphique en PD
type: docs
url: /fr/convert-chart-to-pdf/
keywords: convert an Excel chart to pdf, convert spreadsheet to pdf, Aspose Cloud Web  API, cloud conversion, Excel to PD
description: Ce API convertit de manière transparente les graphiques des feuilles de calcul situées sur un lecteur local en fichier PDF
weight: 100
kwords: Excel, Office Cloud, REST API, Conversion de feuille de calcul, PDF, CSV, JSON, Markdown, Conversion de graphique en PDF, Conversion Cloud
---
 Convertir un graphique à partir d'une feuille de calcul locale/fichier Excel en un[PDF](https://docs.fileformat.com/pdf/) déposer.

## **Convertir le graphique en PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|-------------- ||--------------------- |--------------------------------------------------- |
| Tableur|Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul.|
| feuille de travail| Chaîne| Requête| Le nom de la feuille de calcul contenant le graphique.|
| index des graphiques|Entier| Requête| L'index du graphique à convertir.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Le chemin du dossier où est stocké le fichier converti. La valeur par défaut est null.|
| outStorageName| Chaîne| Requête| Nom de stockage du fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Utilisez des polices personnalisées si nécessaire.|
| région| Chaîne| Requête| Le paramètre de région de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Le mot de passe pour ouvrir le fichier de feuille de calcul.|

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

## Où devez-vous utiliser le tableau de conversion en PDF API ?

- Exportez les graphiques de la feuille de calcul au format PDF.

## Pourquoi devriez-vous utiliser le tableau de conversion en PDF API ?

- Pas besoin de stockage cloud, ce qui réduit la charge sur les ressources cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser le graphique de conversion en PDF API avec les SDK ?

### Convertir un graphique en PDF (Spécification API)

 Le[Convertir un graphique en PDF (Spécification API)](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de convertir un graphique en fichier PDF avec un code court.
Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}

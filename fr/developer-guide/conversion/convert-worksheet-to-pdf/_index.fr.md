---
title: Aspose.Cells Cloud Web API - Convertir une feuille de calcul en fichier PD
second_title: Documen
ArticleTitle: Convert Spreadsheet Worksheet to Pd
linktitle: Convertir une feuille de calcul en Pd
type: docs
url: /fr/convert-worksheet-to-pdf/
keywords: worksheet to pdf, Excel PDF conversion, REST API, cloud-based conversion, spreadsheet to PD
description: Convertissez une feuille de calcul à partir d'une feuille de calcul sur votre disque local en un fichier PDF à l'aide de notre outil basé sur le cloud API
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, convertir une feuille de calcul en PDF, conversion cloud, conversion de fichier local
---
Convertissez une feuille de calcul locale/Excel en fichier PDF avec le Cloud Web Aspose.Cells API.

## **Convertir une feuille de calcul en PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|-----------------|-|-----------------------|------------------------------------|
| Tableur| Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul.|
| feuille de travail|Chaîne| Requête|Nom de la feuille de calcul dans la feuille de calcul.|
| chemin de sortie|Chaîne| Requête|(Facultatif) Le chemin du dossier pour stocker le classeur ; la valeur par défaut est null.|
| outStorageName|Chaîne| Requête| Le nom de stockage du fichier de sortie.|
| Emplacement des polices|Chaîne| Requête| Spécifiez des polices personnalisées.|
| région|Chaîne| Requête| Définissez le paramètre de région de la feuille de calcul.|
|mot de passe|Chaîne| Requête|Le mot de passe requis pour ouvrir le fichier de feuille de calcul.|

### **Réponse**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Codes d'erreur

- **400 Mauvaise requête**: URI Apose.Cells Cloud API non valide.
- **401 Non autorisé**: Jeton d'accès non valide. Ou identifiant client et secret non valides.
- **404 non trouvé**:Le fichier de feuille de calcul n'est pas accessible.
- **Erreur de serveur 500**:La feuille de calcul a rencontré une anomalie lors de l'obtention des données de calcul.

## Pourquoi devriez-vous utiliser le tableau de conversion en PDF API ?

- Pas besoin de stockage cloud, ce qui réduit la charge sur les ressources cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser le tableau de conversion en PDF API avec les SDK ?

### Spécifications de la conversion de tableau en PDF API

 Le[Spécifications de la conversion de tableau en PDF API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToPdf) fournit une interface de programmation accessible au public et permet des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de convertir les données d'un tableau de feuille de calcul en un fichier PDF avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}

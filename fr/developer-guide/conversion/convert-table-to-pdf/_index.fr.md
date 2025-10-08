---
title: Aspose.Cells Cloud Web API - Convertir les données d'un tableau de feuille de calcul en fichier PDF
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Pdf file
linktitle: Convertir un tableau en PD
type: docs
url: /fr/convert-table-to-pdf/
keywords: Table to PDF conversion, Excel to PDF, REST API, Spreadsheet conversion, Aspose.Cells Cloud Web AP
description: Convertissez un tableau d'une feuille de calcul sur votre disque local en un fichier PDF à l'aide de notre outil efficace API
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Excel conversion de table, Cloud PDF service
---
Convertissez les données d'une feuille de calcul locale/tableau Excel en un fichier PDF.

## **Convertir le tableau en PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul à convertir.|
|feuille de travail|Chaîne|Requête|Le nom de la feuille de calcul Spreadsheet/Excel|
|Nom de la table|Chaîne|Requête|Nom de la table à convertir.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Chemin du dossier où sera stocké le fichier PDF converti. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Spécifiez le nom du stockage du fichier de sortie.|
|Emplacement des polices|Chaîne|Requête|Utilisez des polices personnalisées pour le PDF.|
|région|Chaîne|Requête|Définissez le paramètre de région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Mot de passe pour accéder au fichier de feuille de calcul.|

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

## Pourquoi devriez-vous utiliser le tableau de conversion en PDF API ?

- Pas besoin de stockage cloud, ce qui réduit la charge sur les ressources cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser le tableau de conversion en PDF API avec les SDK ?

### Spécifications de la conversion de tableau en PDF API

 Le[Spécifications de la conversion de tableau en PDF API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToPdf) fournit une interface de programmation accessible au public pour exécuter des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de convertir les données d'un tableau de feuille de calcul en un fichier PDF avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}

---
title: Aspose.Cells Cloud Web API - Convertir les données d'un tableau de feuille de calcul en fichier HTML
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Html fil
linktitle: Convertir un tableau en HTM
type: docs
url: /fr/convert-table-to-html/
keywords: Excel Table to HTML, Spreadsheet Conversion, Aspose.Cells Cloud Web API, REST, Convert Excel to HTML, Table to HTML, Document Conversion, Cloud Service
description: Convertissez facilement des tableaux à partir de fichiers de feuille de calcul locaux au format HTML à l'aide de notre solution cloud API
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, HTML, PDF, CSV, JSON, Markdown, Correspondance des cellules vides dans Excel
---
Convertissez les données d'une feuille de calcul/tableau local Excel en un fichier HTML.

## **Convertir un tableau en HTML API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| Tableur| Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul à convertir.|
| feuille de travail| Chaîne| Requête| Le nom de la feuille de calcul Spreadsheet/Excel|
| Nom de la table| Chaîne| Requête| Le nom de la table à convertir.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Le chemin du dossier où le fichier converti sera stocké. La valeur par défaut est nulle.|
|outStorageName| Chaîne| Requête| Le nom de stockage désigné pour le fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Spécifiez des polices personnalisées pour la conversion.|
| région| Chaîne| Requête| Définissez les paramètres de la région de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Le mot de passe requis pour accéder au fichier de feuille de calcul.|

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

## Pourquoi devriez-vous utiliser le tableau de conversion en HTML API ?

- Pas besoin de stockage cloud, ce qui réduit la charge sur les ressources cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la table de conversion en HTML API avec les SDK ?

### Spécifications de conversion de tableau en HTML API

 Le[Spécifications de conversion de tableau en HTML API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToHtml) décrit une interface de programmation accessible au public, vous permettant d'effectuer des interactions REST directement depuis votre navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de convertir les données d'un tableau de feuille de calcul en un fichier HTML avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}

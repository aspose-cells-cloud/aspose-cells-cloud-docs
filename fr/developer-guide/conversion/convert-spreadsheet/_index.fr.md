---
title: Aspose.Cells Cloud Web API - Convertir une feuille de calcul en un autre format de fichier
second_title: Documen
ArticleTitle: Convert a Spreadsheet to another format file
linktitle: Convertir une feuille de calcul
type: docs
url: /fr/convert-spreadsheet/
keywords: spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local file
description: Convertit sans effort une feuille de calcul d'un lecteur local vers différents formats spécifiés à l'aide du Excel API
weight: 100
kwords: Excel, Office Cloud, REST API, Conversion de feuille de calcul, PDF, CSV, JSON, Markdown, Correspondance de toutes les cellules vides dans une feuille de calcul Excel
---
Convertissez une feuille de calcul locale/un fichier Excel en un autre fichier au format Aspose.Cells Cloud Web API.

|**Format de sortie**|**Description**|
|:- |:- |
|[XLS](https://docs.fileformat.com/spreadsheet/xls/)|Excel 95/5.0 - 2003 Cahier d'exercices.|
|[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)|Le format de fichier Open XML SpreadsheetML Office.|
|[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)|Excel Classeur binaire.|
|[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)|Excel Classeur prenant en charge les macros.|
|[XLT](https://docs.fileformat.com/spreadsheet/xlt/)|Excel 97 - Excel 2003 Modèle.|
|[XLTX](https://docs.fileformat.com/spreadsheet/xltx/)|Excel Modèle.|
|[XLTM](https://docs.fileformat.com/spreadsheet/xltm/)|Excel Modèle prenant en charge les macros.|
|[XLAM](https://docs.fileformat.com/spreadsheet/xlam/)|Un fichier complémentaire prenant en charge les macros Excel utilisé pour ajouter de nouvelles fonctions à Excel.|
|[CSV](https://docs.fileformat.com/spreadsheet/csv/)|Fichier CSV (valeurs séparées par des virgules).|
|[TSV](https://docs.fileformat.com/spreadsheet/tsv/)|Fichier TSV (valeurs séparées par des tabulations).|
|[SMS](https://docs.fileformat.com/word-processing/txt/)|Fichier texte brut délimité.|
|[HTML](https://docs.fileformat.com/web/html/)|Format HTML.|
|[MHTML](https://docs.fileformat.com/web/mhtml/)|Fichier MHTML.|
|[SAO](https://docs.fileformat.com/spreadsheet/ods/)|ODS (feuille de calcul OpenDocument).|
|Feuille de calculML|Excel 2003 Fichier XML.|
|[Nombres](https://docs.fileformat.com/spreadsheet/numbers/)|Le document est créé par l'application « Numbers » d'Apple qui fait partie de la suite iWork office d'Apple, un ensemble d'applications qui s'exécutent sur les systèmes d'exploitation Mac OS X et iOS.|
|[JSON](https://docs.fileformat.com/web/json/)|Notation d'objet JavaScript|
|[DIF](https://docs.fileformat.com/spreadsheet/dif/)|Format d'échange de données.|
|[DBF](https://docs.fileformat.com/database/dbf/)|Le fichier avec l'extension .dbf est un fichier de base de données utilisé par une application de système de gestion de base de données appelée dBASE.|
|[PDF](https://docs.fileformat.com/pdf/)|Format de document portable Adobe.|
|[XPS](https://docs.fileformat.com/page-description-language/xps/)|Format de spécification de document XML.|
|[SVG](https://docs.fileformat.com/page-description-language/svg/)|Format graphique vectoriel évolutif.|
|[TIFF](https://docs.fileformat.com/image/tiff/)|Format de fichier d'image balisé|
|[PNG](https://docs.fileformat.com/image/png/)|Format graphique réseau portable|
|[BMP](https://docs.fileformat.com/image/bmp/)|Format d'image bitmap|
|[EMF](https://docs.fileformat.com/image/emf/)|Format de métafichier amélioré|
|[JPEG](https://docs.fileformat.com/image/jpeg/)|JPEG est un type de format d'image enregistré à l'aide de la méthode de compression avec perte.|
|[GIF](https://docs.fileformat.com/image/gif/)|Format d'échange graphique|
|[RÉDUCTION](https://docs.fileformat.com/word-processing/md/)|Représente un document Markdown.|
|[SXC](https://docs.fileformat.com/spreadsheet/sxc/)|Un format basé sur XML utilisé par OpenOffice et StarOffice|
|[FODS](https://docs.fileformat.com/spreadsheet/fods/)|Il s'agit d'un format de document ouvert stocké sous forme de XML plat.|
|[DOCX](https://docs.fileformat.com/word-processing/docx/)|Un format bien connu pour les documents Word Microsoft qui est une combinaison de fichiers XML et binaires.|
|[PPTX](https://docs.fileformat.com/presentation/pptx/)|Le format PPTX est basé sur le format de fichier de présentation XML ouvert Microsoft PowerPoint.|
|[SqlScript](https://docs.fileformat.com/database/sql/)|Langage de requête structuré.|
|[XHtml](https://docs.fileformat.com/web/xhtml/)|Le XHTML est un format de fichier basé sur du texte avec un balisage XML, utilisant une reformulation de HTML 4.0.|
|[Epub](https://docs.fileformat.com/ebook/epub/)|Les fichiers avec l'extension .epub sont un format de fichier de livre électronique qui fournit un format de publication numérique standard pour les éditeurs et les consommateurs.|
|[XML](https://docs.fileformat.com/web/xml/)|XML signifie Extensible Markup Language, un langage similaire à HTML mais différent dans l'utilisation de balises pour définir des objets.|
|[Ots](https://docs.fileformat.com/spreadsheet/ots/)|Ouvrir le fichier de modèle de document (OTS).|
|[AZW3](https://docs.fileformat.com/ebook/azw3/)|AZW est un format de fichier de livre électronique numérique développé par Amazon pour ses appareils Kindle. AZW3, également connu sous le nom de Kindle Format 8 (KF8).|

## **Convertir la feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul à convertir.|
|format|Chaîne|Requête|(Obligatoire) Le format de sortie souhaité (par exemple, « Xlsx », « Pdf », « Csv »).|
|chemin de sortie|Chaîne|Requête|(Facultatif) Le chemin du dossier où sera stocké le classeur converti. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Spécifiez un nom de stockage de fichier de sortie.|
|Emplacement des polices|Chaîne|Requête|Utilisez des polices personnalisées pour la feuille de calcul.|
|région|Chaîne|Requête|Spécifiez le paramètre de région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Le mot de passe pour ouvrir le fichier de feuille de calcul s'il est protégé.|

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

## Pourquoi devriez-vous utiliser la feuille de calcul Convert API ?

- Pas besoin de stockage cloud, ce qui réduit la charge sur les ressources cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul Convert API avec les SDK ?

### Spécifications de la feuille de calcul API

 Le[Spécifications de la feuille de calcul API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) définit une interface de programmation accessible au public, vous permettant d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de convertir un fichier de feuille de calcul en un autre fichier de format avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{< /tab >}}
{{< /tabs >}}

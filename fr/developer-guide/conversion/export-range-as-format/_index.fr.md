---
title: Aspose.Cells Cloud Web API - Exporter les données d'une plage de feuilles de calcul sous forme de fichier de format
second_title: Documen
ArticleTitle: Export a Spreadsheet Range data as a Format file
linktitle: Exporter la plage au format
type: docs
url: /fr/export-range-as-format/
keywords: Aspose.Cells Cloud Web API, Export range, Spreadsheet conversion, REST API, PDF, CSV, JSON, Markdown, Excel workshee
description: Convertissez une plage spécifiée d'une feuille de calcul dans le stockage cloud en différents formats tels que PDF, CSV ou des formats d'image sans télécharger le fichier
weight: 100
kwords: Conversion de feuille de calcul, REST API, PDF, CSV, JSON, Markdown, feuille de calcul Excel
---
Exporter une feuille de calcul cloud/plage Excel vers un fichier de format. Ce fichier peut être enregistré dans le cloud ou exporté vers le stockage local.

## **Plage d'exportation au format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|nom|Chaîne|Chemin|(Obligatoire) Le nom du fichier de classeur à récupérer.|
|feuille de travail|Chaîne|Chemin|Le nom de la feuille de calcul Spreadsheet/Excel|
|gamme|Chaîne|Chemin|La plage à convertir (par exemple, A1:C12).|
|format|Chaîne|Requête|(Obligatoire) Le format de sortie souhaité (par exemple, « png », « pdf », « svg »).|
|dossier|Chaîne|Requête|(Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
|nom de stockage|Chaîne|Requête|(Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé. En cas d'omission, le stockage par défaut est utilisé.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Chemin d'accès au dossier du fichier de sortie. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Le nom du stockage du fichier de sortie.|
|Emplacement des polices|Chaîne|Requête|Emplacement des polices personnalisées.|
|région|Chaîne|Requête|Le paramètre régional de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Le mot de passe requis pour ouvrir le fichier de feuille de calcul.|

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

## Pourquoi devriez-vous utiliser la plage de feuille de calcul d'exportation au format API ?

- Vous pouvez convertir des fichiers cloud en différents formats à tout moment et n'importe où.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la plage de feuille de calcul d'exportation au format API avec les SDK ?

### Plage d'exportation au format API Spécification

 Le[Plage d'exportation au format API Spécification](https://reference.aspose.cloud/cells/#/ConversionController/ExportRangeAsFormat) fournit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant d'exporter une plage de données de feuille de calcul vers un fichier de format avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}

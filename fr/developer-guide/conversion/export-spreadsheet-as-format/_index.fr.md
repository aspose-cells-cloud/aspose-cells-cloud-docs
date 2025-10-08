---
title: Aspose.Cells Cloud Web API - Exporter une feuille de calcul sous forme de fichier de format
second_title: Documen
ArticleTitle: Export a Spreadsheet as a Format fil
linktitle: Exporter la feuille de calcul au format Forma
type: docs
url: /fr/export-spreadsheet-as-format/
keywords: Export spreadsheet, Aspose.Cells Cloud Web API, Convert spreadsheet, Spreadsheet formats, XLSX, PDF, CSV, JSON, Markdow
description: Convertit efficacement les feuilles de calcul stockées dans le stockage cloud en divers formats tels que XLSX, PDF et CSV
weight: 100
kwords: Excel, Office Cloud, REST, Conversion de feuilles de calcul, PDF, CSV, JSON, Markdow
---
Exporter une feuille de calcul cloud/Excel vers un autre format de fichier.

## **Exporter la feuille de calcul au format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| nom| Chaîne| Chemin| (Obligatoire) Le nom du fichier de classeur à récupérer.|
| format| Chaîne| Requête| (Obligatoire) Le format de sortie souhaité (par exemple, « Xlsx », « Pdf », « Csv »).|
| dossier| Chaîne| Requête| (Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
| nom de stockage| Chaîne| Requête|(Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé. Si vous l'omettez, utilisez le stockage par défaut.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Le chemin du dossier où le classeur sera stocké. La valeur par défaut est null.|
|outStorageName| Chaîne| Requête| Nom de stockage du fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Utiliser des polices personnalisées.|
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

## Pourquoi devriez-vous utiliser la feuille de calcul d'exportation au format API ?

- Vous pouvez convertir des fichiers cloud en différents formats à tout moment et n'importe où.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul d'exportation au format API avec les SDK ?

### Exporter la feuille de calcul au format API Spécification

 Le[Exporter la feuille de calcul au format API Spécification](https://reference.aspose.cloud/cells/#/ConversionController/ExportSpreadsheetAsFormat) fournit une interface de programmation accessible au public pour effectuer des interactions REST de manière transparente.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant d'exporter une feuille de calcul vers un fichier de format avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment interagir avec les services Web Aspose.Cells et les différents SDK via :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}

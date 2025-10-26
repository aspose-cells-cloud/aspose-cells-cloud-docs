---
title: Aspose.Cells Cloud Web API - Enregistrer la feuille de calcul en tant que fichier de format
second_title: Documen
ArticleTitle: Save Spreadsheet as a Format fil
linktitle: Enregistrer la feuille de calcul a
type: docs
url: /fr/save-spreadsheet-as/
keywords: spreadsheet conversion, Save as, Excel to PDF, Excel to CSV, RES
description: Convertissez sans effort les feuilles de calcul stockées dans le cloud en différents formats, notamment XLSX, PDF et CSV, à l'aide de notre robuste API
weight: 100
kwords: Excel API, Office Cloud, REST, Feuille de calcul, PDF, CSV, JSON, Markdown, convertir Excel fichiers, enregistrer la feuille de calcul sous, Aspose.Cells Cloud Web AP
---
Enregistrez un fichier de feuille de calcul cloud/Excel en tant que fichier de format sur le stockage cloud.

## **Enregistrer la feuille de calcul sous API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| nom| Chaîne| Chemin| (Obligatoire) Le nom du fichier de classeur à convertir.|
| format| Chaîne| Requête| (Obligatoire) Le format de sortie souhaité (par exemple, « Xlsx », « Pdf », « Csv »).|
| enregistrerOptionsData| Classe| Corps| (Facultatif) Enregistrer les données des options. La valeur par défaut est nulle.|
| dossier| Chaîne| Requête| (Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
| nom de stockage| Chaîne| Requête|(Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé. Si vous l'omettez, utilisez le stockage par défaut.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
|outStorageName| Chaîne| Requête| Nom de stockage du fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Utiliser des polices personnalisées.|
| région| Chaîne| Requête| Le paramètre de région de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Le mot de passe pour ouvrir le fichier de feuille de calcul.|

### **Réponse**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Codes d'erreur

- **400 Mauvaise requête**: URI Apose.Cells Cloud API non valide.
- **401 Non autorisé**: Jeton d'accès non valide. Ou identifiant client et secret non valides.
- **404 non trouvé**:Le fichier de feuille de calcul n'est pas accessible.
- **Erreur de serveur 500**:La feuille de calcul a rencontré une anomalie lors de l'obtention des données de calcul.

## Pourquoi utiliser le Save Spread API ?

- Vous pouvez convertir des fichiers cloud en différents formats à tout moment et n'importe où.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la table de conversion en Json API avec les SDK ?

### Enregistrer la feuille de calcul sous API Spécification

 Le[Enregistrer la feuille de calcul sous API Spécification](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) définit une interface de programmation accessible au public, vous permettant d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant d'enregistrer une feuille de calcul sous forme de fichier de format avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{< /tab >}}
{{< /tabs >}}

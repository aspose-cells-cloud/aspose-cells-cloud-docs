---
title: Aspose.Cells Cloud Web API - Diviser une feuille de calcul en plusieurs fichiers, un pour chaque feuille de calcul
second_title: Documen
ArticleTitle: Split a spreadsheet into multiple files, one for each worksheet
linktitle: Diviser une feuille de calcul distante dans Clou
type: docs
url: /fr/split-remote-spreadsheet/
keywords: spreadsheet splitting, cloud spreadsheet API, split Excel file, multi-format outpu
description: Diviser une feuille de calcul stockée dans le stockage cloud en plusieurs formats de sortie sans téléchargement
weight: 100
kwords: Excel, Office Cloud, REST, Feuille de calcul, PDF, CSV, JSON, Markdown, feuille de calcul distante divisée
---
Divisez la feuille de calcul stockée dans le cloud en fichiers séparés avec 30 formats de fichiers de sortie.

## **Feuille de calcul à distance divisée API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| nom| Chaîne| Chemin| Le nom du fichier de classeur à diviser.|
| dossier| Chaîne| Requête| Le chemin du dossier dans lequel le classeur est stocké.|
| depuis| Entier| Requête| Début de l'index de la feuille de travail.|
| à| Entier| Requête| Index de fin de feuille de travail.|
| format de sortie| Chaîne| Requête| Le format de sortie souhaité (par exemple, « Xlsx », « Pdf », « Csv »).|
| nom de stockage| Chaîne| Requête|(Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé. Si vous l'omettez, utilisez le stockage par défaut.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
|outStorageName| Chaîne| Requête| Nom de stockage du fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Utiliser des polices personnalisées.|
| région| Chaîne| Requête| Le paramètre de région de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Le mot de passe pour ouvrir le fichier de feuille de calcul.|

## **Réponse**

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

## Où devrions-nous utiliser la feuille de calcul Split Remote API ?

Lorsque vous devez fusionner plusieurs fichiers de données, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul Split Remote API ?

- Les fichiers de stockage cloud n'ont pas besoin d'être téléchargés et peuvent être divisés directement dans le cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul distante fractionnée API avec les SDK

### Spécifications de la feuille de calcul distante Split API

 Le[Spécifications de la feuille de calcul distante Split API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) définit une interface de programmation accessible au public et permet les interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de diviser la feuille de calcul stockée dans le cloud en fichiers séparés avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.
Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{< /tab >}}
{{< /tabs >}}

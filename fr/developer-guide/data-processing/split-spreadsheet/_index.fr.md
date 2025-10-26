---
title: Aspose.Cells Cloud WEb API - Diviser la feuille de calcul en fichiers séparés
second_title: Documen
ArticleTitle: Split the Spreadsheet into separate files
linktitle: Feuille de calcul fractionnée
type: docs
url: /fr/split-spreadsheet/
keywords: Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdow
description: Divisez une feuille de calcul locale en plusieurs fichiers de différents formats sans nécessiter de stockage dans le cloud
weight: 100
kwords: Excel API, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Diviser une feuille de calcul locale, Traitement Cloud, Gestion de fichiers, Gestion des erreurs
---
Divisez la feuille de calcul locale en fichiers séparés avec 30 formats de fichiers de sortie sans nécessiter de stockage dans le cloud.

## **Feuille de calcul fractionnée API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| Tableur| Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul à diviser.|
| depuis| Entier| Requête| Spécifiez l'index de début de la feuille de calcul.|
| à| Entier| Requête| Spécifiez l'index de fin de la feuille de calcul.|
| format de sortie| Chaîne| Requête| Définissez le format du fichier de sortie.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Chemin d'accès au dossier de stockage du classeur de sortie. La valeur par défaut est null.|
|outStorageName| Chaîne| Requête| Définissez le nom de stockage du fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Spécifiez des polices personnalisées si nécessaire.|
| revenir| Chaîne| Requête| Définissez la région de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Fournissez le mot de passe pour accéder au fichier de feuille de calcul.|

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

### Codes d'erreur

- **400 Mauvaise requête**: URI Apose.Cells Cloud API non valide.
- **401 Non autorisé**: Jeton d'accès non valide. Ou identifiant client et secret non valides.
- **404 non trouvé**:Le fichier de feuille de calcul n'est pas accessible.
- **Erreur de serveur 500**:La feuille de calcul a rencontré une anomalie lors de l'obtention des données de calcul.

## Où devrions-nous utiliser la feuille de calcul fractionnée API ?

Lorsque vous devez diviser une feuille de calcul en plusieurs fichiers, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul fractionnée API ?

- Pas besoin d'espace de stockage cloud, il suffit de le diviser directement.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul fractionnée API avec les SDK

### Spécifications de la feuille de calcul fractionnée API

 Le[Spécifications de la feuille de calcul fractionnée API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) fournit une interface de programmation accessible au public pour effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de diviser la feuille de calcul en fichiers séparés avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de différents SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}

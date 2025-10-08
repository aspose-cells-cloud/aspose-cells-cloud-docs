---
title: Aspose.Cells Cloud Web API - Fusionner plusieurs feuilles de calcul en une seule feuille de calcul
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: Fusionner la feuille de calcul
type: docs
url: /fr/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: Fusionnez facilement des fichiers de feuille de calcul locaux dans différents formats (XLSX, CSV, PDF) à l'aide du Excel API
weight: 100
kwords: Excel API, Fusion de feuilles de calcul, Office Cloud, REST API, Fusion de feuilles de calcul, Format CSV, JSON, Markdow
---
Fusionnez plusieurs fichiers de feuille de calcul locaux en un seul fichier, tout en prenant en charge la sortie dans plus de 30 formats de fichiers.

## **Fusionner la feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| Tableur| Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul.|
| format de sortie| Chaîne| Requête| Spécifiez le format du fichier de sortie.|
| fusionner dans une feuille| Booléen| Requête| Indiquez si vous souhaitez combiner toutes les données dans une seule feuille de calcul.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Chemin d'accès au dossier du classeur de sortie. La valeur par défaut est null.|
|outStorageName| Chaîne| Requête| Spécifiez le nom de stockage du fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Définissez les polices personnalisées à utiliser.|
| région| Chaîne| Requête| Définissez la région de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Fournissez le mot de passe pour ouvrir le fichier de feuille de calcul.|

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

## Où devrions-nous utiliser la feuille de calcul locale de fusion API ?

Lorsque vous devez fusionner plusieurs fichiers de données, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul locale de fusion API ?

- Pas besoin d'espace de stockage cloud, fusionnez simplement directement.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul locale de fusion API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)fournit une interface de programmation accessible au public, permettant aux utilisateurs d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de fusionner plusieurs feuilles de calcul en une seule feuille de calcul avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}

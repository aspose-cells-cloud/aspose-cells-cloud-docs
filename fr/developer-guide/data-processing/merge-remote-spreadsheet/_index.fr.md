---
title: Aspose.Cells Cloud Web API - Fusionner une feuille de calcul dans une autre.
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: Fusionner une feuille de calcul distante
type: docs
url: /fr/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: Combinez un fichier de feuille de calcul stocké dans un stockage cloud dans une autre feuille de calcul et vous pouvez spécifier le format et l'emplacement de la sortie des données.
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, fusionner les cellules vides, traitement cloud
---
Combinez un fichier de feuille de calcul stocké dans un stockage cloud dans une autre feuille de calcul et vous pouvez spécifier le format et l'emplacement de la sortie des données.

## **Fusionner la feuille de calcul distante API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|nom|Chaîne|Chemin|Le nom du fichier de classeur à fusionner.|
|feuille de calcul fusionnée|Chaîne|Requête|La liste des fichiers de feuille de calcul à fusionner.|
|dossier|Chaîne|Requête|Le chemin du dossier dans lequel le classeur est stocké.|
|format de sortie|Chaîne|Requête|Le format du fichier de sortie (par exemple, XLSX, PDF).|
|fusionner dans une feuille|Booléen|Requête|S'il faut combiner toutes les données dans une seule feuille de calcul.|
|nom de stockage|Chaîne|Requête|(Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé. En cas d'omission, le stockage par défaut est utilisé.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Chemin d'accès au dossier du classeur fusionné. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Le nom du stockage pour le fichier de sortie.|
|Emplacement des polices|Chaîne|Requête|Emplacement de police personnalisé.|
|région|Chaîne|Requête|Le paramètre de région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Le mot de passe pour accéder au fichier de feuille de calcul.|

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

## Où devons-nous utiliser la feuille de calcul distante de fusion API ?

- Lorsque vous devez fusionner plusieurs fichiers de données dans un stockage cloud.


## Pourquoi devriez-vous utiliser la feuille de calcul Merge Remote API ?

- Les fichiers de stockage cloud n'ont pas besoin d'être téléchargés et peuvent être fusionnés directement dans le cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul distante Merge API avec les SDK

### Spécifications de la fusion de feuilles de calcul distantes API

 Le[Spécifications de la fusion de feuilles de calcul distantes API](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) fournit une interface de programmation accessible au public pour exécuter des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de fusionner une feuille de calcul dans une autre feuille de calcul avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.
Les exemples de code suivants montrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

---
title: Aspose.Cells Cloud Web API - Fusionner les fichiers de feuille de calcul correspondants dans un fichier dans un dossier distant
second_title: Documen
ArticleTitle: Merge matching spreadsheet files into a file in a remote Folder
linktitle: Fusionner des feuilles de calcul dans un dossier distant
type: docs
url: /fr/merge-spreadsheets-in-remote-folder/
keywords: Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST AP
description: Combinez les fichiers de feuille de calcul stockés dans le stockage cloud en un seul fichier, et le format de fichier prend en charge 30 formats de sortie, tels que PDF, Csv, Json et d'autres formats courants
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, JSON, Markdown, Fusionner des feuilles de calcul, Traitement dans le Cloud, Gestion de fichiers à distance
---
Fusionnez les fichiers de feuille de calcul correspondants dans des fichiers d'un dossier distant, le format de fichier de sortie prend en charge plus de 30 formats tels que PDF, Csv, Json et d'autres formats courants.


## **Fusionner les feuilles de calcul dans un dossier distant API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| dossier| Chaîne| Requête|Le dossier dans lequel les fichiers fusionnés seront stockés.|
| expression de correspondance de fichier| Chaîne| Requête| Expression pour faire correspondre les fichiers à fusionner.|
| format de sortie| Chaîne| Requête| Le format de fichier de sortie souhaité.|
| fusionner dans une feuille| Booléen| Requête| Indique s'il faut combiner toutes les données dans une seule feuille de calcul.|
| nom de stockage| Chaîne| Requête| (Facultatif) Le nom du stockage cloud personnalisé ; la valeur par défaut est le stockage par défaut s'il est omis.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Le chemin du dossier pour stocker le classeur ; la valeur par défaut est null.|
|outStorageName| Chaîne| Requête| Le nom du stockage pour le fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Spécifie les polices personnalisées.|
| région| Chaîne| Requête| Définit la région de la feuille de calcul.|
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

## Où devons-nous utiliser la feuille de calcul de fusion dans le dossier distant API ?

Lorsque vous devez fusionner plusieurs fichiers de données, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul de fusion dans le dossier distant API ?

- Les fichiers de stockage cloud n'ont pas besoin d'être téléchargés et peuvent être fusionnés directement dans le cloud.
- Fusion par lots de plusieurs fichiers de feuille de calcul, prise en charge de l'expression correspondante.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul de fusion dans le dossier distant API avec les SDK

### Fusionner une feuille de calcul dans un dossier distant API Spécification

 Le[Fusionner une feuille de calcul dans un dossier distant API Spécification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) fournit une interface de programmation accessible au public permettant des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de fusionner les fichiers de feuille de calcul correspondants dans des fichiers d'un dossier distant avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}

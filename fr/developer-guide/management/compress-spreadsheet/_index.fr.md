---
title: Aspose.Cells Cloud Web API - Compresser la taille de la feuille de calcul
second_title: Documen
ArticleTitle: Compress the size of the Spreadshee
linktitle: Compresser une feuille de calcul
type: docs
url: /fr/compress-spreadsheet/
keywords: Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web AP
description: La feuille de calcul compressée API permet aux utilisateurs de réduire efficacement la taille des fichiers des feuilles de calcul en appliquant des niveaux de compression spécifiés, en optimisant le stockage et en améliorant les performances.
weight: 100
kwords: Excel, Office Cloud, REST, Compression de feuilles de calcul, Optimisation de la taille des fichiers, PDF, CSV, Json, Markdow
---
Compresser la taille de la feuille de calcul.

## **Compresser la feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul à compresser.|
|niveau|Entier|Requête|Spécifie le niveau de compression à appliquer, allant de 0 (aucune compression) à 9 (compression maximale).|
|chemin de sortie|Chaîne|Requête|(Facultatif) Le chemin du dossier où le classeur compressé sera stocké. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Nom de stockage du fichier de sortie.|
|région|Chaîne|Requête|Le paramètre de région de la feuille de calcul.|
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

## Où devrions-nous utiliser la feuille de calcul compressée API ?

Lorsque vous avez besoin de réduire la taille des feuilles de calcul, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul Compress API ?

- La feuille de calcul est trop volumineuse et il est nécessaire de réduire la taille du fichier.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul Compress API avec les SDK

### Spécifications de la feuille de calcul compressée API

 Le[Spécifications de la feuille de calcul compressée API](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) fournit une interface accessible au public pour les interactions REST, permettant des appels directs API à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de compresser la taille de la feuille de calcul avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

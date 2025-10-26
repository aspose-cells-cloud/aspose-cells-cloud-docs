---
title: Aspose.Cells Cloud Web API - Renommer une feuille de calcul dans une feuille de calcul
second_title: Documen
ArticleTitle: Rename worksheet in Spreadshee
linktitle: Renommer la feuille de calcul dans Spreadshee
type: docs
url: /fr/rename-worksheet-in-spreadsheet/
keywords: Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet Organizatio
description: Le point de terminaison Web API permet aux utilisateurs de renommer une feuille de calcul spécifiée dans un classeur, améliorant ainsi l'organisation et la lisibilité
weight: 100
kwords: Excel API, Renommer une feuille de calcul, Gestion des classeurs, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Faire correspondre toutes les cellules vides dans une feuille de calcul Excel
---
Renommer le nom de la feuille de calcul dans une feuille de calcul.

## **Renommer le nom de la feuille de calcul dans la feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul.|
|nom de la source|Chaîne|Requête|Nom actuel de la feuille de calcul à renommer.|
|nom de la cible|Chaîne|Requête|Nouveau nom pour la feuille de calcul.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Nom de stockage du fichier de sortie.|
|région|Chaîne|Requête|Paramètre de région de feuille de calcul.|
|mot de passe|Chaîne|Requête|Mot de passe pour ouvrir le fichier de feuille de calcul.|

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

## Où devons-nous utiliser la feuille de calcul Renommer dans la feuille de calcul API ?

Lorsque vous devez renommer une feuille de calcul dans des feuilles de calcul, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul Renommer dans la feuille de calcul API ?

- Renommez rapidement les feuilles de calcul à partir de feuilles de calcul.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul « Renommer » dans la feuille de calcul API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet)détaille une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement le renommage des cellules des feuilles de calcul avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

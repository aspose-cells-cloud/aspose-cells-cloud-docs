---
title: Aspose.Cells Cloud Webb API - Ajouter une feuille de calcul à une feuille de calcul
second_title: Documen
ArticleTitle: Add a Worksheet to a Spreadshee
linktitle: Ajouter une feuille de calcul à une feuille de calcul
type: docs
url: /fr/add-worksheet-to-spreadsheet/
keywords: Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, RES
description: Le Cloud Web Aspose.Cells API permet aux développeurs d'ajouter efficacement une nouvelle feuille de calcul à un classeur, en contrôlant son type, sa position et son nom. Cette fonctionnalité améliore la gestion et la flexibilité des classeurs.
weight: 100
kwords: Excel, Office Cloud, REST, Tableur, PDF, CSV, JSON, Markdown, Gérer Excel Feuilles de calcul, Création de feuilles de calcul dynamiques
---
Ajout d'une feuille de calcul à la feuille de calcul, en spécifiant le type et l'emplacement de la feuille de calcul.

|**Type de feuille de calcul** | Description|
|:- |:- |
|**VB** | Module Visual Basic|
|**Feuille de travail** | Feuille de travail|
|**Graphique** | Feuille de graphique|
|**BIFF4Macro** | Feuille de macro BIFF4|
|**Macro internationale** | Fiche macro internationale|
|**Autre** | Fiche macro internationale|
|**Dialogue** | Feuille de travail de dialogue|

## **Ajouter une feuille de calcul à la feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Télécharger un fichier de feuille de calcul.|
|type de feuille|Chaîne|Requête|Spécifie le nom de la nouvelle feuille de calcul. S'il n'est pas renseigné, un nom par défaut lui sera attribué.|
|position|Entier|Requête|Spécifie la position d'insertion de la nouvelle feuille de calcul. Si ce paramètre n'est pas renseigné, la feuille de calcul sera ajoutée à la fin du classeur.|
|nom de la feuille|Chaîne|Requête|Spécifie le type de feuille de calcul à ajouter. À défaut, un type de feuille de calcul par défaut sera utilisé.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Nom de stockage du fichier de sortie.|
|région|Chaîne|Requête|Le paramètre de région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Le mot de passe pour ouvrir le fichier de feuille de calcul.|

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

## Où devrions-nous utiliser la fonction Ajouter une feuille de calcul à la feuille de calcul API ?

Lorsque vous devez ajouter une feuille de calcul à une feuille de calcul, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul Ajouter à la feuille de calcul API ?

- Ajoutez une feuille de calcul à la feuille de calcul, en spécifiant le type et l’emplacement de la feuille de calcul.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser l'option Ajouter une feuille de calcul à une feuille de calcul API avec les SDK

### Ajouter une feuille de calcul à la feuille de calcul API Spécification

 Le[Ajouter une feuille de calcul à la feuille de calcul API Spécification](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant d'ajouter une feuille de calcul à une feuille de calcul avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels API vers des services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

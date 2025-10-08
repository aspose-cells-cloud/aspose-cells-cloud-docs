---
title: Aspose.Cells Cloud Web API - Créez une nouvelle feuille de calcul avec un modèle de feuille de calcul
second_title: Documen
ArticleTitle: Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc
linktitle: Créer une feuille de calcul
type: docs
url: /fr/create-spreadsheet/
keywords: Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancemen
description: Le Excel API permet aux utilisateurs de créer une nouvelle feuille de calcul avec un nom spécifié, prenant en charge des modèles facultatifs pour un contenu ou un formatage prédéfini, améliorant ainsi la productivité de l'utilisateur
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Correspondance de toutes les cellules vides dans une feuille de calcul Excel, Création de feuille de calcul, Prise en charge des modèles, Amélioration de la productivité
---
Créez une nouvelle feuille de calcul, qui peut être soit une feuille de calcul vierge, soit une feuille de calcul utilisable créée sur la base du modèle spécifié.

## **Créer une feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|---------- ||----------------------- |----- |
|format| Chaîne| Requête| Spécifie le nom de la nouvelle feuille de calcul. Ce nom sera utilisé pour l'identifier dans le système.|
| modèle| Chaîne| Requête| Facultatif. Si cette option est fournie, la nouvelle feuille de calcul sera créée selon le modèle spécifié. Cela peut être utile pour appliquer des mises en page et des styles prédéfinis.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
| outStorageName| Chaîne| Requête| Nom de stockage du fichier de sortie.|
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

## Où devrions-nous utiliser la feuille de calcul Create API ?

Lorsque vous avez besoin de créer une nouvelle feuille de calcul, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul Create API ?

- Vous pouvez non seulement créer une feuille de calcul vierge, mais vous pouvez également créer une feuille de calcul spécifique basée sur un modèle.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul Create API avec les SDK

### Créer une feuille de calcul API Spécification

 Le[Créer une feuille de calcul API Spécification](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) définit une interface de programmation accessible au public et permet les interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de créer la feuille de calcul avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

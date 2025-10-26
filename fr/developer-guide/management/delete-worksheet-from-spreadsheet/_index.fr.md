---
title: Aspose.Cells Cloud Web API - Supprimer une feuille de calcul du tableur
second_title: Documen
ArticleTitle: Delete a worksheet from the Spreadshee
linktitle: Supprimer une feuille de calcul d'une feuille de calcul
type: docs
url: /fr/delete-worksheet-from-spreadsheet/
keywords: delete worksheet, spreadsheet management, Aspose.Cells Cloud Web API, REST API, workbook structure, remove worksheet
description: Ce point de terminaison API permet aux utilisateurs de supprimer une feuille de calcul spécifiée d'un classeur, simplifiant ainsi la gestion des structures de classeur en éliminant les feuilles de calcul inutiles ou redondantes.
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, JSON, Markdown, Gérer Excel Feuilles de calcul, Supprimer les feuilles de calcul redondantes
---
Supprimer une feuille de calcul d'une feuille de calcul.

## **Supprimer la feuille de calcul de la feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:-               |:-     |:-                         |:-           |
| Tableur|Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul.|
| nom de la feuille| Chaîne| Requête| Spécifie le nom ou l'identifiant de la feuille de calcul à supprimer. Ce paramètre est obligatoire et doit correspondre au nom d'une feuille de calcul existante dans le classeur.|
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

## Où devons-nous utiliser la feuille de calcul Supprimer de la feuille de calcul API ?

Lorsque vous devez supprimer une feuille de calcul des feuilles de calcul, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul Supprimer de la feuille de calcul API ?

- Supprimez rapidement les feuilles de calcul des feuilles de calcul.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul Supprimer de la feuille de calcul API avec les SDK

### Supprimer la feuille de calcul de la feuille de calcul API Spécification

 Le[Supprimer la feuille de calcul de la feuille de calcul API Spécification](https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet) définit une interface de programmation accessible au public, vous permettant d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de supprimer une feuille de calcul de la feuille de calcul avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

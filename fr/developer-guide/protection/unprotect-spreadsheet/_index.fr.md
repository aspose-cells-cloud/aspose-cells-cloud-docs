---
title: Aspose.Cells Cloud Web API - Déprotéger la feuille de calcul avec un mot de passe
second_title: Documen
ArticleTitle: Unprotect the Spreadsheet with passwor
linktitle: Déprotéger la feuille de calcul
type: docs
url: /fr/unprotect-spreadsheet/
keywords: Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Managemen
description: Supprime efficacement la protection par mot de passe à double couche des feuilles de calcul Excel, prenant en charge les mots de passe ouverts et modifiables avec des techniques de cryptage avancées
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Correspond à toutes les cellules vides d'une feuille de calcul Excel
---
Applique les feuilles de calcul non protégées Excel avec mot de passe, prenant en charge les mots de passe d'ouverture et de modification.

## **Déprotéger la feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul à déprotéger.|
|mot de passe|Chaîne|Requête|Le mot de passe de cryptage du fichier de feuille de calcul.|
|modifier le mot de passe|Chaîne|Requête|Le mot de passe requis pour modifier le fichier protégé.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Le chemin du dossier où sera stocké le classeur non protégé. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Spécifie le nom de stockage du fichier de sortie.|
|région|Chaîne|Requête|Définit les paramètres de la région de la feuille de calcul.|

### **Réponse**

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

## Où devrions-nous utiliser la suppression des colonnes vides de la feuille de calcul API ?

Lorsque vous avez besoin de transformer des données, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la fonction Supprimer les colonnes vides de la feuille de calcul API ?

- Supprimez rapidement toutes les colonnes vides qui ne contiennent aucune donnée ni aucun autre objet d'une feuille de calcul Excel.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la fonction Supprimer les colonnes vides d'une feuille de calcul API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) définit une interface de programmation accessible au public, vous permettant d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant de supprimer facilement les colonnes vides des cellules des feuilles de calcul avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

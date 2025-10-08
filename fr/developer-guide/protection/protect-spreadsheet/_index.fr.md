---
title: Aspose.Cells Cloud Web API - Protéger les feuilles de calcul
second_title: Developer Guide for Excel Protectio
ArticleTitle: Protect the Spreadsheet with passwor
linktitle: Protéger la feuille de calcul
type: docs
url: /fr/protect-spreadsheet/
keywords: Aspose.Cells Cloud Web API, password protection, encrypt spreadsheet, modify passwor
description: Ce API applique une protection par mot de passe à double couche aux feuilles de calcul Excel, garantissant un accès et une modification sécurisés grâce au cryptage
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, protection par mot de passe double couche, crypter la feuille de calcul, sécuriser Excel
---
Applique la protection par mot de passe aux feuilles de calcul Excel, prenant en charge les mots de passe d'ouverture et de modification.

## **Protéger la feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul à protéger.|
|mot de passe|Chaîne|Requête|Mot de passe de cryptage pour le fichier de feuille de calcul.|
|modifier le mot de passe|Chaîne|Requête|Mot de passe requis pour modifier la feuille de calcul.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Le chemin du dossier où sera stocké le classeur protégé. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Nom du stockage pour les fichiers de sortie.|
|région|Chaîne|Requête|Définit les paramètres de région pour la feuille de calcul.|

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

## Où devons-nous utiliser la feuille de calcul Protect API ?

Lorsque vous devez verrouiller une feuille de calcul avec un mot de passe, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la feuille de calcul Protect API ?

- Verrouillez rapidement les feuilles de calcul avec un mot de passe.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la feuille de calcul Protect API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/ProtectionController/ProtectSpreadsheet)fournit une interface de programmation détaillée pour exécuter des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement la protection des cellules des feuilles de calcul avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

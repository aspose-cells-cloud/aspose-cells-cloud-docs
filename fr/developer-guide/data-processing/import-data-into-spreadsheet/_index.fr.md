---
title: Aspose.Cells Cloud Web API - Importer des données CSV, JSON ou XML dans un fichier de feuille de calcul
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: Importer des données dans une feuille de calcul
type: docs
url: /fr/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: Importez efficacement des données dans une feuille de calcul à partir de formats pris en charge tels que CSV, JSON et XML à l'aide du Cloud Web Aspose.Cells API
weight: 100
kwords: Aspose.Cells Cloud Web API, Importer des données, Office Cloud, REST, Tableur, CSV, JSON, XM
---
 Importez des données dans une feuille de calcul. Le format du fichier de données importé est pris en charge.[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) ou[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **Importer des données dans une feuille de calcul API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| fichier de données| Déposer| Données de formulaire| Téléchargez le fichier de données à importer.|
| Tableur| Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul cible.|
| feuille de travail| Chaîne| Requête| Spécifiez la feuille de calcul pour l’importation des données.|
| cellule de démarrage| Chaîne| Requête|Spécifiez la position de départ pour l'importation des données.|
| insérer| Booléen| Requête| Indique s'il faut insérer ou écraser les données d'importation spécifiées.|
| convertir des données numériques| Booléen| Requête| Spécifiez si vous souhaitez convertir les données numériques lors de l'importation.|
| séparateur| Chaîne| Requête| Spécifiez le délimiteur pour le format CSV.|
| chemin de sortie| Chaîne| Requête| (Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
|outStorageName| Chaîne| Requête| Spécifiez le nom de stockage du fichier de sortie.|
| Emplacement des polices| Chaîne| Requête| Définissez les polices personnalisées à utiliser.|
| revenir| Chaîne| Requête| Définissez la configuration de la région de la feuille de calcul.|
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

## Où devons-nous utiliser les données d'importation dans la feuille de calcul API ?

- Importation de grandes quantités de données dans une feuille de calcul.
-  Le format du fichier de données importé est[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) et[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## Pourquoi devriez-vous utiliser l'importation de données dans la feuille de calcul API ?

- Importation de grandes quantités de données dans des feuilles de calcul.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser l'importation de données dans une feuille de calcul API avec les SDK

### Importer des données dans une feuille de calcul API Spécification

 Le[Importer des données dans une feuille de calcul API Spécification](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) fournit une interface de programmation accessible au public, permettant des interactions REST directement depuis votre navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant d'importer des données dans une feuille de calcul avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

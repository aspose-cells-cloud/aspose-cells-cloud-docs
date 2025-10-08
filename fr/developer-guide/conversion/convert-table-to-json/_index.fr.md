---
title: Aspose.Cells Cloud Web API - Convertir les données d'un tableau de feuille de calcul en fichier JSON
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Json file
linktitle: Convertir un tableau en JSO
type: docs
url: /fr/convert-table-to-json/
keywords: Excel API, JSON conversion, spreadsheet to JSON, cloud file conversion, REST API, Aspose.Cell
description: Convertissez efficacement une table de feuille de calcul locale au format JSON à l'aide de la méthode Excel API. Cette méthode permet un traitement de fichiers transparent sans nécessiter de stockage dans le cloud.
weight: 100
kwords: Excel API, conversion JSON, conversion de fichiers cloud, feuille de calcul, REST API, Aspose.Cells, traitement du lecteur local, conversion de format de fichier
---
Convertissez une feuille de calcul/tableau local Excel en fichier json avec le Cloud Web Aspose.Cells API.

## **Convertir le tableau en Json API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|-------------|-|-----------------------|----------------------------------------------|
| Tableur| Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul.|
| feuille de travail|Chaîne| Requête| Spécifiez le nom de la feuille de calcul.|
| Nom de la table|Chaîne| Requête| Indiquez le nom de la table à convertir.|
| chemin de sortie|Chaîne| Requête| (Facultatif) Le chemin du dossier dans lequel le classeur est stocké ; la valeur par défaut est null.|
| outStorageName|Chaîne| Requête| Spécifiez le nom de stockage du fichier de sortie.|
| Emplacement des polices|Chaîne| Requête| Utilisez des polices personnalisées pour la conversion.|
| région|Chaîne| Requête|Définissez les paramètres de région pour la feuille de calcul.|
| mot de passe|Chaîne| Requête| Le mot de passe requis pour ouvrir le fichier de feuille de calcul.|

## **Réponse**

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

## Pourquoi devriez-vous utiliser la table de conversion en Json API ?

- Pas besoin de stockage cloud, ce qui réduit la charge sur les ressources cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la table de conversion en Json API avec les SDK ?

### Spécification de conversion de tableau en Json API

 Le[Spécification de conversion de tableau en Json API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToJson) fournit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant de convertir les données d'une table de feuille de calcul en un fichier json avec un code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}
{{< /tab >}}
{{< /tabs >}}

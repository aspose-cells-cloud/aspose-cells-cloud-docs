---
title: Aspose.Cells Cloud Web API - Remplacer le contenu de la plage dans une feuille de calcul distante
second_title: Documen
ArticleTitle: Replace Range Content in Remote a Spreadshee
linktitle: Remplacer le contenu de la portée à distance
type: docs
url: /fr/replace-content-in-remote-range/
keywords: API, Excel API, Replace Content, Remote Spreadsheet, Cloud Storage, Text Replacement, REST AP
description: Remplacez efficacement le texte dans les plages spécifiées de feuilles de calcul distantes à l'aide de Aspose.Cells Cloud API
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Faire correspondre toutes les cellules vides dans une feuille de calcul Excel, remplacement de texte à distance, intégration de stockage cloud
---
Remplacez efficacement le texte spécifié dans une plage d'un fichier de feuille de calcul distant.

## **Remplacer le contenu dans la plage distante API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| nom| Chaîne| Chemin| Le nom du fichier de classeur à modifier.|
| recherche de texte| Chaîne| Requête| Le texte à rechercher dans la feuille de calcul.|
| remplacer le texte| Chaîne| Requête| Le texte par lequel remplacer le texte recherché.|
| feuille de travail| Chaîne| Chemin| Le nom de la feuille de calcul où le remplacement aura lieu.|
| zone de cellule| Chaîne| Chemin| La zone cellulaire spécifique pour le remplacement.|
| dossier| Chaîne| Requête| Le chemin du dossier dans lequel le classeur est stocké.|
| nom de stockage| Chaîne| Requête|(Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé. Si vous l'omettez, utilisez le stockage par défaut.|
| région| Chaîne| Requête| Le paramètre de région de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Le mot de passe pour ouvrir le fichier de feuille de calcul.|

### **Réponse**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Codes d'erreur

- **400 Mauvaise requête**: URI Apose.Cells Cloud API non valide.
- **401 Non autorisé**: Jeton d'accès non valide. Ou identifiant client et secret non valides.
- **404 non trouvé**:Le fichier de feuille de calcul n'est pas accessible.
- **Erreur de serveur 500**:La feuille de calcul a rencontré une anomalie lors de l'obtention des données de calcul.

## Où devons-nous utiliser le contenu de remplacement de la plage dans la feuille de calcul distante API ?

Lorsque vous devez remplacer le contenu d'une plage dans une feuille de calcul distante, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser le contenu de remplacement de la plage dans la feuille de calcul distante API ?

- Remplacez rapidement le contenu de la plage dans les feuilles de calcul distantes.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser le contenu de remplacement de la plage dans la feuille de calcul distante API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteRange) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement le remplacement de contenu dans les feuilles de calcul pour les cellules avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}

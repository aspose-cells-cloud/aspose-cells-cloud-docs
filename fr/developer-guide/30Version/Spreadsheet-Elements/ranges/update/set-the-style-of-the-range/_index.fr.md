---
title: "Définir le style d'une plage – API Aspose.Cells Cloud"
second_title: "Documentation"
linktitle: "Définir le style d'une plage"
type: docs
url: /fr/ranges/update/style/
aliases: [  /fr/set-the-style-of-the-range/ ]
keywords: "Aspose.Cells, style de plage, API, Excel, cloud"
description: "Découvrez comment définir le style d'une plage de cellules dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut les étapes d'authentification, le format de la requête, les détails de la réponse et des exemples d'SDK pour .NET, Java, Python, Go, etc."
weight: 70
---

## **Introduction**
Cet exemple montre comment définir le style d'une plage à l'aide de l'API Aspose.Cells Cloud. Vous pouvez appeler cette API depuis de nombreux langages de programmation, notamment .NET, Java, PHP, Ruby, Python, JavaScript (jQuery), et d'autres.

## **Informations sur l'API**

| API                                                      | Type | Description                                  | Lien vers la ressource                                                                                                                         |
| -------------------------------------------------------- | ---- | -------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style        | POST | Définit le style des cellules d'une plage nommée | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **Exemple cURL**

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

**Prérequis**  
1. Obtenir un jeton d'accès via le flux d'informations d'identification client OAuth2 (`POST https://api.aspose.cloud/connect/token`).  
2. Inclure l'en-tête `Authorization: Bearer <access_token>` dans chaque requête.  

**Requête**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*L'objet `Range` spécifie la cellule en haut à gauche ainsi que la taille de la plage. L'objet `Style` contient les options de mise en forme à appliquer.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Réponse**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Gestion des erreurs** – En cas d'échec de l'appel, l'API renvoie le code d'état HTTP approprié (par exemple, 400, 401, 500) accompagné d'un corps JSON contenant les champs `Error` et `Message`. Vérifiez la valeur de `Code` ; tout résultat différent de 200 doit être enregistré et traité conformément à votre politique de gestion des erreurs.

{{< /tab >}}

{{< /tabs >}}

## **Source des SDK**
Les SDK Aspose.Cells Cloud peuvent être téléchargés à partir de la page suivante : [SDK disponibles](/cells/available-sdks/)

### **Exemples de SDK**
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
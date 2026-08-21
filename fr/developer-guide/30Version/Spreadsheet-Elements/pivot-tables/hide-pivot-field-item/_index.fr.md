---
title: "Masquer un élément de champ croisé dans un tableau croisé"
second_title: "Document"
linktype: Hide
type: docs
url: /fr/pivot-tables/hide-pivot-field-item/
aliases: [/fr/hide-pivot-field-item/]
keywords: "Aspose.Cells, masquer un élément de champ croisé, API PivotTable, API REST, SDK cloud"
description: "Découvrez comment masquer un élément de champ croisé dans un tableau croisé à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails de la requête, un exemple cURL et des extraits de code SDK pour plusieurs langages."
weight: 110
ArticleTitle: "Masquer un élément de champ croisé dans un tableau croisé – Guide de l’API Aspose.Cells Cloud"
---

Avant d'appeler l'API, assurez-vous d'avoir :

* Un **jeton d'accès JWT** valide (obtenu via le flux d'authentification Aspose Cloud).  
* Le classeur cible téléchargé dans votre stockage Aspose Cloud.  
* La feuille de calcul et le tableau croisé déjà créés.

Ces conditions préalables évitent les erreurs d'authentification et les réponses « ressource introuvable ». Les étapes suivantes décrivent la configuration nécessaire avant d'invoquer l'API.

Cette API REST permet de masquer un élément de champ croisé dans un tableau croisé.

## API PostPivotTableFieldHideItem

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                                                      |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------ |
| name             | string  | path        | Nom du fichier Excel.                                                                            |
| sheetName        | string  | path        | Feuille de calcul contenant le tableau croisé.                                                   |
| pivotTableIndex  | integer | path        | Index du tableau croisé dans la feuille de calcul.                                               |
| pivotFieldType   | string  | query       | Type du champ croisé (Row, Column, Page, Data, etc.).                                           |
| fieldIndex       | integer | query       | Index (à partir de zéro) du champ croisé à modifier.                                             |
| itemIndex        | integer | query       | Index (à partir de zéro) de l'élément spécifique à masquer dans le champ.                        |
| isHide           | boolean | query       | Définir sur **true** pour masquer l’élément ; **false** pour l'afficher.                         |
| needReCalculate  | boolean | query       | Indique si le tableau croisé doit être recalculé après la modification. La valeur par défaut est **false**. |
| folder           | string  | query       | Chemin du dossier où le classeur est stocké.                                                     |
| storageName      | string  | query       | Nom du service de stockage.                                                                      |

**Référence rapide des paramètres de requête requis**

- **pivotFieldType** – type du champ (par exemple, `Row`).  
- **fieldIndex** – index (à partir de zéro) du champ à modifier.  
- **itemIndex** – index (à partir de zéro) de l’élément à masquer/afficher.  
- **isHide** – `true` pour masquer, `false` pour afficher.  
- **needReCalculate** – facultatif, valeur par défaut : `false`.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Détails de la réponse**

| Code d’état | Description                                                           |
| ----------- | --------------------------------------------------------------------- |
| 200         | L’élément a été masqué avec succès.                                  |
| 400         | Requête incorrecte – paramètres manquants ou non valides.            |
| 401         | Non autorisé – jeton JWT invalide ou manquant.                       |
| 500         | Erreur serveur – l’opération n’a pas pu être terminée.               |

**Remarque :** Si l’index de champ (`fieldIndex`) ou l’index d’élément (`itemIndex`) fourni est hors limite, l’API renvoie une réponse **400 Bad Request**.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer avec l’API. Les SDK gèrent les détails de bas niveau, afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment masquer un élément de champ croisé à l’aide de divers SDK.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // Préparer le classeur et la feuille de calcul
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Télécharger le classeur
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Créer la feuille de calcul qui contiendra le tableau croisé
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Créer une deuxième feuille de calcul avec des données d'exemple
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Importer des données d'exemple dans Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // Raccourci pour la concision
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Ajouter un tableau croisé dynamique à PivotSheet
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Masquer un élément spécifique du champ ligne
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**Remarque :** Les exemples SDK supposent que vous avez déjà configuré l'authentification (jeton JWT) et que le classeur se trouve dans le dossier de stockage spécifié. Ajustez les paramètres `folder` et `storageName` en fonction de votre environnement.
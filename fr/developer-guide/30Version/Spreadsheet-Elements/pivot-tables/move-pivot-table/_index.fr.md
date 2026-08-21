---
title: "Déplacer un tableau croisé dynamique dans un fichier Excel"
second_title: "Document"
linktitle: Déplacer
type: docs
url: /fr/pivot-tables/move/
aliases: [  /fr/move-pivot-table/ ]
keywords: "Aspose.Cells Cloud, déplacer un tableau croisé dynamique, Excel, API REST, SDK, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Découvrez comment utiliser l'API REST Aspose.Cells Cloud pour déplacer un tableau croisé dynamique au sein d'un classeur Excel. Des SDK sont disponibles pour Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift."
weight: 120
---

Cet API REST permet de déplacer un tableau croisé dynamique au sein d’un classeur Excel.

**Prérequis :** Avant d’appeler cette opération, vous devez disposer d’un jeton d’accès JWT valide et le classeur doit être stocké dans le stockage Aspose Cloud. Spécifiez les paramètres `folder` (dossier) et `storageName` (nom du service de stockage) selon vos besoins.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Move
```

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                  |
|------------------|---------|-------------|--------------------------------------------------------------|
| name             | string  | chemin      | Nom du fichier Excel.                                        |
| sheetName        | string  | chemin      | Nom de la feuille de calcul contenant le tableau croisé dynamique. |
| pivotTableIndex  | integer | chemin      | Index de base zéro du tableau croisé dynamique à déplacer.   |
| fieldIndex       | integer | requête     | Index du champ croisé dynamique à déplacer.                  |
| from             | string  | requête     | Zone source du champ (par exemple, `Row` ou `Column`).       |
| to               | string  | requête     | Zone de destination du champ (par exemple, `Row` ou `Column`). |
| folder           | string  | requête     | Dossier dans le stockage où le fichier est situé.            |
| storageName      | string  | requête     | Nom du service de stockage.                                  |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldMoveTo) définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Move?fieldIndex=0&from=C1&to=C10" \
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

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Utilisez des points de terminaison HTTPS en production.
public void Run_PivotTable_Move()
{
    url = @"https://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null}, ... ],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/Move?row=10&column=10&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Move?fieldIndex=1&from=Row&to=Column&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "60360c7d035abd1b2c9e36c68c9f00fb" >}}

{{< /tab >}}

{{< /tabs >}}
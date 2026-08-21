---
title: "Trier les données d’un ListObject dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Trier"
type: docs
url: /fr/list-objects/sort-data/
aliases: [  /fr/get-a-list-object-or-table-inside-the-worksheet/ , /fr/tables/sort-data/ ]
keywords: "Aspose.Cells Cloud, Excel, ListObject, Trier les données, API REST, Feuille de calcul"
description: "Découvrez comment trier les données d’un ListObject (tableau) dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’URL du point de terminaison, les paramètres, une requête cURL d’exemple et des exemples de SDK."
weight: 40
ArticleTitle: "Trier les données d’un ListObject dans une feuille de calcul Excel – API Aspose.Cells Cloud"
---

**Conditions préalables**  
Pour appeler cette API, vous devez disposer d’un jeton d’accès JWT valide pour Aspose Cloud, et le classeur doit avoir été chargé dans le stockage Aspose Cloud. Incluez l’en-tête `Authorization: Bearer <jeton JWT>` dans chaque requête.

Cette API REST permet de trier les données d’un tableau dans une feuille de calcul Excel.  
Pour utiliser cette opération, fournissez le nom du classeur, le nom de la feuille de calcul et l’index du ListObject cible, ainsi qu’un corps JSON `dataSorter` définissant les critères de tri.

## API PostWorksheetListObjectSortTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                     |
| ---------------- | ------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------- |
| name             | string  | path                                                   | Nom du fichier Excel stocké dans le stockage Aspose Cloud.                                                     |
| sheetName        | string  | path                                                   | Nom de la feuille de calcul contenant le ListObject.                                                           |
| listObjectIndex  | integer | path                                                   | Index de base zéro du ListObject (tableau) dans la feuille de calcul.                                          |
| dataSorter       | object  | body                                                   | Objet JSON spécifiant les options de tri (par exemple, `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`). |
| folder           | string  | query                                                  | Chemin du dossier dans le stockage où se trouve le fichier Excel.                                              |
| storageName      | string  | query                                                  | Nom du stockage Aspose Cloud.                                                                                   |

**Remarques**  
Le corps de la requête doit être un objet JSON valide conforme au schéma `dataSorter`. Assurez-vous que le classeur, la feuille de calcul et le ListObject existent avant d’appeler l’opération de tri.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code de statut | Description                                           |
|----------------|-------------------------------------------------------|
| 200            | OK – tri terminé avec succès.                        |
| 400            | Requête incorrecte – paramètres invalides.          |
| 401            | Non autorisé – échec de l’authentification.         |
| 404            | Introuvable – classeur, feuille de calcul ou ListObject non trouvé(s). |
| 500            | Erreur interne du serveur – problème côté serveur.  |

**Paramètres de la réponse**

| Paramètre | Type   | Description                                   |
|-----------|--------|-----------------------------------------------|
| Code      | integer| Code de statut HTTP renvoyé par l’API.        |
| Status    | string | Description textuelle du résultat (par ex., "OK"). |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[Retour à la vue d’ensemble des ListObjects](/list-objects/)
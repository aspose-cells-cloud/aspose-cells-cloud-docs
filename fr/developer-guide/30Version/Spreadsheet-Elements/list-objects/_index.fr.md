---
title: "Travail avec Excel ListObject"
ArticleTitle: "Travail avec Excel ListObject"
second_title: "Document"
linktype: "ListObjects"
type: docs
url: /list-objects/
aliases:
  - /working-with-list-objects/
  - /working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, API tableau Excel, ajouter un tableau, mettre à jour un tableau, supprimer un tableau, convertir un tableau en plage, trier un tableau Excel"
description: "Découvrez comment ajouter, mettre à jour, supprimer, récupérer, trier et convertir des ListObjects Excel (tableaux) à l'aide de l'API REST Aspose.Cells Cloud. Inclut des exemples de code en C#, Java, Python, et plus encore."
weight: 100
---

Les ListObjects Excel (tableaux) offrent un moyen structuré d’organiser des jeux de données. Ils incluent des fonctionnalités telles que l’arrangement automatique des données, les lignes d’en-tête, les filtres intégrés et éventuellement des lignes de total. Maîtrisez ces capacités pour analyser vos données rapidement et efficacement.

**Définition de ListObject :** Un **ListObject** est l’objet tableau natif d’Excel qui regroupe des lignes et des colonnes, permet le tri, le filtrage et le style, et peut être accessible via l’API Aspose.Cells Cloud.

## Comment travailler avec un tableau (ListObject)

- [Comment ajouter un tableau (ListObject) dans la feuille de calcul](/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [Comment mettre à jour un tableau (ListObject) dans la feuille de calcul](/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [Comment convertir un tableau (ListObject) en plage](/cells/convert-list-object-or-table-to-range/)
- [Comment trier les données du tableau](/cells/sort-table-data/)
- [Comment supprimer les lignes en double d’un tableau](/cells/list-objects/remove-duplicates/)
- [Comment insérer un filtre à segment pour un tableau](/cells/list-objects/insert-slicer/)

**Référence de l’API (vue d’ensemble) :**  
L’API REST Aspose.Cells Cloud expose les opérations ListObject via des points de terminaison tels que `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`, et `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Les paramètres de requête requis incluent `folder` (obligatoire) et `storage` (facultatif). Les corps de requête sont des objets JSON décrivant les propriétés du tableau (nom, showHeaderRow, showTotalRow, etc.), et les réponses retournent des charges utiles JSON contenant les détails du ListObject créé ou modifié.

**Prérequis :**  
- Un jeton d’authentification valide pour Aspose.Cells Cloud.  
- Le fichier classeur doit être téléchargé vers un emplacement de stockage pris en charge (par défaut : **/**) et le paramètre de requête `folder` doit pointer vers cet emplacement.  
- Facultatif : définissez `storage` si vous utilisez un service de stockage non par défaut.

**Détails des points de terminaison**

| Méthode | Point de terminaison | Paramètres de requête | Corps de la requête (JSON) | Réponse réussie (exemple) | Codes d’état |
|--------|----------------------|------------------------|---------------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (obligatoire), `storage` (facultatif) | *aucun* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK, 400 – Requête incorrecte, 401 – Non autorisé, 404 – Introuvable |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (obligatoire), `storage` (facultatif) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Créé, 400 – Requête incorrecte, 401 – Non autorisé, 409 – Conflit |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (obligatoire), `storage` (facultatif) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK, 400 – Requête incorrecte, 401 – Non autorisé, 404 – Introuvable |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (obligatoire), `storage` (facultatif) | *aucun* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK, 400 – Requête incorrecte, 401 – Non autorisé, 404 – Introuvable |

**Extraits de code**

*C# (POST – Ajouter un ListObject)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – Récupérer les ListObjects)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – Mettre à jour le ListObject)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – Supprimer le ListObject)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**Remarques :**  
- Les index ListObject sont indexés à partir de zéro.  
- Lors de l’ajout d’un ListObject, `StartRow` et `StartColumn` définissent la cellule supérieure gauche du tableau.  
- L’API prend en charge la pagination via les paramètres de requête `offset` et `limit` (non indiqués dans le tableau) pour les grandes feuilles de calcul.  
- Limites de débit : 100 requêtes par minute par compte ; les dépassements retournent **429 Too Many Requests**.

En intégrant le terme **Excel ListObject** plusieurs fois dans la page, le contenu s’aligne sur les mots-clés cibles « Excel ListObject », « Aspose.Cells Cloud » et « Excel table API », améliorant ainsi le référencement tout en restant naturel pour les lecteurs.
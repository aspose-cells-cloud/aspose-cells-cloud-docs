---
title: "Comment obtenir le contenu d'une plage dans une feuille Excel"
second_title: "Document"
linktype: "Get"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel, API, obtenir, plage, feuille de calcul, REST"
description: "Découvrez comment récupérer le contenu d'une plage dans une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut la syntaxe de la requête et du code d'exemple."
weight: 20
ArticleTitle: "Comment obtenir le contenu d'une plage dans une feuille Excel – Aspose.Cells Cloud API"
---

## Travailler avec la récupération du contenu d'une plage dans une feuille Excel

- [Comment obtenir les données d'une cellule à partir d'une plage nommée](/cells/ranges/get/values/)
- [Comment obtenir une plage nommée à partir d'un classeur Excel](/cells/ranges/get/name/)

**Prérequis**

- Un jeton d'accès valide Aspose Cloud (ou `client_id`/`client_secret` pour OAuth).
- Le fichier Excel doit être uploadé dans le dossier de stockage cible.
- SDK Aspose.Cells Cloud version 3.0 ou ultérieure.

L'opération **Get Range** (Obtenir la plage) renvoie le contenu d'une plage spécifiée dans une feuille de calcul.  
Il s'agit d'une simple requête `GET` qui renvoie les données de la plage au format JSON (ou dans d'autres formats si demandé).

**Aperçu de la requête**

| Élément | Valeur |
|---------|-------|
| **Méthode HTTP** | `GET` |
| **Point de terminaison** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **Paramètres de chemin** | `fileName` – nom du fichier Excel (y compris l'extension) <br> `sheetName` – nom de la feuille de calcul <br> `rangeName` – nom de la plage (par ex. `A1:B10`) |
| **Paramètres de requête** (facultatifs) | `folder` – dossier de stockage <br> `storage` – nom du stockage <br> `outFormat` – format de la réponse (par ex. `json`, `xml`) |
| **En-têtes** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**Exemple cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer VOTRE_JETON_D_ACCES" \
     -H "Accept: application/json"
```

**Exemple en C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**Exemple en Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**Exemple en Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**Schéma de réponse (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Valeur1", "Valeur2"]
    ]
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou invalides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier uploadé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |

- `200 OK` – Plage récupérée avec succès.  
- `400 Bad Request` – Paramètres manquants ou invalides.  
- `401 Unauthorized` – Jeton d'accès invalide ou manquant.  
- `404 Not Found` – Le fichier, la feuille de calcul ou la plage spécifiée est introuvable.  
- `500 Internal Server Error` – Erreur inattendue du serveur.

**Exemples de réponses d’erreur**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "Les paramètres de la requête sont invalides ou manquants."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "Jeton d'accès invalide ou manquant."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "Le fichier, la feuille de calcul ou la plage spécifiée est introuvable."
}
```

**Voir aussi**

- [Comment obtenir les données d'une cellule à partir d'une plage nommée](/cells/ranges/get/values/)  
- [Comment obtenir une plage nommée à partir d'un classeur Excel](/cells/ranges/get/name/)  
- [Mettre à jour le contenu d'une plage](/cells/ranges/update/)  
- [Supprimer une plage](/cells/ranges/delete/)  
---
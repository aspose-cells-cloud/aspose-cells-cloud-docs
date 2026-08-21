---
title: Supprimer le saut de page vertical – API REST Aspose.Cells Cloud
description: Supprimer un saut de page vertical d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut la syntaxe de la requête, les paramètres, les exemples, les codes de réponse et les extraits de code SDK.
keywords: supprimer le saut de page vertical, Aspose.Cells Cloud, API REST
slug: delete-vertical-page-break
api_version: v3.0
---

# Supprimer le saut de page vertical

Supprimez un saut de page vertical d'une feuille de calcul dans un classeur Excel à l'aide de l'API REST Aspose.Cells Cloud.

---

## Conditions préalables

* Un **jeton d’authentification JWT** doit être fourni dans l’en-tête `Authorization`.  
* Le classeur (`{name}`) doit être stocké dans le **dossier** ou le **stockage** spécifié et être accessible au client de l’API.

---

## Requête HTTP

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| Paramètre | Type   | Emplacement | Obligatoire | Description |
|-----------|--------|-------------|-------------|-------------|
| **name**      | string | chemin   | Oui | Le nom du fichier Excel. |
| **sheetName** | string | chemin   | Oui | Le nom de la feuille de calcul contenant le saut de page. |
| **index**     | integer| chemin   | Oui | Index de base zéro du saut de page vertical à supprimer. |
| **folder**    | string | requête  | Non | Chemin du dossier où le fichier est stocké. |
| **storageName**| string| requête  | Non | Nom du service de stockage. |

---

## Exemple de requête

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton_jwt>"
```

---

## Réponse en cas de succès

| Code | Description |
|------|-------------|
| **200** | Le saut de page vertical a été supprimé avec succès. |

**Exemple de corps de réponse**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Réponses d’erreur

| Code HTTP | Description |
|-----------|-------------|
| **401** | Non autorisé – jeton manquant ou invalide. |
| **404** | Introuvable – le fichier, la feuille de calcul ou l’index de saut de page spécifié n’existe pas. |
| **400** | Requête incorrecte – syntaxe de la requête incorrecte ou paramètres invalides. |
| **500** | Erreur interne du serveur – une condition inattendue s’est produite. |

**Exemples de corps d’erreur**

*401 – Non autorisé*

```json
{
  "Code": 401,
  "Message": "Jeton d’authentification invalide."
}
```

*404 – Introuvable*

```json
{
  "Code": 404,
  "Message": "Le fichier, la feuille de calcul ou l’index de saut de page spécifié est introuvable."
}
```

*400 – Requête incorrecte*

```json
{
  "Code": 400,
  "Message": "Les paramètres de la requête sont invalides ou mal formés."
}
```

*500 – Erreur interne du serveur*

```json
{
  "Code": 500,
  "Message": "Une erreur inattendue s’est produite sur le serveur."
}
```

---

## Exemples de code SDK

Les exemples suivants montrent comment appeler l’opération **DeleteVerticalPageBreak** à l’aide des divers SDK Aspose.Cells Cloud.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status : {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception lors de l’appel à CellsApi.DeleteVerticalPageBreak : " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status : " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status :", response.status)
except Exception as e:
    print("Erreur :", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status :', response.status))
  .catch(error => console.error('Erreur :', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Erreur :", err)
        return
    }
    fmt.Println("Status :", resp.Status)
}
```

</details>

*(Les extraits de code SDK pour PHP, Ruby, Perl et d’autres langues suivent le même modèle et sont disponibles dans le dépôt GitHub officiel.)*

---

## Ressources connexes

* **Spécification OpenAPI** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **SDK Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>  
* **Guide d’authentification** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*Dernière mise à jour du document : 2026‑07‑30*
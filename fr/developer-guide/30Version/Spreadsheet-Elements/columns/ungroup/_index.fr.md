---
title: Dégrouper des colonnes dans Excel – Aspose.Cells Cloud API  
description: Supprimer le regroupement des colonnes dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’URL du point de terminaison, les paramètres requis, la méthode d’authentification, un exemple d’appel cURL, le format de réponse et des extraits de code pour les SDK.  
keywords: Aspose.Cells, dégrouper, colonnes, Excel, API, REST, cloud, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# Dégrouper des colonnes dans Excel  

Aspose.Cells Cloud propose une opération **POST** permettant de supprimer le regroupement des colonnes d’une feuille de calcul spécifiée. Cette page décrit le format de la requête, les paramètres requis, la méthode d’authentification, des exemples d’appels et l’utilisation des SDK.

---

## Conditions préalables  

| Exigence | Raison |
|----------|--------|
| **Compte Aspose Cloud** | Accès aux services Aspose.Cells Cloud. |
| **Jeton d’accès JWT** | Toutes les requêtes d’API doivent être autorisées à l’aide d’un jeton « bearer ». Voir le [guide d’authentification JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Classeur stocké dans le stockage Aspose Cloud** | L’API traite les fichiers situés dans le stockage cloud (ou dans un stockage externe connecté). |
| **Nom de la feuille de calcul** | La feuille de calcul cible doit exister dans le classeur. |

---

## Authentification  

Toutes les requêtes nécessitent un en‑tête **Authorization** contenant un jeton JWT valide :

```http
Authorization: Bearer <access_token>
```

Le jeton est obtenu via le flux OAuth d’Aspose Cloud. Les jetons ont une durée de validité limitée ; veuillez les actualiser si nécessaire.

---

## Point de terminaison  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Chemin** – Nom du fichier classeur (par ex. `test.xlsx`).  
* `{sheetName}` – **Chemin** – Nom de la feuille de calcul (par ex. `Sheet1`).  

---

## Paramètres  

### Paramètres de chemin  

| Nom | Type | Obligatoire | Description |
|-----|------|-------------|-------------|
| `name` | string | Oui | Nom du fichier classeur. |
| `sheetName` | string | Oui | Nom de la feuille de calcul. |

### Paramètres de requête  

| Nom | Type | Obligatoire | Description |
|-----|------|-------------|-------------|
| `firstIndex` | integer | Oui | Index de la première colonne à dégrouper (indexation à partir de 0). |
| `lastIndex` | integer | Oui | Index de la dernière colonne à dégrouper (indexation à partir de 0). |
| `folder` | string | Non | Chemin du dossier contenant le classeur. |
| `storageName` | string | Non | Nom du service de stockage où se trouve le fichier. |

---

## Exemple de requête (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*Remplacez `<access_token>` par un jeton JWT valide.*

---

## Réponse réussie  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

L’objet de réponse (`CellsCloudResponse`) contient l’intervalle de colonnes qui a été dégroupé avec succès.

### Réponse en cas d’erreur  

Lorsque la requête échoue, le service renvoie une charge utile JSON comportant les champs suivants :

| Champ | Signification |
|-------|---------------|
| `Code` | Code d’erreur conforme à HTTP (par ex. 400, 401). |
| `Status` | Description brève de l’erreur. |
| `ErrorMessage` | Description détaillée de l’erreur. |

---

**Codes d’état HTTP**

| Code | Signification               | Description                                               |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille autorisée. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |
---

## Extraits de code pour les SDK  

Ci-dessous figurent des extraits prêts à l’emploi pour les SDK les plus populaires. Remplacez les valeurs génériques (par ex. `<YourAccessToken>`, `<YourFileName>`, etc.) par vos propres données.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Colonnes dégroupées : {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Colonnes dégroupées : " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Colonnes dégroupées : {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Colonnes dégroupées : ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Colonnes dégroupées : %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **Remarque :** Les SDK pour PHP, Ruby, Perl et d’autres langages suivent le même ordre des paramètres. Reportez-vous au [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir des exemples complets.

---

## Références  

* **Spécification OpenAPI :** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **Guide d’authentification :** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **Dépôt des SDK :** <https://github.com/aspose-cells-cloud>

---

## Historique des révisions  

| Date | Auteur | Modification |
|------|--------|--------------|
| 2026‑07‑30 | Optimiseur IA | Correction de l’encodage UTF‑8, ajout des conditions préalables, nettoyage des mots‑clés méta, amélioration de la hiérarchie des titres et insertion d’exemples de code SDK. |
| 2026‑07‑29 | Original | Brouillon initial de la documentation. |

---
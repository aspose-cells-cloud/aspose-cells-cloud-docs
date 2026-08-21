---
title: Obtenir les détails de la colonne – Référence de l’API Aspose.Cells Cloud (v4.0)
description: Récupérer des informations détaillées sur une colonne de feuille de calcul (index, largeur, style, état masqué) à l’aide de l’API REST Aspose.Cells Cloud.
keywords: Aspose.Cells, API Cloud, colonne Excel, obtenir une colonne, API REST, JWT, feuille de calcul
date: 2026-07-30
---

# Obtenir les détails de la colonne  

Récupérez des informations détaillées sur une colonne spécifique d’une feuille de calcul (index, largeur, style, état masqué) à partir d’un classeur Excel stocké dans Aspose Cloud.

## Table des matières
1. [Conditions préalables](#prerequisites)  
2. [Authentification](#authentication)  
3. [Endpoint](#endpoint)  
4. [Paramètres de la requête](#request-parameters)  
5. [Exemple cURL](#curl-example)  
6. [Exemple de réponse](#response-example)  
7. [Schéma de réponse](#response-schema)  
8. [Erreurs possibles](#possible-errors)  
9. [Exemples de SDK](#sdk-examples)  
10. [Ressources supplémentaires](#additional-resources)  

---

## Conditions préalables
- Un **jeton d’accès JWT** valide obtenu via l’authentification Aspose Cloud.  
- Le fichier du classeur doit être stocké dans le stockage Aspose Cloud (ou un autre stockage pris en charge), et le chemin du dossier (le cas échéant) doit être connu.  

---

## Authentification
Toutes les API Aspose.Cells Cloud utilisent l’**authentification par jeton JWT**. Incluez le jeton dans l’en-tête `Authorization` :

```http
Authorization: Bearer <access_token>
```

Pour plus de détails sur l’obtention d’un jeton, consultez le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Endpoint
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – nom du fichier du classeur (par exemple, `test.xlsx`).  
- **{sheetName}** – nom de la feuille de calcul (par exemple, `Sheet1`).  
- **{columnIndex}** – index de la colonne à récupérer (indexation à partir de zéro).

---

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

## Paramètres de la requête

| Nom              | Emplacement | Type    | Obligatoire | Description |
|------------------|-------------|---------|------------|-------------|
| **name**         | path        | string  | Oui        | Nom du fichier du classeur. |
| **sheetName**    | path        | string  | Oui        | Feuille de calcul contenant la colonne. |
| **columnIndex**  | path        | integer | Oui        | Index (à partir de zéro) de la colonne à récupérer. |
| **folder**       | query       | string  | Non        | Dossier de stockage où réside le classeur. |
| **storageName**  | query       | string  | Non        | Nom du service de stockage (par exemple, Aspose Cloud Storage). |

---

## Exemple cURL
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## Exemple de réponse
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Schéma de réponse
| Champ                 | Type    | Description |
|-----------------------|---------|-------------|
| `Column.GroupLevel`   | integer | Niveau de regroupement (outline) de la colonne (utilisé pour le groupement). |
| `Column.Index`        | integer | Index de la colonne (à partir de zéro). |
| `Column.IsHidden`     | boolean | `true` si la colonne est masquée ; sinon `false`. |
| `Column.Width`        | number  | Largeur de la colonne exprimée en caractères. |
| `Column.Style`        | object  | Contient un lien vers la ressource de style de la colonne. |
| `Column.link`         | object  | Lien auto-référentiel vers la ressource de la colonne. |
| `Code`                | integer | Code d’état HTTP de la réponse. |
| `Status`              | string  | Description textuelle de l’état (par exemple, **OK**). |

---

## Erreurs possibles
| Statut HTTP | Code | Message                        | Situation |
|-------------|------|--------------------------------|-----------|
| 400         | 400  | Bad Request (Requête incorrecte) | Paramètres obligatoires manquants ou mal formés. |
| 401         | 401  | Unauthorized (Non autorisé)      | En-tête `Authorization` manquant ou jeton invalide. |
| 404         | 404  | Not Found (Introuvable)          | Le classeur, la feuille de calcul ou la colonne n’existe pas. |
| 500         | 500  | Internal Server Error (Erreur interne du serveur) | Problème inattendu côté serveur. |

### Exemple – 404 Introuvable
```json
{
  "Code": 404,
  "Message": "L’index de colonne est hors de portée."
}
```

### Exemple – 401 Non autorisé
```json
{
  "Code": 401,
  "Message": "Jeton d’authentification invalide ou manquant."
}
```

---

## Exemples de SDK
Les extraits de code suivants montrent comment appeler l’opération **Get Worksheet Columns** à l’aide des SDK officiels Aspose.Cells Cloud. Si un Gist devient indisponible, le code d’exemple est fourni ci-dessous.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// Configuration du client API
var apiInstance = new CellsApi("client_id", "client_secret");

// Définition des paramètres obligatoires
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // optionnel
string storageName = "MyStorage";    // optionnel

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Index de la colonne : " + response.Column.Index);
    Console.WriteLine("Largeur : " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Exception lors de l’appel à CellsApi.GetWorksheetColumns : " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // optionnel
        String storageName = "MyStorage";    // optionnel

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Index de la colonne : " + result.getColumn().getIndex());
            System.out.println("Largeur : " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Exception lors de l’appel à CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # optionnel
storage_name = "MyStorage"  # optionnel

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Index de la colonne :", response.column.index)
    print("Largeur :", response.column.width)
except Exception as e:
    print("Exception lors de l’appel à CellsApi->get_worksheet_columns :", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // optionnel
const storageName = "MyStorage"; // optionnel

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Index de la colonne :", result.column?.index);
        console.log("Largeur :", result.column?.width);
    })
    .catch((error) => {
        console.error("Erreur lors de l’appel à getWorksheetColumns :", error);
    });
```

</details>

> **Remarque :** Tous les SDK gèrent automatiquement l’en-tête `Authorization` une fois que vous avez fourni `client_id` et `client_secret`.

---

## Ressources supplémentaires
- **Spécification OpenAPI :** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **Guide d’authentification :** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **Dépôt GitHub (SDK et exemples) :** <https://github.com/aspose-cells-cloud>  

--- 

*Document mis à jour pour la dernière fois le 2026-07-30.*
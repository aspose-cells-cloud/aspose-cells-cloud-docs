---
title: "Récupérer une seule ligne d'une feuille Excel à l'aide de l'API Aspose.Cells Cloud"
description: "Découvrez comment récupérer une ligne spécifique d'une feuille Excel stockée dans le stockage Aspose Cloud à l'aide de l'API REST Aspose.Cells Cloud. Inclut la syntaxe de requête, les paramètres, le schéma de réponse, un exemple cURL et du code SDK (C#, Java, Python)."
keywords: "Aspose.Cells Cloud, récupérer une ligne, API Excel, REST pour feuilles de calcul, SDK C#, SDK Java, SDK Python"
date: 2026-07-30
api_version: "v3.0"
---

# Récupérer une seule ligne d'une feuille Excel

**Point de terminaison** : `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Récupère une ligne à partir d'une feuille de calcul stockée dans le stockage Aspose Cloud. Cette opération nécessite un jeton d'accès OAuth 2.0 valide doté du périmètre **Read** (Lecture).

---

## Table des matières
1. [Conditions préalables](#prerequisites)  
2. [Requête HTTP](#http-request)  
3. [Paramètres](#parameters)  
   - [Paramètres de chemin](#path-parameters)  
   - [Paramètres de requête](#query-parameters)  
4. [Exemple cURL](#curl-example)  
5. [Réponse](#response)  
   - [Schéma de succès](#success-schema)  
   - [Codes de statut](#status-codes)  
6. [Exemples de code SDK](#sdk-code-samples)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [Opérations associées](#related-operations)  
8. [Notes et limites](#notes--limits)  

---

## Prerequisites  
- **Compte Aspose Cloud** avec un abonnement actif.  
- **Jeton d'accès OAuth 2.0** incluant le périmètre **Read** (Lecture).  
- Le classeur cible doit déjà exister dans le stockage Aspose Cloud.  

---

## Requête HTTP
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*URL de base* : `https://api.aspose.cloud/v3.0`

---

## Paramètres

### Paramètres de chemin
| Nom       | Type   | Obligatoire | Description                                      |
|-----------|--------|-------------|--------------------------------------------------|
| `name`    | chaîne | ✅          | Nom du fichier du classeur (par ex. `MonClasseur.xlsx`). |
| `sheetName`| chaîne | ✅         | Nom de la feuille de calcul (par ex. `Feuil1`). |
| `rowIndex`| entier | ✅          | Index de base zéro de la ligne à récupérer.     |

### Paramètres de requête *(facultatifs)*
| Nom            | Type   | Obligatoire | Description |
|----------------|--------|-------------|-------------|
| `folder`       | chaîne | ❌          | Chemin du dossier dans le stockage cloud où réside le classeur. |
| `storageName`  | chaîne | ❌          | Nom du service de stockage (si vous utilisez un stockage personnalisé). |

---

## Exemple cURL
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MonClasseur.xlsx/worksheets/Feuil1/rows/5?folder=Docs&storageName=MonStockage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Réponse

### Schéma de succès (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* objet de style */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...cellules supplémentaires... */
    ]
  }
}
```

### Codes de statut
| Code | Signification |
|------|---------------|
| **200** | Ligne récupérée avec succès. |
| **401** | Non autorisé – jeton d'accès manquant ou invalide. |
| **404** | Classeur, feuille de calcul ou ligne introuvable. |
| **500** | Erreur interne du serveur. |

### Exemple d'erreur (`401 Non autorisé`)
```json
{
  "Code": 401,
  "Message": "Le jeton d'accès est manquant ou invalide."
}
```

---

## Exemples de code SDK

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "VOTRE_ID_CLIENT";
var clientSecret = "VOTRE_SECRET_CLIENT";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MonClasseur.xlsx",
    sheetName: "Feuil1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // facultatif
);

Console.WriteLine($"Ligne {response.Row.Index} récupérée avec {response.Row.Cells.Count} cellules.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("VOTRE_ID_CLIENT", "VOTRE_SECRET_CLIENT");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MonClasseur.xlsx",
    "Feuil1",
    5,
    "Docs",
    null   // storageName – facultatif
);

System.out.println("Index de la ligne : " + response.getRow().getIndex());
System.out.println("Nombre de cellules : " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "VOTRE_ID_CLIENT"
client_secret = "VOTRE_SECRET_CLIENT"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MonClasseur.xlsx",
        sheet_name="Feuil1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Ligne {response.row.index} récupérée avec {len(response.row.cells)} cellules.")
except ApiException as e:
    print("Exception lors de l'appel à CellsApi->cells_rows_get_worksheet_row :", e)
```

---

## Opérations associées
| Opération | Description |
|-----------|-------------|
| **Ajouter une ligne** | `POST /cells/{name}/worksheets/{sheetName}/rows` – Insère une nouvelle ligne dans une feuille de calcul. |
| **Supprimer une ligne** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – Supprime une ligne existante. |
| **Récupérer plusieurs lignes** | `GET /cells/{name}/worksheets/{sheetName}/rows` – Récupère une collection de lignes. |
| **Vue d'ensemble des lignes** | `/cells/rows/` – Documentation générale relative aux points de terminaison liés aux lignes. |

---

## Notes et limites
- **Limite de débit** : 100 requêtes par minute et par compte.  
- **Formats pris en charge** : XLS, XLSX, CSV, ODS.  
- L'index de ligne est en **base zéro** ; la première ligne a pour index `0`.  
- Assurez-vous que le classeur est uploadé dans le dossier spécifié par `folder` avant d'appeler ce point de terminaison.  

---
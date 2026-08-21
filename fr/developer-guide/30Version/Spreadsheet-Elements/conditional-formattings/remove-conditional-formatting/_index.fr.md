---
title: "Supprimer le formatage conditionnel – Référence de l’API Aspose.Cells Cloud"
type: docs
url: /fr/conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, Formatage conditionnel, Supprimer, API, Excel, Cloud"
description: "Supprimer une règle de formatage conditionnel d’une feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud. Inclut les paramètres, l’authentification, des exemples de requête/réponse et des extraits de code SDK."
weight: 60
---

# Supprimer le formatage conditionnel

## Contexte
Le formatage conditionnel permet d’appliquer des styles visuels aux cellules qui remplissent des critères spécifiques (par exemple, mettre en surbrillance les valeurs supérieures à un seuil). Dans des scénarios d’automatisation, vous pouvez avoir besoin de supprimer une règle existante. Ce point de terminaison supprime une règle de formatage conditionnel d’une feuille de calcul d’un classeur Excel stocké dans le stockage Aspose Cloud.

## Conditions préalables
- Un compte **Aspose Cloud** avec le produit **Cells** activé.  
- **Jeton d’accès JWT** généré via le flux d’informations d’identification client OAuth 2.0.  
- Le classeur (`{name}`) doit déjà exister dans le **dossier** spécifié et le **stockage** (le cas échéant).  
- La version de l’API **v3.0** (par défaut) est utilisée dans les URL affichées ci-dessous.

## Authentification
Tous les points de terminaison d’Aspose.Cells Cloud nécessitent une authentification basée sur un jeton JWT.

```http
Authorization: Bearer <access_token>
```

### Obtenir un jeton d’accès (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**Réponse**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Utilisez le `access_token` renvoyé dans l’en-tête `Authorization` pour chaque requête.

## Requête HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Paramètres de chemin

| Nom          | Type    | Obligatoire | Description |
|--------------|---------|-------------|-------------|
| `name`       | string  | Oui         | Nom du fichier de classeur (par exemple, `Book1.xlsx`). |
| `sheetName`  | string  | Oui         | Feuille de calcul contenant le formatage conditionnel. |
| `index`      | integer | Oui         | Index à base zéro de la règle de formatage conditionnel à supprimer. |

### Paramètres de requête

| Nom            | Type   | Obligatoire | Description |
|----------------|--------|-------------|-------------|
| `folder`       | string | Non         | Dossier Cloud où réside le classeur. |
| `storageName`  | string | Non         | Nom du service de stockage Aspose Cloud. |

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Réponse réussie

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification        | Description |
|------|----------------------|-------------|
| 200  | OK                   | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête     | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé         | Jeton JWT non valide ou manquant. |
| 413  | Charge utile trop grande | Le fichier envoyé dépasse la limite de taille. |
| 500  | Erreur interne du serveur | Erreur serveur inattendue. |

## Réponses d’erreur

| Code HTTP | Raison | Corps d’exemple |
|-----------|--------|-----------------|
| **400**   | Mauvaise requête – paramètres manquants ou non valides. | `{ "Code":"400", "Message":"Valeur de paramètre non valide." }` |
| **401**   | Non autorisé – jeton JWT manquant ou non valide. | `{ "Code":"401", "Message":"Jeton d’accès manquant ou non valide." }` |
| **404**   | Non trouvé – le classeur ou la feuille de calcul n’existe pas. | `{ "Code":"404", "Message":"Fichier introuvable." }` |
| **500**   | Erreur interne du serveur – défaillance serveur inattendue. | `{ "Code":"500", "Message":"Une erreur inattendue s’est produite." }` |

## Exemples de SDK
Les extraits suivants illustrent comment invoquer l’opération **Supprimer le formatage conditionnel** à l’aide des SDK officiels d’Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// Configuration du client API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// Supprimer le formatage conditionnel
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Formatage conditionnel supprimé.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Formatage conditionnel supprimé.")
```

*(Des extraits de code supplémentaires pour Ruby, Go, Perl et Swift sont disponibles sur le [dépôt GitHub](https://github.com/aspose-cells-cloud).)*

## Voir aussi
- **Guide d’authentification** – [Authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Spécification OpenAPI** – Schéma détaillé de ce point de terminaison (s’ouvre dans un nouvel onglet)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">Spécification OpenAPI</a>`  
- **Vue d’ensemble du formatage conditionnel** – Découvrez comment créer, mettre à jour et lister les règles de formatage.  
- **SDK Aspose.Cells Cloud** – Liste complète des langues prises en charge sur le [dépôt GitHub](https://github.com/aspose-cells-cloud).  

---  

*Cette page suit le modèle standard de documentation de l’API Aspose.Cells Cloud, inclut une section Conditions préalables et respecte les meilleures pratiques en matière d’accessibilité et de référencement SEO.*
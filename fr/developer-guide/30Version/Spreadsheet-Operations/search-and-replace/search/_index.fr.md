---
title: "Rechercher du texte dans des fichiers Excel – API Aspose.Cells Cloud"
description: "Recherchez du texte spécifique dans des fichiers Excel (XLS, XLSX, XLSM, XLSB) et ODS à l’aide de l’API Aspose.Cells Cloud. Inclut les détails de la requête, des exemples cURL et SDK, ainsi que la gestion des erreurs."
keywords: "Aspose.Cells, Excel, recherche, API, REST"
type: docs
url: /fr/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Rechercher du texte dans des fichiers Excel – API Aspose.Cells Cloud

## Vue d’ensemble
Aspose.Cells Cloud fournit un endpoint **POST** permettant de rechercher une chaîne de texte donnée dans des classeurs Excel (XLS, XLSX, XLSM, XLSB) et des fichiers de feuille de calcul OpenDocument (ODS). L’API renvoie chaque cellule contenant la chaîne recherchée, accompagnée d’un lien vers la feuille de calcul où la correspondance a été trouvée.

> **Cas d’usage**  
> - Valider qu’une valeur particulière existe dans un rapport avant de procéder à un traitement ultérieur.  
> - Développer rapidement un outil de « recherche et remplacement » qui répertorie d’abord toutes les occurrences.  
> - Générer un index de termes clés à travers un lot de feuilles de calcul.

---

## Conditions préalables
| Exigence | Détails |
|----------|---------|
| **Authentification** | Jeton JWT obtenu via le flux OAuth Aspose Cloud. Le jeton doit inclure la portée **Cells**. |
| **Formats pris en charge** | XLS, XLSX, XLSM, XLSB, ODS |
| **Taille maximale du fichier** | 150 Mo (compressé). Les fichiers plus volumineux génèrent une erreur **413 Payload Too Large**. |
| **En-têtes requis** | `Authorization: Bearer <jeton-jwt>`  <br> `Accept: application/json` |
| **Permissions** | Le jeton doit disposer de la permission *lecture* sur le stockage cible (si un stockage distant est utilisé) – cette condition n’est pas requise lorsque le fichier est envoyé en tant que `multipart/form-data`. |

*Conseil :* Utilisez l’endpoint **/connect/token** pour générer un jeton JWT. Consultez le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) pour plus de détails.

---

## Endpoint

| Élément | Valeur |
|---------|--------|
| **Méthode HTTP** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **Objectif** | Rechercher une chaîne de texte spécifiée dans un classeur Excel envoyé. |
| **Sécurité** | Jeton JWT (Bearer) – voir *Conditions préalables* ci-dessus. |

---

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## Paramètres de la requête

| Nom | Type | Emplacement | Obligatoire | Description |
|-----|------|-------------|-------------|-------------|
| `file` | **fichier** | `formData` (multipart) | **Oui** | Le fichier de feuille de calcul à uploader. |
| `text` | **chaîne** | Chaîne de requête | **Oui** | La chaîne de texte à rechercher. |
| `password` | **chaîne** | Chaîne de requête | Non | Mot de passe nécessaire pour ouvrir un classeur protégé. |
| `sheetname` | **chaîne** | Chaîne de requête | Non | Nom de la feuille de calcul dans laquelle limiter la recherche. Si omis, toutes les feuilles sont recherchées. |
| `checkExcelRestriction` | **booléen** | Chaîne de requête | Non (par défaut : `true`) | Lorsque `true`, l’API valide les restrictions spécifiques à Excel (par exemple, les cellules en lecture seule) avant la recherche. |

---

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton-jwt>" \
  -F "file=@InvoiceReport.xlsx"
```

*Remplacez `<jeton-jwt>` par un jeton valide et ajustez les paramètres de requête selon vos besoins.*

---

## Réponse réussie

**HTTP 200 – Recherche réussie ; la réponse contient les éléments de texte trouvés.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### Champs de la réponse

| Champ | Type | Description |
|-------|------|-------------|
| `Status` | chaîne | Statut global de la requête (`OK` en cas de succès). |
| `Code` | entier | Code d’état HTTP (200). |
| `TextItems.link` | objet | Lien hypermédia vers la ressource de collection. |
| `TextItems.TextItemList` | tableau | Liste des correspondances trouvées. Chaque élément contient : |
| `Text` | chaîne | La valeur de la cellule correspondant à la chaîne recherchée. |
| `link` | objet | Lien hypertexte vers la feuille de calcul où la correspondance a été trouvée (`Href` pointe vers `Workbook/worksheets/NomFeuille`). |

---

## Réponses d’erreur

| Code HTTP | Signification | Cause typique | Corps d’exemple |
|-----------|---------------|---------------|-----------------|
| **400** | Requête incorrecte | Paramètres requis manquants, type de fichier non pris en charge ou valeurs de requête invalides. | `{ "Status":"Error","Code":400,"Message":"Le paramètre de requête 'text' est obligatoire." }` |
| **401** | Non autorisé | Jeton JWT manquant ou invalide. | `{ "Status":"Error","Code":401,"Message":"Jeton d’accès invalide ou expiré." }` |
| **413** | Charge utile trop volumineuse | Le fichier envoyé dépasse la limite de 150 Mo. | `{ "Status":"Error","Code":413,"Message":"La taille du fichier dépasse la limite autorisée." }` |
| **500** | Erreur interne du serveur | Problème inattendu côté serveur. | `{ "Status":"Error","Code":500,"Message":"Une erreur inattendue s’est produite." }` |

---

## Exemples SDK

Ci-dessous figurent des extraits de code minimalisés pour l’opération **PostSearch**, utilisant les SDK officiels Aspose.Cells Cloud. Remplacez `VOTRE_JETON_JWT` et le chemin du fichier par vos propres valeurs.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "VOTRE_JETON_JWT",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("VOTRE_JETON_JWT");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // mot de passe
                "Sheet1",      // nomFeuille
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "VOTRE_JETON_JWT"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "VOTRE_JETON_JWT",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(Les SDK pour PHP, Ruby, Go et Perl sont disponibles dans le [dépôt GitHub Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).)*

---

## Remarques complémentaires

- **`checkExcelRestriction`** est `true` par défaut. Ne le définissez pas sur `false` sauf si vous êtes certain que le classeur ne contient pas de cellules protégées pouvant perturber la recherche.
- L’API renvoie des **liens hypertexte** (`Href`) pouvant être utilisés avec d’autres endpoints Aspose.Cells Cloud (par exemple, pour télécharger la feuille de calcul ou récupérer le formatage des cellules).
- Lors de la recherche dans de grands classeurs, envisagez de limiter la portée à l’aide du paramètre `sheetname` afin d’améliorer la rapidité de réponse.

---

## Liens connexes

- **Guide d’authentification** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **Spécification OpenAPI pour PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **SDK Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>
- **Limites de débit et quotas** – <https://docs.aspose.cloud/total/getting-started/limits/>
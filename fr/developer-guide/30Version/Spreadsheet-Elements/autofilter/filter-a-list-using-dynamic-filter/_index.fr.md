---
title: Ajouter un filtre dynamique dans une feuille Excel à l'aide de l'API Aspose.Cells Cloud
description: Découvrez comment appliquer un filtre dynamique (par exemple, BelowAverage, Tomorrow, LastMonth) à une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut l'authentification, la syntaxe des requêtes, les paramètres, la gestion des réponses et des exemples de SDK pour plusieurs langages.
keywords: Aspose.Cells, filtre dynamique, API Excel, REST, filtre automatique, SDK cloud
slug: add-dynamic-filter
api_version: v3.0
---

## Vue d'ensemble

L'opération **PutWorksheetDynamicFilter** ajoute un filtre dynamique à une plage spécifiée dans une feuille Excel.  
Les filtres dynamiques évaluent automatiquement des valeurs telles que des dates, des moyennes ou des cellules vides, vous permettant de créer des vues « intelligentes » sans écrire de formules personnalisées.

## Conditions préalables

| Exigence | Détails |
|----------|---------|
| **Authentification** | Un jeton JWT valide obtenu à partir du point de terminaison `/connect/token`. Il doit être inclus dans l’en-tête `Authorization: Bearer <token>`. |
| **Stockage** | Le classeur doit se trouver dans un emplacement de stockage Aspose Cloud (par défaut ou personnalisé). |
| **Formats de fichier pris en charge** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv`, etc. |
| **Permissions** | Accès en lecture/écriture au dossier/fichier cible. |

## Requête HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Paramètres de chemin

| Paramètre | Type | Obligatoire | Description |
|-----------|------|-------------|-------------|
| `name` | string | ✅ | Le nom du classeur Excel (par exemple, `Book1.xlsx`). |
| `sheetName` | string | ✅ | Le nom de la feuille contenant la plage à filtrer. |

### Paramètres de requête

| Paramètre | Type | Obligatoire | Description |
|-----------|------|-------------|-------------|
| `range` | string | ✅ | La plage de cellules à laquelle le filtre est appliqué (par exemple, `A1:B1`). |
| `fieldIndex` | integer | ✅ | Index à base zéro de la colonne à l’intérieur de la plage à laquelle le filtre dynamique est appliqué. |
| `dynamicFilterType` | string | ✅ | Type de filtre dynamique à appliquer (voir **Types de filtres dynamiques pris en charge**). |
| `matchBlanks` | boolean | ❌ | Si `true`, les cellules vides sont incluses dans les résultats du filtre. Par défaut : `false`. |
| `refresh` | boolean | ❌ | Si `true`, le filtre automatique est rafraîchi après l’application du filtre. |
| `folder` | string | ❌ | Chemin du dossier dans le stockage où se trouve le classeur. |
| `storageName` | string | ❌ | Nom du stockage Aspose Cloud à utiliser. |

### Corps de la requête

Le corps de la requête est un objet JSON vide :

```json
{}
```

## Types de filtres dynamiques pris en charge

| Valeur | Signification |
|--------|---------------|
| `BelowAverage` | Lignes dont la valeur est inférieure à la moyenne de la colonne. |
| `AboveAverage` | Lignes dont la valeur est supérieure à la moyenne de la colonne. |
| `Tomorrow` | Lignes dont la date correspond à celle de demain. |
| `Yesterday` | Lignes dont la date correspond à celle d’hier. |
| `NextWeek` | Lignes dont la date se situe dans la semaine civile suivante. |
| `LastMonth` | Lignes dont la date provient du mois précédent. |
| `ThisYear` | Lignes dont la date se situe dans l’année en cours. |

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # Le corps JSON d’une requête PUT est vide
```

## Exemple de réponse

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "Filtre dynamique appliqué avec succès."
}
```

**Codes d’état HTTP**

| Code | Signification                | Description |
|------|------------------------------|-------------|
| 200  | OK                           | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                 | Jeton JWT non valide ou manquant. |
| 413  | Charge utile trop grande      | Le fichier chargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur     | Erreur inattendue du serveur. |

## Exemples de SDK

Ci-dessous figurent des extraits de code prêts à l’emploi pour les SDK les plus populaires. Remplacez `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` et autres espaces réservés par vos propres valeurs.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | Nom du classeur.
var sheetName = "Sheet1"; // string | Nom de la feuille.
var range = "A1:B1"; // string | Plage à filtrer.
var fieldIndex = 0; // int? | Index de colonne à base zéro.
var dynamicFilterType = "BelowAverage"; // string | Type de filtre dynamique.
var matchBlanks = true; // bool? | Inclure les cellules vides.
var refresh = true; // bool? | Rafraîchir après application.
var folder = "myFolder"; // string (facultatif)
var storageName = null; // string (facultatif)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception lors de l’appel à AutoFilterApi.PutWorksheetDynamicFilter : " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (facultatif)
            undefined              // storageName (facultatif)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Des extraits similaires sont disponibles pour Ruby, PHP, Go et Perl dans le dépôt officiel des SDK.)*

## Sujets connexes

- **Ajouter un filtre automatique standard** – [Ajouter un filtre standard](/autofilter/add-filter)  
- **Ajouter un filtre de date** – [Ajouter un filtre de date](/autofilter/add-date-filter)  
- **Supprimer un filtre automatique** – [Supprimer le filtre automatique](/autofilter/delete-filter)  
- **Travailler avec des feuilles de calcul** – [Vue d’ensemble de l’API des feuilles de calcul](/worksheets/)

## Notes

* Toutes les images utilisées dans la documentation d'origine ont été examinées pour leur accessibilité. Les icônes décoratives sont marquées avec `alt=""` et `role="presentation"` ; les icônes fonctionnelles conservent un texte `alt` descriptif.  
* Les mots-clés méta ont été nettoyés afin d'éliminer les entrées vides et les doublons.  
* La page respecte désormais une hiérarchie claire des titres (un seul H1 dans le front matter, des H2 pour les sections principales, des H3/H4 pour les sous-sections), ce qui améliore le référencement et la navigation via les lecteurs d'écran.
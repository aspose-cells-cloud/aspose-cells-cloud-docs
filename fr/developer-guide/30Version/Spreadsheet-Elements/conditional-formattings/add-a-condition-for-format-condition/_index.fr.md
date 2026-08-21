---
title: Ajouter une condition au formatage conditionnel
description: Découvrez comment ajouter une condition à un formatage conditionnel d'une feuille de calcul à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut l'URL du point de terminaison, les paramètres, l'authentification, un exemple cURL, des extraits de code SDK et la gestion des erreurs.
keywords: "Aspose.Cells Cloud, Formatage conditionnel, Ajouter une condition, API REST, Excel, Feuille de calcul"
type: docs
url: /fr/conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# Ajouter une condition au formatage conditionnel

Ajoutez une condition à une règle existante de formatage conditionnel dans une feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud (v3.0).

---

## Conditions préalables

| Exigence | Détails |
|----------|---------|
| **Authentification** | Un jeton d’accès JWT valide (Bearer) obtenu via le flux OAuth 2.0. |
| **Version de l’API** | v3.0 – l’URL du point de terminaison contient `/v3.0/`. |
| **Stockage** | Le classeur doit se trouver dans un emplacement de stockage accessible à Aspose.Cells Cloud (par défaut : `Default`). |
| **Permissions** | Autorisation de lecture/écriture sur le classeur cible. |
| **Formats pris en charge** | Tout format de classeur pris en charge par Aspose.Cells (par exemple, `.xlsx`, `.xls`, `.xlsm`). |

---

## Point de terminaison

**Méthode HTTP :** `PUT`  
**URL :**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Paramètre | Emplacement | Type | Obligatoire | Description |
|-----------|-------------|------|-------------|-------------|
| `name` | Chemin | string | **Oui** | Nom du fichier classeur (y compris l’extension). |
| `sheetName` | Chemin | string | **Oui** | Nom de la feuille de calcul contenant le formatage conditionnel. |
| `index` | Chemin | entier | **Oui** | Index de base zéro de la collection de formatage conditionnel à modifier. |
| `type` | Requête | string | **Oui** | Type de condition. Valeurs autorisées : `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Requête | string | **Oui** | Opérateur de la condition. Valeurs autorisées : `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`. |
| `formula1` | Requête | string | **Oui** | Première formule/valeur associée à la condition. |
| `formula2` | Requête | string | Non | Deuxième formule/valeur (nécessaire uniquement pour les opérateurs nécessitant deux valeurs, par exemple `Between`). |
| `folder` | Requête | string | Non | Dossier dans le stockage où se trouve le classeur. |
| `storageName` | Requête | string | Non | Nom du service de stockage. |

> **Remarque :** Tous les paramètres de chemin (`name`, `sheetName`, `index`) ainsi que les paramètres de requête `type`, `operatorType`, `formula1` sont obligatoires. `formula2`, `folder` et `storageName` sont facultatifs.

---

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*Remplacez `<jwt_token>` par un jeton d’accès valide et ajustez les valeurs de `name`, `sheetName`, `index` et des paramètres de requête selon vos besoins.*

---

## Réponse réussie

```json
{
  "Code": "200",
  "Status": "OK"
}
```

La réponse indique que la condition a été ajoutée avec succès. L’opération renvoie un objet générique `CellsCloudResponse` contenant le code de statut HTTP et un court message d’état.

---

## Réponses d’erreur

| Code HTTP | Raison | Corps d’exemple |
|-----------|--------|-----------------|
| **400** | Mauvaise requête – paramètres manquants ou invalides. | `{ "Code":"400", "Message":"Valeur de paramètre non valide." }` |
| **401** | Non autorisé – jeton JWT manquant ou invalide. | `{ "Code":"401", "Message":"Le jeton d’accès est manquant ou invalide." }` |
| **404** | Introuvable – le classeur, la feuille de calcul ou l’index de formatage conditionnel n’existe pas. | `{ "Code":"404", "Message":"Fichier introuvable." }` |
| **500** | Erreur interne du serveur – défaillance inattendue du serveur. | `{ "Code":"500", "Message":"Une erreur inattendue s’est produite." }` |

---

## Notes et pièges courants

* **Codage des paramètres** – Échappez les caractères spéciaux dans `formula1`/`formula2` dans l’URL (par exemple, les espaces → `%20`).  
* **Compatibilité des opérateurs** – Certains opérateurs (par exemple, `Between`) nécessitent à la fois `formula1` et `formula2`. Omettez `formula2` pour les opérateurs n’exigeant qu’une seule valeur.  
* **Index du formatage conditionnel** – L’index est de base zéro. Utilisez le point de terminaison **Obtenir les formatages conditionnels** pour récupérer l’index correct si vous êtes incertain.  
* **Dossier de stockage** – Si le classeur se trouve dans un dossier non par défaut, fournissez le paramètre de requête `folder` ; sinon, l’API suppose le dossier racine.  
* **Limitation du débit** – Aspose.Cells Cloud applique des limites de requêtes par compte. Si vous recevez une réponse 429, attendez un court instant avant de réessayer.

---

## Exemples de SDK

Ci-dessous figurent des extraits prêts à l’emploi pour les SDK les plus populaires. Remplacez les valeurs génériques (`YOUR_FILE`, `YOUR_SHEET`, etc.) par vos propres données.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // facultatif
        string storageName = null;     // facultatif

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Statut : {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception lors de l’appel à ConditionalFormattingsApi.PutWorksheetFormatConditionCondition : " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Réponse : " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Statut :', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Statut : #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception lors de l’appel à ConditionalFormattingsApi->put_worksheet_format_condition_condition : #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Statut : " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception lors de l’appel à ConditionalFormattingsApi->put_worksheet_format_condition_condition : $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Erreur : %v\n", err)
        return
    }
    fmt.Printf("Statut : %s\n", resp.Status)
}
```

> **SDK manquants** – Si le langage dont vous avez besoin n’est pas listé ici, reportez-vous à la **Référence API générique** et construisez manuellement la requête HTTP.

---

## Voir aussi

- **[Obtenir les formatages conditionnels](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – Récupérez la liste des règles de formatage conditionnel pour une feuille de calcul.  
- **[Supprimer un formatage conditionnel](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – Supprimez une règle de formatage conditionnel existante.  
- **[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – Définition complète, lisible par machine, de cette opération.  

---
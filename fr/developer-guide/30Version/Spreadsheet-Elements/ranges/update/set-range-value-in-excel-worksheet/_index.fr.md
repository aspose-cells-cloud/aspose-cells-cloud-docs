---
title: "Définir une valeur de plage dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Définir des valeurs"
type: docs
url: /fr/ranges/update/values/
aliases: [  /fr/set-range-value-in-excel-worksheet/ ]
keywords: "Aspose.Cells, API Excel, définir la valeur d'une plage, API REST, SDK cloud, mise à jour de la feuille de calcul"
description: "Découvrez comment définir la valeur d'une cellule ou d'une plage dans un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud (version 3.0). Inclut l’URL du point de terminaison, les paramètres, un exemple cURL, des exemples de code SDK et la gestion des erreurs."
weight: 72
ArticleTitle: "Définir une valeur de plage dans une feuille de calcul Excel – API Aspose.Cells Cloud"
---

Utilisez cette API REST pour définir une valeur dans la plage spécifiée. Lorsque cela est approprié, la valeur est convertie vers un autre type de données et le format numérique de la cellule est réinitialisé.

**Conditions préalables**  
- Un compte Aspose Cloud valide.  
- Un jeton JWT incluant le scope `Cells.ReadWrite`.  
- Le classeur doit déjà avoir été téléchargé dans l’emplacement de stockage cible.

## API PostWorksheetCellsRangeValue

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type    | Emplacement | Description                                              |
|------------------|---------|-------------|----------------------------------------------------------|
| name             | string  | path        | Nom du classeur                                          |
| sheetName        | string  | path        | Nom de la feuille de calcul                              |
| value            | string  | query       | Valeur d'entrée                                          |
| range            | object  | body        | Objet plage dans la feuille de calcul                    |
| isConverted      | boolean | query       | Indique si la valeur d'entrée doit être convertie       |
| setStyle         | boolean | query       | Indique s’il faut appliquer un style aux cellules cibles |
| folder           | string  | query       | Dossier du classeur                                      |
| storageName      | string  | query       | Nom du stockage                                         |

**Exemple d’objet `range`** pouvant être envoyé dans le corps de la requête :

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL. **Incluez un jeton JWT valide dans l’en-tête `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Schéma de réponse**

| Champ   | Type    | Description                                             |
|---------|---------|---------------------------------------------------------|
| Code    | integer | Code de statut HTTP de l'opération.                    |
| Status  | string  | Brève description du résultat (par exemple, « OK »).    |
| Message | string  | Message d’erreur détaillé en cas d’échec de la requête (facultatif). |
| Result  | object  | Données supplémentaires renvoyées pour les appels réussis (facultatif). |

**Codes de statut HTTP possibles**

- **200 OK** – La valeur de la plage a été définie avec succès.  
- **400 Bad Request** – Paramètres invalides ou corps de requête mal formé.  
- **401 Unauthorized** – Jeton JWT manquant ou invalide.  
- **403 Forbidden** – Autorisations insuffisantes pour l’opération demandée.  
- **404 Not Found** – Le classeur, la feuille de calcul ou la plage spécifiée n’existe pas.  
- **500 Internal Server Error** – Erreur serveur inattendue.

*Exemple de réponse d’erreur pour un code 400 Bad Request :*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "L’objet 'range' ne contient pas les champs obligatoires."
}
```

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}
---
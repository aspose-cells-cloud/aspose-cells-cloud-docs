---
title: "Ajouter un champ croisé à un tableau croisé dynamique"
second_title: "Document"
linktitle: "Ajouter un champ croisé"
type: docs
url: /fr/pivot-tables/add-pivot-field/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, tableau croisé dynamique, ajouter un champ croisé, API REST, SDK"
description: "Ajouter un champ croisé à un tableau croisé dynamique existant à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails de la requête, un exemple cURL et des extraits de code SDK."
weight: 40
ArticleTitle: "Ajouter un champ croisé à un tableau croisé dynamique – Documentation Aspose.Cells Cloud"
---

Cette API REST **ajoute** un champ croisé à un tableau croisé dynamique existant.

> **Prérequis :** Pour appeler ce point de terminaison, vous devez inclure un jeton d’authentification JWT valide dans l’en-tête `Authorization` et vous assurer que le classeur est stocké dans le dossier spécifié ou dans le stockage par défaut.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                       |
|------------------|---------|-------------|-------------------------------------------------------------------|
| name             | string  | path        | Nom du document.                                                  |
| sheetName        | string  | path        | Nom de la feuille de calcul.                                      |
| pivotTableIndex  | integer | path        | Index du tableau croisé dynamique.                                |
| pivotFieldType   | string  | query       | Type de zone des champs (par exemple, Row, Column).               |
| request          | object  | body        | DTO contenant les index des champs à ajouter.                     |
| needReCalculate  | boolean | query       | Définir sur **true** pour recalculer le tableau croisé dynamique après l'opération. |
| folder           | string  | query       | Dossier dans lequel le document est stocké.                       |
| storageName      | string  | query       | Nom du stockage.                                                  |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler les services web Aspose.Cells. L’exemple ci-dessous montre comment ajouter un champ croisé à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

La réponse en cas de succès renvoie un objet JSON contenant les champs `Code` et `Status`. Exemple de schéma :

```json
{
  "Code": 0,        // entier indiquant le code de statut HTTP
  "Status": "OK"    // message texte
}
```

Les réponses d’erreur possibles incluent **400 Bad Request** pour les paramètres manquants, **401 Unauthorized** si le jeton est invalide, et **500 Internal Server Error** pour les problèmes côté serveur.

## Famille de SDK Cloud

Utiliser un SDK est la méthode la plus rapide pour intégrer cette fonctionnalité. Les SDK gèrent les détails de bas niveau, vous permettant ainsi de vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**Voir aussi :**  
- [Ajouter un tableau croisé dynamique](https://docs.aspose.cloud/cells/pivot-tables/add-pivot-table/)  
- [Supprimer un champ croisé](https://docs.aspose.cloud/cells/pivot-tables/delete-pivot-field/)
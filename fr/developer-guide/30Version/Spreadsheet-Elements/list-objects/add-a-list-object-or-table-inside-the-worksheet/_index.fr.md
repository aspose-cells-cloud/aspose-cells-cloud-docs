---
title: "Ajouter un objet liste (tableau) à une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ajouter"
type: docs
url: /fr/list-objects/add/
aliases: [  /fr/add-a-list-object-or-table-inside-the-worksheet/ , /fr/tables/add/ ]
keywords: "Aspose.Cells Cloud, API Excel, objet liste, tableau, API REST, feuille de calcul"
description: "Découvrez comment ajouter un objet liste (tableau Excel) à une feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint, les paramètres, les étapes d’authentification, un exemple cURL et des exemples de code SDK."
weight: 10
ArticleTitle: "Ajouter un objet liste (tableau) à une feuille de calcul Excel – Documentation Aspose.Cells Cloud"
---

Cette API REST ajoute un **objet liste (tableau)** à une feuille de calcul Excel.

Avant d'utiliser cet endpoint, assurez-vous d'avoir un jeton JWT valide, que le classeur soit stocké dans un stockage cloud pris en charge et que la feuille de calcul existe.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                           |
| ---------------- | ------- | ----------- | --------------------------------------------------------------------- |
| **name**         | string  | path        | Nom du fichier du classeur.                                           |
| **sheetName**    | string  | path        | Nom de la feuille de calcul.                                          |
| **startRow**     | integer | query       | Index de base zéro de la première ligne de la plage de table.        |
| **startColumn**  | integer | query       | Index de base zéro de la première colonne de la plage de table.      |
| **endRow**       | integer | query       | Index de base zéro de la dernière ligne de la plage de table.        |
| **endColumn**    | integer | query       | Index de base zéro de la dernière colonne de la plage de table.      |
| **hasHeaders**   | boolean | query       | `true` si la première ligne contient des en-têtes de colonne ; sinon `false`. |
| **listObject**   | object  | body        | Définition de l'objet liste (voir **Schéma du corps de la requête**). |
| **folder**       | string  | query       | Dossier contenant le classeur.                                        |
| **storageName**  | string  | query       | Nom du stockage.                                                      |

### Schéma du corps de la requête

L'objet **listObject** décrit le tableau qui sera créé. Seules les propriétés les plus courantes sont affichées ; reportez-vous à la spécification OpenAPI pour la liste complète.

```json
{
  "displayName": "MonTableau",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "displayName": "MonTableau",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### Exemple de réponse

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Codes d’erreur

| Statut HTTP | Raison             | Description                                                |
| ----------- | ------------------ | ---------------------------------------------------------- |
| **400**     | Demande incorrecte | Paramètres de plage invalides ou corps JSON mal formé.    |
| **401**     | Non autorisé       | Jeton JWT manquant ou expiré.                              |
| **404**     | Non trouvé         | Le classeur ou la feuille de calcul spécifié(s) n'existent pas. |
| **500**     | Erreur interne du serveur | Échec inattendu côté serveur.                          |

**Exemple de réponse 400**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Paramètres de plage invalides."
}
```

**Exemple de réponse 401**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Le jeton d'authentification est manquant ou expiré."
}
```

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) fournit le contrat complet pour cette opération.

## Famille de SDK Cloud

L'utilisation d'un SDK est le moyen optimal d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
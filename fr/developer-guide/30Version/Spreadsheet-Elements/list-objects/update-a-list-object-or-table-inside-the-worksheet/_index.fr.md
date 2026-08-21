---
title: "Mettre à jour un objet liste dans une feuille de calcul Excel"
ArticleTitle: "Mettre à jour un objet liste dans une feuille de calcul Excel – Documentation de l’API Aspose.Cells Cloud"
second_title: "Document"
linktype: "update"
type: docs
url: /fr/list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, Mettre à jour un tableau, API Excel, REST, SDK cloud, mise à jour d’un objet liste, feuille de calcul Excel, tableau"
description: "Découvrez comment mettre à jour un tableau Excel à l’aide de l’API Aspose.Cells Cloud (v3.0). Inclut l’URL du point de terminaison, les paramètres, des exemples cURL, les codes d’erreur et des exemples de SDK."
weight: 20
---

Cet API REST permet de mettre à jour les propriétés d’un **objet liste** (tableau) dans une feuille de calcul Excel.

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Schéma du corps de la demande

L’objet DTO `listObject` contient les champs suivants. Seuls les champs que vous souhaitez modifier doivent être présents dans le corps de la demande.

| Champ                                           | Type               | Obligatoire | Description                                                                |
| ----------------------------------------------- | ------------------ | ----------- | -------------------------------------------------------------------------- |
| **DisplayName**                                 | string             | facultatif  | Nom affiché du tableau.                                                    |
| **StartRow** / **StartColumn**                  | integer            | facultatif  | Indice de la première ligne/colonne du tableau (indexation à partir de 0). |
| **EndRow** / **EndColumn**                      | integer            | facultatif  | Indice de la dernière ligne/colonne du tableau (indexation à partir de 0). |
| **Range**                                       | string             | facultatif  | Adresse au format A1 définissant la plage du tableau (par ex., `A1:D10`).  |
| **ShowHeaderRow**                               | boolean            | facultatif  | `true` pour afficher la ligne d’en‑tête.                                   |
| **ShowTotals**                                  | boolean            | facultatif  | `true` pour afficher la ligne des totaux.                                  |
| **TableStyleName**                              | string             | facultatif  | Nom du style de tableau intégré à appliquer.                               |
| **TableStyleType**                              | string             | facultatif  | Type de style (`TableStyleLight`, `TableStyleMedium`, etc.).               |
| **ListColumns**                                 | tableau d’objets   | facultatif  | Collection de définitions de colonnes (`Name`, `TotalsCalculation`).      |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | objet              | facultatif  | Options avancées de style et de filtrage (voir le DTO complet dans la spécification OpenAPI). |

### Exemple minimal de charge utile

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **Paramètres de la demande**

| Nom du paramètre    | Type    | Emplacement | Description                              |
| ------------------- | ------- | ----------- | ---------------------------------------- |
| **name**            | string  | chemin      | Nom du document.                         |
| **sheetName**       | string  | chemin      | Nom de la feuille de calcul.             |
| **listObjectIndex** | integer | chemin      | Index de l’objet liste à mettre à jour.  |
| **listObject**      | objet   | corps       | Objet DTO `ListObject` dans le corps de la demande. |
| **folder**          | string  | requête     | Dossier contenant le document.           |
| **storageName**     | string  | requête     | Nom du stockage.                         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Demande

{{< tabs tabTotal="2" tabID="11" tabName11="Demande" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Réponse

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La réponse en cas de succès inclut les champs suivants :

| Champ                     | Type   | Description                                                  |
| ------------------------- | ------ | ------------------------------------------------------------ |
| Code                      | integer| Code de statut HTTP (200 en cas de succès).                 |
| Status                    | string | Description textuelle du statut.                             |
| UpdatedObject *(facultatif)* | objet | Représentation de l’objet `ListObject` mis à jour, contenant les propriétés modifiées. |

{{< /tab >}}

{{< /tabs >}}

## Réponses d’erreur

| Code HTTP | Description                                                                   | Exemple de charge utile                               |
| --------- | ----------------------------------------------------------------------------- | ----------------------------------------------------- |
| **400**   | Demande incorrecte – champs obligatoires manquants ou JSON mal formé.        | `{ "Code": 400, "Message": "Invalid request body." }` |
| **401**   | Non autorisé – jeton JWT manquant ou invalide.                                | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Introuvable – le classeur, la feuille de calcul ou l’objet liste spécifié n’existe pas. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**   | Erreur interne du serveur – condition inattendue côté serveur.                | `{ "Code": 500, "Message": "Server error." }`         |

## FAQ

<details>  
<summary>Comment mettre à jour un objet liste à l’aide de l’API Aspose.Cells Cloud ?</summary>

Utilisez le point de terminaison `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Incluez un corps JSON contenant les propriétés que vous souhaitez modifier (par ex., `DisplayName`, `ShowHeaderRow`). Authentifiez-vous à l’aide d’un jeton JWT dans l’en‑tête `Authorization`.

</details>

<details>  
<summary>Quelle réponse reçois‑je après une mise à jour réussie ?</summary>

Un objet JSON contenant `Code : 200` et `Status : "OK"` est renvoyé. En cas d’erreur, la réponse contient le code HTTP approprié ainsi qu’un objet `Error` décrivant le problème.

</details>

<details>  
<summary>Puis‑je mettre à jour uniquement un sous‑ensemble des propriétés de l’objet liste ?</summary>

Oui. Incluez uniquement les champs que vous souhaitez modifier dans le corps de la demande ; tous les champs omis restent inchangés.

</details>

## Documentation connexe

- [Ajouter un objet liste](https://docs.aspose.cloud/cells/list-objects/add/)
- [Obtenir un objet liste](https://docs.aspose.cloud/cells/list-objects/get/)
- [Supprimer un objet liste](https://docs.aspose.cloud/cells/list-objects/delete/)

## Famille de SDK cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
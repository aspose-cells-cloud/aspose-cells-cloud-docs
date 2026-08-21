---
title: "Aspose.Cells Cloud API – Fusion de plages de cellules"
second_title: "Document"
linktitle: "Fusionner"
type: docs
url: /fr/ranges/merge/
aliases: [  /fr/combines-a-range-of-cells-into-a-single-cell/ ]
keywords: "Aspose.Cells, fusionner des cellules, API Excel, REST, SDK cloud"
description: "Fusionner une plage de cellules en une seule cellule à l’aide de l’API REST Aspose.Cells Cloud. Découvrez le format de la requête, les paramètres et les exemples de SDK pour C#, Java, Python, etc."
weight: 20
---

Cet API REST permet de fusionner une plage de cellules en une seule cellule sur une feuille Excel.

**Vue d’ensemble** – La fusion d’une plage combine les cellules sélectionnées en une seule cellule, en conservant la valeur de la cellule en haut à gauche et en supprimant les autres. Utilisez cette opération lorsque vous devez créer un en‑tête couvrant plusieurs colonnes ou lignes, ou lorsque vous souhaitez simplifier la mise en page d’une feuille.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                    |
| ---------------- | ------ | ----------- | ---------------------------------------------- |
| **name**         | string | path        | Nom du classeur.                               |
| **sheetName**    | string | path        | Nom de la feuille de calcul.                   |
| **range**        | object | body        | Objet plage spécifiant les cellules à fusionner. |
| **folder**       | string | query       | Dossier dans lequel le classeur est stocké.    |
| **storageName**  | string | query       | Nom du stockage.                               |

#### Schéma du corps de la requête

L’objet **Range** doit contenir les champs suivants (les autres sont facultatifs) :

| Propriété       | Type    | Obligatoire | Description                                           |
| --------------- | ------- | ----------- | ----------------------------------------------------- |
| **FirstRow**    | integer | Oui         | Index de ligne (à partir de 0) de la première ligne de la plage. |
| **FirstColumn** | integer | Oui         | Index de colonne (à partir de 0) de la première colonne de la plage. |
| **RowCount**    | integer | Oui         | Nombre de lignes à inclure dans la plage.             |
| **ColumnCount** | integer | Oui         | Nombre de colonnes à inclure dans la plage.           |
| **Name**        | string  | Non         | Nom facultatif pour la plage.                         |
| **RefersTo**    | string  | Non         | Formule à laquelle la plage fait référence.            |
| **Worksheet**   | string  | Non         | Nom de la feuille de calcul (si différent du paramètre de chemin). |
| **RowHeight**   | number  | Non         | Hauteur des lignes dans la plage (en pixels).         |
| **ColumnWidth** | number  | Non         | Largeur des colonnes dans la plage (en pixels).       |

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci‑dessous montre comment effectuer un appel à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
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

#### Détails de la réponse

| Statut HTTP                   | Description                                              | Exemple JSON                                           |
| ----------------------------- | -------------------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | La plage a été fusionnée avec succès.                    | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | Paramètres de plage non valides (par ex., indices hors limites). | `{ "Code": 400, "Message": "Plage non valide." }`         |
| **401 Unauthorized**          | Jeton JWT manquant ou invalide.                          | `{ "Code": 401, "Message": "Échec de l’authentification." }` |
| **404 Not Found**             | Classeur ou feuille de calcul introuvable.              | `{ "Code": 404, "Message": "Ressource introuvable." }`    |
| **500 Internal Server Error** | Erreur interne inattendue du serveur.                   | `{ "Code": 500, "Message": "Erreur interne du serveur." }` |

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau, ce qui vous permet de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci‑dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
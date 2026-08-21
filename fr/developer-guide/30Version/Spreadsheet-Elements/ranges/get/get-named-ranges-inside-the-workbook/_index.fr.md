---
title: "Obtenir des plages nommées dans un classeur Excel"
second_title: "Document"
linktitle: "Nom"
type: docs
url: /fr/ranges/get/name/
aliases: [  /fr/get-named-ranges-inside-the-workbook/ ]
keywords: "plages nommées, Excel, Aspose.Cells, API REST dans le cloud, feuilles de calcul"
description: "Récupérer des plages nommées à partir d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails de la requête, des exemples de commandes cURL et des exemples de SDK pour plusieurs langages de programmation."
ArticleTitle: "Obtenir des plages nommées dans un classeur Excel – Aspose.Cells Cloud API"
weight: 10
---

Cette API REST renvoie des informations sur les plages nommées définies dans les feuilles de calcul.

**Contexte** – Une *plage nommée* est un identifiant défini par l'utilisateur qui fait référence à une cellule spécifique ou à un bloc de cellules dans une feuille de calcul. Les plages nommées simplifient la création de formules, améliorent la lisibilité et permettent un accès programmatique aux zones fréquemment utilisées d’un classeur.

**Conditions préalables** – L’accès à l’API REST Aspose.Cells Cloud nécessite un jeton d’accès JWT valide. Obtenez ce jeton en vous authentifiant à l’aide de votre identifiant client Aspose Cloud et de votre secret client via le point de terminaison de jeton OAuth 2.0. Incluez le jeton dans l’en-tête `Authorization: Bearer <jeton JWT>` de chaque requête.

## API GetNamedRanges

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement     | Description                                  |
| ---------------- | ------ | --------------- | -------------------------------------------- |
| name             | string | Chemin          | Le nom du fichier Excel.                     |
| folder           | string | Chaîne de requête | Le dossier contenant le document.            |
| storageName      | string | Chaîne de requête | Le nom du stockage où réside le document.    |

**Codes d’état HTTP**

| Code | Signification                | Description                                              |
|------|------------------------------|----------------------------------------------------------|
| 200  | OK                           | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                 | Jeton JWT invalide ou manquant.                          |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.      |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue.                               |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) définit une interface de programmation accessible publiquement qui permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler les services web Aspose.Cells. L’exemple ci-dessous montre comment récupérer les plages nommées à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Modèle de réponse**

| Champ            | Type    | Description                                                |
|------------------|---------|------------------------------------------------------------|
| `ColumnCount`    | entier  | Nombre de colonnes dans la plage.                          |
| `ColumnWidth`    | nombre  | Largeur de chaque colonne (en points).                      |
| `FirstColumn`    | entier  | Index de base zéro de la première colonne dans la plage.   |
| `FirstRow`       | entier  | Index de base zéro de la première ligne dans la plage.     |
| `Name`           | chaîne  | Nom défini par l’utilisateur de la plage.                  |
| `RefersTo`       | chaîne  | Une formule définissant la référence de cellule (par exemple, `=Sheet1!$B$10:$H$10`). |
| `RowCount`       | entier  | Nombre de lignes dans la plage.                            |
| `RowHeight`      | nombre  | Hauteur de chaque ligne (en points).                        |
| `Worksheet`      | chaîne  | Nom de la feuille de calcul contenant la plage.            |

## Famille de SDK dans le cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour intégrer cette fonctionnalité. Les SDK gèrent les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}
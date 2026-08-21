---
title: "Modifier les largeurs de colonnes dans une plage"
ArticleTitle: "Modifier les largeurs de colonnes dans une plage – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Largeur de colonne"
type: docs
url: /fr/ranges/update/column-width/
aliases: [  /fr/change-widths-of-columns-inside-the-range/ ]
keywords: "Aspose.Cells, largeur de colonne, API REST, Excel, SDK, plage, cloud"
description: "Découvrez comment modifier les largeurs de colonnes dans une plage à l’aide de l’API REST Aspose.Cells Cloud ou des SDK (C#, Java, Python, etc.). Inclut cURL, détails sur la requête/réponse et étapes d’authentification."
weight: 74
---

Cet API REST définit la largeur de colonne d'une plage.

## Sécurité et authentification
Les API REST Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**Prérequis** – Avant d’appeler le point de terminaison, vous devez :

1. Créer un compte Aspose Cloud et obtenir un *ID client* et un *secret client*.  
2. Demander un jeton JWT en appelant le point de terminaison OAuth (`/connect/token`). Le jeton est retourné dans le champ `access_token`.  
3. Télécharger le classeur cible vers votre stockage Aspose Cloud (ou vous assurer qu’il existe déjà dans le dossier spécifié).  

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| name             | string | path        | Nom du fichier du classeur |
| sheetName        | string | path        | Nom de la feuille de calcul |
| value            | number | query       | Valeur souhaitée pour la largeur de colonne |
| range            | object | body        | Objet plage définissant les cellules cibles |
| folder           | string | query       | Chemin du dossier où le classeur est stocké |
| storageName      | string | query       | Nom du service de stockage |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

<h3 id="request">Requête</h3>

```bash
# Appeler le point de terminaison columnWidth pour le classeur *test.xlsx*,
# feuille *Sheet1*, en définissant la largeur des colonnes sélectionnées à 20 points.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">Réponse</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Réponses d’erreur possibles*  

| Code HTTP | Description                               |
|-----------|-------------------------------------------|
| 400       | Requête incorrecte – JSON ou paramètres invalides |
| 401       | Non autorisé – jeton manquant ou invalide |
| 404       | Non trouvé – classeur ou feuille de calcul absent |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ

**Q :** *Quel point de terminaison dois-je appeler pour définir la largeur de colonne d’une plage dans un classeur Excel ?*  
**R :** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth`, où `{name}` est le nom du fichier du classeur et `{sheetName}` est le nom de la feuille de calcul cible.

**Q :** *Comment authentifier la requête lors de l'utilisation de l'API de largeur de colonne ?*  
**R :** Inclure l’en-tête `Authorization: Bearer <jeton jwt>`. Obtenez le jeton JWT via le flux OAuth Aspose Cloud (`/connect/token`) en utilisant votre ID client et votre secret client.

**Q :** *Quel corps JSON dois-je envoyer pour modifier la largeur des colonnes A à C à 25 points ?*  
**R :**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

Ajoutez le paramètre de requête `value=25` à l’URL de la requête.
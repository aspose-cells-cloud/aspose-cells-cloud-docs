---
title: "Ajouter un filtre d'icônes à une feuille de calcul Excel"
second_title: "Document"
linktype: "Ajouter un filtre d'icônes"
type: docs
url: /fr/autofilter/add-icon-filter/
aliases: [/ajouter-un-filtre-d-icônes/,/fr/autofilter/add-icon-filter/]
keywords: "Aspose.Cells Cloud, Excel, Filtre d'icônes, Filtre automatique, API REST"
description: "Découvrez comment ajouter un filtre d'icônes à une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud, avec les détails de la requête, un exemple cURL, des extraits de code SDK et la gestion des erreurs."
weight: 65
ArticleTitle: "Ajouter un filtre d'icônes à une feuille de calcul Excel – Documentation Aspose.Cells Cloud"
---

## API REST

Cette API REST ajoute un **filtre d'icônes** à une feuille de calcul Excel à l'aide de **l'API REST Aspose.Cells Cloud**.

**Contexte :** Un filtre d'icônes applique un jeu d'icônes visuelles aux cellules en fonction de leurs valeurs, permettant une analyse rapide des tendances des données. Les cas d'utilisation courants comprennent la mise en surbrillance des indicateurs de performance, des indicateurs d'état ou la catégorisation des valeurs à l'aide d'icônes de signalisation routière (feux tricolores) directement dans les feuilles de calcul Excel.

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

### Paramètres de la requête :

| Nom du paramètre | Type    | Emplacement | Description |
|------------------|---------|-------------|-------------|
| name             | string  | Path        | Nom du classeur. |
| sheetName        | string  | Path        | Nom de la feuille de calcul. |
| range            | string  | Query       | Plage de cellules (par exemple, `A1:B1`) à laquelle le filtre sera appliqué. |
| fieldIndex       | integer | Query       | Index à base zéro de la colonne ciblée par le filtre. |
| iconSetType      | string  | Query       | Jeu d'icônes à utiliser. Valeurs autorisées : `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId           | integer | Query       | Identifiant de l'icône spécifique au sein du jeu d'icônes sélectionné. |
| matchBlanks      | boolean | Query       | Indique si les cellules vides doivent être incluses (`true` ou `false`). |
| refresh          | boolean | Query       | Indique si le filtre doit être actualisé après application (`true` ou `false`). |
| folder           | string  | Query       | Dossier contenant le classeur original. |
| storageName      | string  | Query       | Nom du stockage où réside le classeur. |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification                | Description |
|------|------------------------------|-------------|
| 200  | OK                           | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Requête incorrecte           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                 | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande      | Fichier téléchargé dépassant la limite de taille. |
| 500  | Erreur interne du serveur     | Erreur inattendue sur le serveur. |

## Comment utiliser l'API PutWorksheetIconFilter à l'aide des SDK

### Spécification de l'API PutWorksheetIconFilter

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) définit une interface de programmation accessible publiquement et permet d'effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l'outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L'exemple ci-dessous montre comment effectuer un appel à l'API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codes de statut de réponse possibles :

| Code | Description |
|------|-------------|
| 200 | Filtre appliqué avec succès. |
| 400 | Requête incorrecte – paramètres manquants ou non valides. |
| 401 | Non autorisé – jeton d'authentification invalide ou manquant. |
| 404 | Classeur, feuille de calcul ou plage spécifiée introuvable. |
| 500 | Erreur interne du serveur. |
{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Pour d'autres fonctionnalités de filtre automatique, consultez la documentation sur **[Ajouter un filtre de couleur](/fr/autofilter/add-color-filter/)**, **[Ajouter un filtre de date](/fr/autofilter/add-date-filter/)** et **[Effacer le filtre automatique](/fr/autofilter/clear-autofilter/)**.
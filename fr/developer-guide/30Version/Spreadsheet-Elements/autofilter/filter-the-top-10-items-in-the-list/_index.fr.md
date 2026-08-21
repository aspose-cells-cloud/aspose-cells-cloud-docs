---
title: "Ajouter un filtre Top 10 à une feuille de calcul Excel (Aspose.Cells Cloud)"
ArticleTitle: "Ajouter un filtre Top 10 à une feuille de calcul Excel – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Ajouter un filtre Top 10"
type: docs
url: /autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, filtre Top 10, API Excel"
description: "Découvrez comment appliquer un filtre AutoFilter Top 10 à une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint, les paramètres, un exemple HTTPS cURL, les détails d’authentification, la gestion des erreurs et des extraits de code SDK pour C#, Java, Python, et plus encore."
weight: 65
---

Cet API REST permet de filtrer les **Top 10** éléments d’une liste.

> **Prérequis**  
> • Obtenir un jeton JWT valide à l’aide de l’authentification Aspose.Cells Cloud.  
> • Téléverser le classeur Excel vers votre stockage Aspose Cloud (ou spécifier le stockage/dossier dans lequel il se trouve).  
> • Connaître le nom de la feuille de calcul et la plage de cellules à filtrer.

## API PutWorksheetFilterTop10

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Obligatoire | Valeur par défaut | Description                                                                 |
| ---------------- | ------- | ----------- | ----------- | ---------------- | --------------------------------------------------------------------------- |
| **name**         | string  | chemin      | Oui         | —                | Le nom du fichier Excel.                                                    |
| **sheetName**    | string  | chemin      | Oui         | —                | Le nom de la feuille de calcul contenant les données.                       |
| **range**        | string  | requête     | Oui         | —                | La plage de cellules à laquelle le filtre est appliqué (par ex., `A1:B10`). |
| **fieldIndex**   | integer | requête     | Oui         | —                | Index de colonne à zéro de départ sur lequel le filtre est appliqué.        |
| **isTop**        | boolean | requête     | Oui         | `true`           | `true` pour filtrer les éléments les plus élevés ; `false` pour les plus faibles. |
| **isPercent**    | boolean | requête     | Non         | `false`          | `true` pour traiter `itemCount` comme un pourcentage ; `false` pour un nombre absolu. |
| **itemCount**    | integer | requête     | Non         | `10`             | Nombre d’éléments à inclure dans le filtre.                                 |
| **matchBlanks**  | boolean | requête     | Non         | `false`          | `true` pour inclure les cellules vides dans les résultats du filtre.        |
| **refresh**      | boolean | requête     | Non         | `false`          | `true` pour actualiser le filtre après l’avoir appliqué.                    |
| **folder**       | string  | requête     | Non         | —                | Le dossier, dans le stockage, où se trouve le fichier Excel.                |
| **storageName**  | string  | requête     | Non         | —                | Le nom du stockage Aspose Cloud.                                             |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Réponses d’erreur typiques**

```json
{
    "Code":400,
    "Message":"Bad Request – paramètres manquants ou non valides."
}
```

```json
{
    "Code":401,
    "Message":"Unauthorized – jeton JWT non valide ou manquant."
}
```

```json
{
    "Code":413,
    "Message":"Payload Too Large – le fichier téléversé dépasse la taille autorisée."
}
```

```json
{
    "Code":500,
    "Message":"Internal Server Error – erreur inattendue du serveur."
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                  |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Bad Request                 | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Unauthorized                | Jeton JWT non valide ou manquant.                            |
| 413  | Payload Too Large           | Le fichier téléversé dépasse la limite de taille.            |
| 500  | Internal Server Error       | Erreur serveur inattendue.                                   |

## Comment utiliser l’API PutWorksheetFilterTop10 avec les SDK

### Spécification de l’API PutWorksheetFilterTop10

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
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

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}
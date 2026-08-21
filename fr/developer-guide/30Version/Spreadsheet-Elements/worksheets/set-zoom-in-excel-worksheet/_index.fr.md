---
title: "Définir le zoom d'une feuille Excel – Aspose.Cells Cloud API v3.0"
second_title: "Document"
linktitle: "Zoom"
type: docs
url: /worksheets/zoom/
aliases: [/set-zoom-in-excel-worksheet/]
keywords: "Aspose.Cells, zoom Excel, zoom de feuille de calcul, API REST, SDK cloud, automatisation Excel"
description: "Découvrez comment définir le zoom d'une feuille de calcul (de 10 à 400 %) à l’aide de l’API Aspose.Cells Cloud v3.0. Inclut des exemples cURL, des exemples de SDK et la gestion des erreurs."
weight: 20
ArticleTitle: "Définir le zoom d'une feuille Excel – Aspose.Cells Cloud API v3.0"
---

Cette API REST permet de définir la valeur de zoom d’une feuille de calcul Excel. **Une authentification est requise** ; incluez un jeton Bearer JWT valide dans l’en-tête `Authorization` de chaque requête.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **Paramètres de la requête**

| Paramètre    | Type    | Emplacement | Description                                                     |
| ------------ | ------- | ----------- | --------------------------------------------------------------- |
| name         | string  | chemin      | Nom du fichier Excel ( classeur ).                             |
| sheetName    | string  | chemin      | Nom de la feuille de calcul à modifier.                        |
| value        | integer | requête     | Pourcentage de zoom (intervalle autorisé **10 – 400**, ex. `40` pour 40 %). |
| folder       | string  | requête     | Chemin du dossier où le fichier est stocké.                    |
| storageName  | string  | requête     | Nom du service de stockage.                                     |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
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

**Informations sur la réponse d’erreur**  
Les codes d’état HTTP possibles sont les suivants :

- `400 Bad Request` – paramètres manquants ou non valides.
- `401 Unauthorized` – jeton JWT manquant ou non valide.
- `404 Not Found` – le fichier ou la feuille de calcul spécifié(s) n’existe(ent) pas.
- `500 Internal Server Error` – erreur inattendue côté serveur.

Chaque réponse d’erreur renvoie un corps JSON contenant un `Code` et un `Message` descriptif.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

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
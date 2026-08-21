---
title: "Supprimer un filtre de date – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Supprimer un filtre de date"
type: docs
url: /fr/autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, supprimer un filtre de date, filtre automatique Excel, API REST, SDK"
description: "Découvrez comment supprimer un filtre de date à partir d'une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint, les paramètres, un exemple cURL HTTPS, la charge utile de réponse et des extraits de code SDK."
ArticleTitle: "Supprimer un filtre de date – Documentation de l’API Aspose.Cells Cloud"
---

Cette API REST supprime un filtre de date sur une feuille Excel.

**Prérequis :** Assurez-vous d’avoir un jeton JWT valide, que le classeur est stocké dans le stockage Aspose Cloud et que vous disposez des autorisations appropriées pour modifier la feuille.

## API DeleteWorksheetDateFilter

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre     | Type    | Emplacement | Description                                                                                     |
|----------------------|---------|-------------|-------------------------------------------------------------------------------------------------|
| name                 | string  | chemin      | Nom du fichier Excel.                                                                          |
| sheetName            | string  | chemin      | Nom de la feuille de calcul.                                                                   |
| fieldIndex           | integer | requête     | Index à base zéro de la colonne à laquelle le filtre est appliqué.                             |
| dateTimeGroupingType | string  | requête     | Type de regroupement pour le filtre de date (par exemple, Year, Month, Day).                   |
| year                 | integer | requête     | Composante année du filtre (valeur par défaut : 0).                                             |
| month                | integer | requête     | Composante mois du filtre (valeur par défaut : 0).                                              |
| day                  | integer | requête     | Composante jour du filtre (valeur par défaut : 0).                                              |
| hour                 | integer | requête     | Composante heure du filtre (valeur par défaut : 0).                                             |
| minute               | integer | requête     | Composante minute du filtre (valeur par défaut : 0).                                            |
| second               | integer | requête     | Composante seconde du filtre (valeur par défaut : 0).                                           |
| folder               | string  | requête     | Chemin du dossier dans le stockage où le fichier est situé.                                     |
| storageName          | string  | requête     | Nom du stockage Aspose Cloud.                                                                  |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                                           |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                                  |

L’API renvoie des codes de statut HTTP standard indiquant le résultat de l’opération de suppression.

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Le filtre de date a été supprimé avec succès ; la réponse contient l’état de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                                           |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                                  |

## Comment utiliser l’API DeleteWorksheetDateFilter avec les SDK

### Spécification de l’API DeleteWorksheetDateFilter

La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
  -X DELETE \
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

Utiliser un SDK est la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
title: "Ajouter un filtre de date à une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ajouter un filtre de date"
type: docs
url: /fr/autofilter/add-date-filter/
aliases:
  - /fr/add-date-filter-in-a-worksheet/
  - /fr/autofilter/add-a-date-filter/
description: "Découvrez comment ajouter un filtre de date à une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut un exemple cURL, des extraits de code SDK (C#, Java, Python, etc.), les paramètres et la gestion des erreurs."
weight: 65
ArticleTitle: "Ajouter un filtre de date à une feuille de calcul Excel | API Aspose.Cells Cloud"
keywords: "Aspose.Cells, filtre de date Excel, API AutoFilter, API REST, SDK cloud, cURL, automatisation de feuilles de calcul"
---

Cette API REST ajoute un **filtre de date** à une feuille de calcul Excel.

**Prérequis :** Vous devez disposer d’un jeton JWT valide, et le classeur cible doit déjà exister à l’emplacement de stockage spécifié. La requête ne nécessite pas de corps JSON.

## API PutWorksheetDateFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête


| Nom du paramètre         | Type    | Emplacement | Description                                                                                                                                                     |
| ------------------------ | ------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path        | Le nom du classeur.                                                                                                                                             |
| **sheetName**            | string  | Path        | Le nom de la feuille de calcul.                                                                                                                                 |
| **range**                | string  | Query       | Plage Excel à laquelle le filtre est appliqué (par exemple, `A1:B1`).                                                                                           |
| **fieldIndex**           | integer | Query       | Index de colonne de base zéro à filtrer.                                                                                                                        |
| **dateTimeGroupingType** | string  | Query       | Type de regroupement pour le filtre de date/heure. Les valeurs autorisées sont `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. Les valeurs sont sensibles à la casse ; la valeur par défaut est `Day`. |
| **year**                 | integer | Query       | Composante année de la valeur de filtre.                                                                                                                        |
| **month**                | integer | Query       | Composante mois de la valeur de filtre.                                                                                                                         |
| **day**                  | integer | Query       | Composante jour de la valeur de filtre.                                                                                                                         |
| **hour**                 | integer | Query       | Composante heure de la valeur de filtre.                                                                                                                        |
| **minute**               | integer | Query       | Composante minute de la valeur de filtre.                                                                                                                       |
| **second**               | integer | Query       | Composante seconde de la valeur de filtre.                                                                                                                      |
| **matchBlanks**          | boolean | Query       | Inclure les cellules vides (`true` ou `false`).                                                                                                                 |
| **refresh**              | boolean | Query       | Actualiser le filtre après application (`true` ou `false`).                                                                                                     |
| **folder**               | string  | Query       | Chemin du dossier contenant le classeur original.                                                                                                               |
| **storageName**          | string  | Query       | Nom du service de stockage.                                                                                                                                     |

*La requête PUT ne nécessite pas de corps de requête ; tous les paramètres sont fournis via la chaîne de requête.*

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
| 400  | Bad Request (Requête incorrecte) | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Unauthorized (Non autorisé) | Jeton JWT invalide ou manquant.                                              |
| 413  | Payload Too Large (Charge utile trop volumineuse) | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Internal Server Error (Erreur interne du serveur) | Erreur serveur inattendue.                                                  |

## Comment utiliser l’API PutWorksheetDateFilter avec les SDK

### Spécification de l’API PutWorksheetDateFilter


La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer un appel à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
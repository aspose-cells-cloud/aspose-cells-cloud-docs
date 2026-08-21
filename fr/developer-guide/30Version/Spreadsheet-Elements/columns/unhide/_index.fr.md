---
title: "Réafficher des colonnes dans une feuille de calcul Excel"
ArticleTitle: "Réafficher des colonnes dans une feuille de calcul Excel – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, API Cloud, réafficher des colonnes, Excel, REST, SDK"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour réafficher des colonnes dans une feuille de calcul Excel. Inclut les détails de la requête, un exemple cURL et des exemples de code SDK pour plusieurs langages de programmation."
weight: 50
---

Cette API REST réaffiche les colonnes d'une feuille de calcul.

**Prérequis** – Tous les points de terminaison d’Aspose.Cells Cloud nécessitent HTTPS et un jeton d’accès OAuth 2.0 valide. Assurez-vous d’avoir obtenu un jeton d’accès et de l’avoir inclus dans l’en-tête `Authorization` de vos requêtes.

## API PostUnhideWorksheetColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                      |
| ---------------- | ------- | ----------- | ------------------------------------------------ |
| name             | string  | path        | Le nom du classeur.                              |
| sheetName        | string  | path        | Le nom de la feuille de calcul.                  |
| startColumn      | integer | query       | L'index de la première colonne à traiter.        |
| totalColumns     | integer | query       | Le nombre de colonnes à traiter.                 |
| width            | number  | query       | Largeur souhaitée des colonnes (par défaut = 50,0). |
| folder           | string  | query       | Le dossier contenant le document.                |
| storageName      | string  | query       | Le nom du service de stockage.                   |

La <a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

**Codes HTTP de statut typiques**

| Code | Description                                          |
|------|------------------------------------------------------|
| 200  | OK – Les colonnes ont été correctement réaffichées. |
| 400  | Requête incorrecte – Paramètres non valides.        |
| 401  | Non autorisé – Jeton manquant ou invalide.          |
| 404  | Introuvable – Classeur ou feuille de calcul non trouvé. |
| 500  | Erreur interne du serveur – Échec inattendu.        |

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
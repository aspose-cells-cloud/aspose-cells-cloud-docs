---
title: "Supprimer plusieurs lignes à partir d’une feuille de calcul Excel"
second_title: "Document"
linktitle: "Lignes"
type: docs
url: /rows/delete/rows/
keywords: "Aspose.Cells Cloud, supprimer des lignes, supprimer plusieurs lignes, feuille de calcul Excel, API REST, SDK"
description: "Découvrez comment supprimer une ou plusieurs lignes à partir d’une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails des points de terminaison, des paramètres, un exemple cURL et des exemples de code SDK pour divers langages."
weight: 80
ArticleTitle: "Supprimer plusieurs lignes d’une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST permet de supprimer plusieurs lignes **à partir** d’une feuille de calcul Excel.

**Conditions préalables :** Pour appeler ce point de terminaison, vous devez disposer d’un jeton d’accès JWT valide obtenu via l’authentification Aspose Cloud ainsi que des autorisations de stockage appropriées pour le classeur.

## API DeleteWorksheetRows

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Chemin / Chaîne de requête / Corps HTTP | Description                                                                 |
|------------------|---------|-----------------------------------------|-----------------------------------------------------------------------------|
| name             | string  | chemin                                  | Le nom du classeur.                                                         |
| sheetName        | string  | chemin                                  | Le nom de la feuille de calcul.                                             |
| startrow         | integer | requête                                 | Indice de la première ligne à supprimer (à partir de zéro ; par ex. `0` = première ligne). |
| totalRows        | integer | requête                                 | Le nombre de lignes à supprimer.                                            |
| updateReference  | boolean | requête                                 | Indique s’il faut mettre à jour les références après la suppression (`true`/`false`). |
| folder           | string  | requête                                 | Le dossier du document.                                                     |
| storageName      | string  | requête                                 | Le nom du stockage.                                                         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud via cURL. **Tous les points de terminaison exigent HTTPS ; HTTP est obsolète.**

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton JWT>"
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

**Codes de réponse possibles**

| Statut HTTP | Description |
|-------------|-------------|
| 200 | Lignes supprimées avec succès. |
| 400 | Requête incorrecte – paramètres non valides. |
| 401 | Non autorisé – jeton JWT manquant ou non valide. |
| 404 | Introuvable – le classeur ou la feuille de calcul n’existe pas. |
| 500 | Erreur interne du serveur – condition inattendue. |

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
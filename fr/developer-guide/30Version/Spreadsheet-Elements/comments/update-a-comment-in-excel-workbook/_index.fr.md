---
title: "Mettre à jour le commentaire d'une cellule d'une feuille de calcul"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, API REST, Excel, feuille de calcul, commentaire de cellule, mise à jour du commentaire de feuille de calcul, objet commentaire"
description: "Utilisez l’API REST Aspose.Cells Cloud pour mettre à jour le commentaire d’une cellule dans une feuille de calcul d’un classeur Excel, y compris les détails de la requête, les codes de réponse et les exemples de SDK."
weight: 30
ArticleTitle: "Mettre à jour le commentaire d'une cellule de feuille de calcul – Aspose.Cells Cloud API"
---

Cette API REST met à jour le commentaire d'une cellule d'une feuille de calcul. Utilisez ce point de terminaison pour **mettre à jour un commentaire de feuille de calcul** dans un fichier Excel.

**Prérequis :**  
- Un jeton d'accès OAuth/JWT valide doit être inclus dans l'en-tête `Authorization`.  
- Le classeur doit être stocké dans un emplacement de stockage cloud pris en charge (spécifiez `folder` et éventuellement `storageName`).

## API PostWorksheetComment

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                               |
| ---------------- | ------ | ----------- | ------------------------------------------------------------------------- |
| name             | string | path        | Le nom du document Excel.                                                |
| sheetName        | string | path        | Le nom de la feuille de calcul contenant la cellule.                    |
| cellName         | string | path        | L'adresse de la cellule (par exemple, **A1**).                           |
| comment          | object | body        | Un objet **Comment** qui définit le commentaire à ajouter ou mettre à jour. |
| folder           | string | query       | Le dossier dans lequel le document est stocké.                          |
| storageName      | string | query       | Le nom du service de stockage.                                           |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) définit une interface de programmation accessible publiquement et vous permet d'effectuer directement des interactions REST à partir d'un navigateur web.

Vous pouvez utiliser l'outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L'exemple suivant montre comment effectuer un appel à l'API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "ceci est un commentaire",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
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

Codes de statut de réponse possibles :

| Code | Description                                         |
|------|-----------------------------------------------------|
| 200  | Commentaire mis à jour avec succès.                |
| 400  | Requête incorrecte – paramètres manquants ou non valides. |
| 401  | Non autorisé – échec de l'authentification.        |
| 404  | Introuvable – le classeur, la feuille de calcul ou le commentaire n'existe pas. |
| 500  | Erreur interne du serveur.                          |

**Notes / Conseils :**  
- La longueur maximale d’un commentaire est de 1024 caractères.  
- Les caractères pris en charge sont en UTF‑8 ; évitez les caractères de contrôle.

## Famille de SDK Cloud

L'utilisation d'un SDK est le moyen le plus rapide de développer avec Aspose.Cells Cloud. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

Opérations associées :  
- [Obtenir le commentaire de feuille de calcul](/comments/get/)  
- [Ajouter un commentaire de feuille de calcul](/comments/add/)  
- [Supprimer le commentaire de feuille de calcul](/comments/delete/)
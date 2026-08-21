---
title: "Ajouter plusieurs lignes à une feuille de calcul Excel"
ArticleTitle: "Ajouter plusieurs lignes à une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
second_title: "Document"
linktype: "Lignes"
type: docs
url: /fr/rows/add/rows/
keywords: "Aspose.Cells Cloud, insérer des lignes, feuille de calcul Excel, API REST, SDK, ajouter plusieurs lignes"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour insérer plusieurs lignes dans une feuille de calcul Excel. Ce guide couvre le point de terminaison, les paramètres de requête, les commandes cURL d’exemple et des exemples d’utilisation du SDK."
weight: 20
---

Cette API REST permet d’ajouter plusieurs nouvelles lignes à une feuille de calcul Excel.

## API PutInsertWorksheetRows

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                              |
|------------------|---------|-------------|--------------------------------------------------------------------------|
| name             | string  | chemin      | Le nom du classeur.                                                      |
| sheetName        | string  | chemin      | Le nom de la feuille de calcul.                                          |
| startrow         | integer | requête     | L’index de la première ligne à insérer (**indexation à 0**).             |
| totalRows        | integer | requête     | Le nombre de lignes à insérer.                                           |
| updateReference  | boolean | requête     | Indique s’il faut mettre à jour les références de cellules après insertion (`true` ou `false`). |
| folder           | string  | requête     | Le dossier contenant le document.                                        |
| storageName      | string  | requête     | Le nom du stockage.                                                      |

**Conditions préalables**  
Le classeur doit déjà exister dans le stockage (ou dossier) spécifié avant d’invoquer cette opération.

**Authentification**  
L’API exige un jeton JWT valide. Incluez-le dans l’en-tête `Authorization`, comme indiqué dans l’exemple cURL ci-dessous.

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

> **Remarque :** Cette opération `PUT` ne nécessite pas de corps de requête ; un objet JSON vide (`{}`) peut être envoyé si la bibliothèque client impose la présence d’un payload.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Codes de réponse possibles*  

- **200 OK** – Lignes insérées avec succès.  
- **400 Bad Request** – Paramètres invalides (par exemple, index de ligne négatif).  
- **401 Unauthorized** – Jeton JWT manquant ou invalide.  
- **404 Not Found** – Le classeur ou la feuille de calcul spécifiés n’existent pas.  
- **500 Internal Server Error** – Erreur serveur inattendue.

{{< /tab >}}

{{< /tabs >}}

Pour d’autres opérations sur les lignes, consultez les pages associées : **Supprimer des lignes**, **Obtenir les lignes** et **Copier des lignes**.

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
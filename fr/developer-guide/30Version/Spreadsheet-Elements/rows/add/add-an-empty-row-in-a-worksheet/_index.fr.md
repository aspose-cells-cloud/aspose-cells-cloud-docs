---
title: "Ajouter une ligne vide dans une feuille de calcul Excel"
ArticleTitle: "Ajouter une ligne vide à une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
second_title: "Document"
linktype: "Ligne"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, ajouter une ligne vide, feuille de calcul, API REST, insérer une ligne, feuille de calcul cloud"
description: "Utilisez l’API REST Aspose.Cells Cloud pour insérer une ligne vide dans une feuille de calcul Excel. Prend en charge de nombreux SDK (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) pour un développement rapide."
weight: 20
---

Cette API REST ajoute une nouvelle ligne à une feuille de calcul Excel. Elle insère une ligne vide à l’index zéro-based spécifié.

**Conditions préalables :**  
- Un jeton d’accès Aspose Cloud valide (Bearer JWT) doit être inclus dans l’en-tête `Authorization`.  
- Le classeur cible doit être chargé dans votre stockage Aspose Cloud, et les paramètres `folder` et `storageName` doivent pointer vers son emplacement.

**Notes :**  
- L’index `rowIndex` est zéro-based ; l’insertion à l’index 0 ajoute une ligne en haut de la feuille de calcul.  
- Les feuilles de calcul Excel comportent un maximum de 1 048 576 lignes ; tenter d’insérer au-delà de cette limite entraînera une erreur.

## API PutInsertWorksheetRow

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                  |
| ---------------- | ------- | ----------- | ------------------------------------------------------------ |
| name             | string  | path        | Le nom du fichier du classeur.                              |
| sheetName        | string  | path        | Le nom de la feuille de calcul.                             |
| rowIndex         | integer | path        | L’index zéro-based à partir duquel la nouvelle ligne sera insérée. |
| folder           | string  | query       | Le chemin du dossier dans le stockage contenant le classeur. |
| storageName      | string  | query       | Le nom du stockage Aspose Cloud à utiliser.                 |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) définit une interface de programmation publiquement accessible et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

> **Remarque :** Tous les points de terminaison Aspose.Cells Cloud exigent HTTPS. Utilisez le schéma sécurisé `https://` pour les appels en production.

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

**Codes de statut HTTP**

| Code | Signification               | Description                                                     |
|------|-----------------------------|-----------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                     |

*Exemple de réponse d’erreur (par exemple, si l’index de ligne dépasse la limite de la feuille de calcul) :*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Index de ligne hors limites. Nombre maximal de lignes autorisé : 1048576."
}
```

## Famille de SDK Cloud

Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}
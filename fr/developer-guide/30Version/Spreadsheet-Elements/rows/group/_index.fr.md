---
title: "Regrouper des lignes dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Regrouper"
type: docs
url: /fr/rows/group/
aliases: [  /fr/group-rows-in-excel-worksheet/ ]
keywords: "regrouper des lignes, Excel, Aspose.Cells Cloud, API REST, SDK, feuille de calcul, API Excel"
description: "Regrouper des lignes dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Prend en charge plusieurs SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) pour une intégration simplifiée."
weight: 60
ArticleTitle: "Regrouper des lignes dans une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cet API REST permet de regrouper des lignes dans une feuille de calcul Excel.

**Prérequis :**  
- Un jeton d’accès OAuth 2.0 valide (Bearer JWT) doit être fourni dans l’en-tête `Authorization`.  
- Le classeur doit déjà exister dans le `folder` spécifié de la `storageName` choisie (ou dans le stockage par défaut) avant l’envoi de la requête.

## API PostGroupWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                              |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------ |
| name             | string  | path        | Nom du fichier du classeur.                                              |
| sheetName        | string  | path        | Nom de la feuille de calcul.                                             |
| firstIndex       | integer | query       | Index de base zéro de la première ligne à regrouper.                     |
| lastIndex        | integer | query       | Index de base zéro de la dernière ligne à regrouper.                     |
| hide             | boolean | query       | Indique si les lignes groupées doivent être masquées (`true` ou `false`). |
| folder           | string  | query       | Chemin du dossier contenant le classeur.                                 |
| storageName      | string  | query       | Nom du stockage dans lequel se trouve le classeur.                       |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Payload trop volumineux     | Le fichier envoyé dépasse la taille limite autorisée.                      |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                                          |

Réponses d’erreur typiques :

- **400 Mauvaise requête** – vérifiez que `firstIndex` et `lastIndex` sont des entiers valides et que `firstIndex` ≤ `lastIndex`.  
- **401 Non autorisé** – vérifiez que l’en-tête `Authorization` contient un jeton JWT valide et à jour.  
- **404 Non trouvé** – assurez-vous que le classeur (`name`) et la feuille de calcul (`sheetName`) existent dans le `folder` / `storageName` spécifiés.

{{< /tab >}}

{{< /tabs >}}

**Voir aussi :** [Dégrouper des lignes dans une feuille de calcul Excel](../rows/ungroup/ "Dégrouper des lignes dans une feuille de calcul Excel"), [Masquer des lignes dans une feuille de calcul Excel](../rows/hide/ "Masquer des lignes dans une feuille de calcul Excel"), [Afficher des lignes masquées dans une feuille de calcul Excel](../rows/unhide/ "Afficher des lignes masquées dans une feuille de calcul Excel").

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur vos tâches de projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
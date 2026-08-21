---
title: "Ajouter une colonne vide à une feuille de calcul Excel - API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Ajouter"
type: docs
url: /fr/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "ajouter, colonne, Excel, API, Aspose.Cells, Cloud, REST, insérer"
description: "Découvrez comment insérer une nouvelle colonne dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe de la requête, un exemple cURL et des extraits de code SDK."
weight: 20
ArticleTitle: "Ajouter une colonne vide à une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST insère une ou plusieurs colonnes dans une feuille de calcul.

**Conditions préalables**  
Avant d’appeler ce point de terminaison, assurez-vous d’avoir effectué les étapes suivantes :

- Obtenir un jeton d’accès OAuth 2.0 valide et l’inclure dans l’en-tête `Authorization`.  
- Stocker le classeur cible dans le stockage sélectionné (par défaut = « Default ») ou spécifier les paramètres appropriés `folder` et `storageName`.  
- Vérifier que le nom de la feuille de calcul fourni dans `sheetName` existe dans le classeur.

## API PutInsertWorksheetColumns

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                           |
| ----------------- | ------- | ----------- | --------------------------------------------------------------------- |
| **name**          | string  | path        | Nom du fichier de classeur.                                           |
| **sheetName**     | string  | path        | Nom de la feuille de calcul.                                          |
| **columnIndex**   | integer | path        | Index de colonne en base zéro à partir duquel commence l’insertion.  |
| **totalColumns**  | integer | query       | Nombre de colonnes à insérer.                                         |
| **updateReference** | boolean | query     | Si **true**, les références aux cellules sont mises à jour pour refléter l’insertion. |
| **folder**        | string  | query       | Chemin du dossier contenant le classeur.                             |
| **storageName**   | string  | query       | Nom du service de stockage.                                           |

**Notes**

- Le `columnIndex` doit être compris entre 0 et le nombre actuel de colonnes dans la feuille de calcul. L’insertion au-delà de la plage existante élargit automatiquement la feuille.  
- L’insertion de plusieurs colonnes (`totalColumns` > 1) décale les colonnes existantes vers la droite.  
- Le drapeau `updateReference` vaut `false` par défaut ; définissez-le sur `true` pour mettre à jour les formules et les plages nommées.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler les services web Aspose.Cells. L’exemple suivant montre une requête complète, incluant l’authentification et le paramètre de chemin correct.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <jeton_daccès>" \
     -H "accept: application/json"
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

**Codes de réponse**

| Code | Description                                    |
|------|------------------------------------------------|
| 200  | Colonne(s) insérée(s) avec succès.             |
| 400  | Requête incorrecte – paramètres manquants ou invalides. |
| 401  | Non autorisé – jeton invalide ou manquant.    |
| 404  | Classeur ou feuille de calcul introuvable.    |
| 500  | Erreur interne du serveur.                     |

**Exemples de réponses d’erreur**

```json
// 400 Requête incorrecte – paramètres manquants ou invalides
{
  "Code": 400,
  "Message": "Paramètre invalide : totalColumns doit être un entier positif."
}

// 401 Non autorisé – jeton invalide ou manquant
{
  "Code": 401,
  "Message": "Échec de l’authentification. Le jeton d’accès est manquant ou invalide."
}

// 404 Non trouvé – le classeur ou la feuille de calcul n’existe pas
{
  "Code": 404,
  "Message": "Le classeur « test.xlsx » est introuvable."
}

// 500 Erreur interne du serveur
{
  "Code": 500,
  "Message": "Une erreur inattendue s’est produite sur le serveur."
}
```

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur la logique de votre projet. Consultez le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
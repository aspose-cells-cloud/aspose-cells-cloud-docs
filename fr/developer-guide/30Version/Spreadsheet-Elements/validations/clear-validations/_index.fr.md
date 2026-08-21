---
title: "Supprimer toutes les validations de feuille de calcul – API Aspose.Cells Cloud"
second_title: "Documentation"
linktitle: "Supprimer"
type: docs
url: /fr/validations/clear/
keywords: "Aspose.Cells Cloud, Supprimer les validations de feuille de calcul, Excel, API REST, Validation de feuille de calcul, API"
description: "Supprimer toutes les règles de validation de données d'une feuille de calcul dans un fichier Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut les étapes d'authentification, les détails de la requête, un exemple cURL, le schéma de réponse, la gestion des erreurs et des extraits de code SDK."
weight: 10
---

**Conditions préalables**

- Un compte Aspose Cloud valide.
- Un jeton d’accès JWT obtenu via l’API d’authentification Aspose Cloud (`/connect/token`).
- Le classeur doit être stocké dans votre espace de stockage Aspose Cloud (ou les paramètres de requête optionnels `folder` / `storageName` doivent être fournis).

Cette API REST supprime toutes les validations de feuille de calcul d’une feuille Excel.

## API REST

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                             |
| ---------------- | ------ | ----------- | ------------------------------------------------------- |
| name             | string | path        | Le nom du document Excel.                              |
| sheetName        | string | path        | Le nom de la feuille de calcul contenant les validations. |
| folder           | string | query       | Le dossier dans lequel le document est stocké.        |
| storageName      | string | query       | Le nom du service de stockage.                         |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API à l’aide de cURL après avoir obtenu un jeton JWT.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
  -X DELETE \
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

{{< /tab >}}

{{< /tabs >}}

### Gestion des erreurs

| Statut HTTP | Signification         | Description                                              |
| ----------- | --------------------- | -------------------------------------------------------- |
| 400         | Mauvaise requête      | La requête est mal formée ou les paramètres obligatoires sont manquants. |
| 401         | Non autorisé          | Le jeton JWT est manquant, invalide ou expiré.           |
| 404         | Non trouvé            | Le classeur ou la feuille de calcul spécifié(s) n’existe(nt) pas. |
| 500         | Erreur interne du serveur | Une erreur inattendue s’est produite côté serveur.      |

La charge utile d’erreur suit la même structure JSON avec les champs `Code` et `Message`, par exemple :

```json
{
  "Code": 401,
  "Message": "Jeton invalide ou expiré."
}
```

## Famille de SDK Cloud

Utiliser un SDK est le moyen le plus rapide de développer. Un SDK abstrait les détails de bas niveau afin que vous puissiez vous concentrer sur la logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}
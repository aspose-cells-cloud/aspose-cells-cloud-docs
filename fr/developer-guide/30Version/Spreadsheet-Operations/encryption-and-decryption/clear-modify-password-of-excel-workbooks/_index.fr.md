---
title: "Supprimer la protection en écriture (mot de passe) d’un classeur Excel"
second_title: "Document"
linktitle: "Effacer le mot de passe des fichiers Excel"
type: docs
url: /fr/clear-excel-files-password/
aliases:
  [
    /clear-modify-password-of-excel-workbooks/,
    /workbook/clear-modify-password/，/workbook/password/clear/,
  ]
keywords: "Aspose.Cells, Excel, suppression de mot de passe, protection en écriture, API REST, exemples de SDK"
description: "Découvrez comment supprimer la protection en écriture (mot de passe) d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut un exemple cURL, les étapes d’authentification et des exemples de code SDK."
weight: 110
ArticleTitle: "Supprimer la protection en écriture (mot de passe) d’un classeur Excel"
---

Cette API REST supprime la **protection en écriture (mot de passe)** d’un classeur Excel, vous permettant ainsi de supprimer la protection par mot de passe d’un fichier Excel de manière programmatique.

**Prérequis :** Obtenez un jeton JWT valide, assurez-vous que le classeur est stocké dans un emplacement pris en charge, et utilisez la version de l’API v3.0.

Pour ajouter une protection, consultez le guide [Protéger un fichier Excel](/cells/protect/).

## API DeleteDocumentUnprotectFromChanges

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                           |
| ---------------- | ------ | ----------- | ----------------------------------------------------- |
| `name`           | string | path        | Le nom du classeur Excel.                             |
| `folder`         | string | query       | Le dossier contenant le classeur (facultatif).       |
| `storageName`    | string | query       | Le nom du service de stockage (facultatif).          |


### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                |
| ---- | --------------------------- | ---------------------------------------------------------- |
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                           |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.       |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue.                                |

## Comment utiliser l’API DeleteDocumentUnprotectFromChanges avec les SDK

### Spécification de l’API DeleteDocumentUnprotectFromChanges

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services Aspose.Cells. L’exemple ci-dessous montre comment effectuer un appel à l’API REST avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
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


### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}
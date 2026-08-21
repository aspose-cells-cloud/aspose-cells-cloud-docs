---
title: "Supprimer une propriété de document spécifique"
second_title: "Document"
linktitle: "Supprimer"
type: docs
url: /fr/document-properties/delete/
aliases: [  /fr/remove-a-particular-document-property/ ]
keywords: "Aspose.Cells, supprimer une propriété de document, API de métadonnées Excel, REST, SDK cloud, exemple cURL"
description: "Supprimer une propriété de document spécifique d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud v3.0. Inclut des exemples cURL et des exemples de SDK pour C#, Java, Python, et plus encore."
weight: 50
---

Cette API REST supprime une propriété de document à partir d’un classeur.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Obligatoire | Description                                             |
| ---------------- | ------ | ----------- | ----------- | ------------------------------------------------------- |
| name             | string | path        | Oui         | Le nom du classeur Excel.                              |
| propertyName     | string | path        | Oui         | Le nom de la propriété de document à supprimer.       |
| folder           | string | query       | Non         | Le chemin du dossier dans lequel le classeur est stocké. |
| storageName      | string | query       | Non         | Le nom du service de stockage.                         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
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

### Réponses d’erreur

| Statut HTTP | Description                                                              | Exemple JSON                                                       |
| ----------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------ |
| 400         | Requête incorrecte – paramètres requis manquants ou valeurs invalides. | `{"Code":400,"Message":"Paramètre requis manquant : 'name'."}`    |
| 401         | Non autorisé – jeton JWT invalide ou absent.                            | `{"Code":401,"Message":"Jeton d'accès invalide."}`                |
| 404         | Introuvable – le classeur ou la propriété spécifiée n’existe pas.       | `{"Code":404,"Message":"Propriété de document introuvable."}`     |
| 500         | Erreur interne du serveur – une condition inattendue s’est produite.   | `{"Code":500,"Message":"Une erreur inattendue s'est produite."}` |

## Famille de SDK cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}
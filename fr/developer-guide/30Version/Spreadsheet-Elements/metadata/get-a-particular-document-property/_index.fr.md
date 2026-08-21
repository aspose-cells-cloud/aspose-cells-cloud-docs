---
title: "Obtenir une propriété spécifique d’un document"
second_title: "Document"
linktitle: "Obtenir"
type: docs
url: /fr/document-properties/get/
aliases: [  /fr/get-a-particular-document-property/ ]
keywords: "Aspose.Cells, API Cloud, Obtenir une propriété de document, métadonnées Excel, REST GET, exemples de SDK"
description: "Récupérer une propriété de document nommée (par exemple, Auteur, Titre) à partir d’un fichier Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut un exemple cURL, des extraits de code SDK et le schéma de réponse."
weight: 20
---

Cette API REST lit une propriété de document par son nom.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                    |
| ---------------- | ------ | ----------- | ---------------------------------------------- |
| name             | string | path        | Le nom du fichier Excel.                       |
| propertyName     | string | path        | Le nom de la propriété de document à récupérer. |
| folder           | string | query       | Le dossier contenant le fichier (facultatif).  |
| storageName      | string | query       | Le nom du stockage (facultatif).               |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Détails de la réponse

L’objet JSON retourné par l’API contient les champs suivants :

| Champ                               | Type    | Description                                                           |
| ----------------------------------- | ------- | --------------------------------------------------------------------- |
| **DocumentProperty.Name**           | string  | Le nom de la propriété (par exemple, `Author`).                        |
| **DocumentProperty.Value**          | string  | La valeur de la propriété. Peut être vide si non définie.             |
| **DocumentProperty.BuiltIn**        | boolean | Indique si la propriété est une propriété intégrée d’Excel.            |
| **DocumentProperty.link.Href**      | string  | URL relative vers la ressource de la propriété.                        |
| **DocumentProperty.link.Rel**       | string  | Type de relation, généralement `self`.                                 |
| **DocumentProperty.link.Title**     | string  | Titre lisible par un humain (peut être `null`).                        |
| **DocumentProperty.link.Type**      | string  | Type MIME de la ressource liée (peut être `null`).                     |
| **Code**                            | integer | Code d’état HTTP renvoyé par le service.                               |
| **Status**                          | string  | Description textuelle de l’état (par exemple, `OK`).                   |

### Réponses d’erreur

| Statut HTTP | Code                   | Description                                              |
| ----------- | ---------------------- | -------------------------------------------------------- |
| 400         | `InvalidParameter`     | Un ou plusieurs paramètres de requête sont invalides.    |
| 401         | `AuthenticationFailed` | Jeton JWT manquant ou invalide.                          |
| 404         | `PropertyNotFound`     | La propriété de document spécifiée n’existe pas.         |
| 500         | `InternalError`        | Une erreur inattendue s’est produite sur le serveur.     |

Un corps d’erreur typique ressemble à :

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## Famille de SDK Cloud

Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Terminologie

| Terme                   | Définition                                                                                      |
| ----------------------- | ----------------------------------------------------------------------------------------------- |
| **Propriété de document** | Une métadonnée associée à un classeur Excel (par exemple, Auteur, Titre, Créé).                 |
| **Métadonnées**         | Terme générique désignant les données qui décrivent d’autres données ; ici, cela fait référence aux propriétés de document. |
| **Propriété personnalisée** | Une propriété définie par l’utilisateur, non incluse dans l’ensemble intégré.                 |

### Questions fréquentes (FAQ)

**Q :** *Comment puis-je récupérer la propriété Auteur d’un fichier Excel stocké dans Aspose Cloud ?*  
**A :** Envoyez une requête GET vers `https://api.aspose.cloud/v3.0/cells/{nomFichier}/documentproperties/author` avec un jeton Bearer valide. La réponse JSON inclut `DocumentProperty.Name = "Author"` et sa `Value`.

**Q :** *Quelle erreur est renvoyée si la propriété demandée n’existe pas ?*  
**A :** L’API renvoie HTTP 404 avec un corps JSON contenant `Code : 404` et `Status : "Property not found"`.

**Q :** *Dois-je spécifier `storageName` lorsque le fichier se trouve dans le stockage par défaut ?*  
**A :** Non. Le paramètre de requête `storageName` est facultatif ; omettez-le pour utiliser le stockage par défaut configuré pour votre compte.
---
title: "Récupérer les éléments texte d’un classeur Excel"
ArticleTitle: "Récupérer les éléments texte d’un classeur Excel à l’aide de l’API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /workbook/get-text-items/
aliases: [/get-text-items-from-a-workbook/]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, API REST, Classeur, Récupérer les éléments texte"
description: "Récupérez les éléments texte d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud. Disponible via les SDK pour C#, Java, Python, PHP, Ruby, Go, Node.js, Perl et Swift."
---


## API REST

Cette API REST lit les **éléments texte** d’un classeur dans un fichier Excel.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.


### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                            |
| ---------------- | ------ | ----------- | ------------------------------------------------------ |
| name             | string | path        | Le nom du fichier du classeur.                         |
| folder           | string | query       | Le chemin du dossier dans le stockage où réside le classeur. |
| storageName      | string | query       | Le nom du service de stockage.                         |

### **Réponse**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                   |
|------|-----------------------------|---------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Payload trop volumineux     | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur. |

## Comment utiliser l’API GetWorkbookTextItems avec les SDK

### Spécification de l’API GetWorkbookTextItems

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

Codes de réponse HTTP typiques :

| Code | Description                                           |
|------|-------------------------------------------------------|
| 200  | Requête réussie ; les éléments texte sont retournés. |
| 401  | Non autorisé – jeton manquant ou non valide.         |
| 403  | Interdit – permissions insuffisantes.                 |
| 404  | Non trouvé – classeur ou ressource introuvable.       |
| 500  | Erreur interne du serveur – échec inattendu.          |

### Utiliser les SDK Aspose.Cells Cloud

Cet exemple utilise la version de l’API **v3.0** ; consultez le journal des modifications pour les versions plus récentes. L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}
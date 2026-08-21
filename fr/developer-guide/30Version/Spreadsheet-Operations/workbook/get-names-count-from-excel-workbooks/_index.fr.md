---
title: "Récupérer les noms d'un classeur Excel"
second_title: "Document"
linktitle: "Noms"
type: docs
url: /fr/get-names-from-an-excel-file/
aliases:
  [
    "/get-names-count-from-excel-workbooks/",
    "/workbook/names/",
    "/workbook/get/names/",
  ]
keywords: "Aspose.Cells, Cloud, Excel, Classeur, Noms, API REST, SDK"
description: "Récupérer tous les noms définis dans un classeur Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut des conseils sur l'authentification, un exemple cURL, le schéma de réponse, la gestion des erreurs et des exemples de SDK."
weight: 120
ArticleTitle: "Récupérer les noms d'un classeur Excel – Aspose.Cells Cloud API"
---

Cette API REST permet de récupérer les noms définis dans un classeur Excel.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## API GetWorkbookNames

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description                            |
| ---------------- | ------ | ----------- | -------------------------------------- |
| name             | string | path        | Nom du fichier classeur.               |
| folder           | string | query       | Dossier contenant le classeur.         |
| storageName      | string | query       | Nom du stockage à utiliser.            |

La requête doit inclure les en-têtes HTTP suivants :

| En-tête         | Type   | Description                                         |
| --------------- | ------ | --------------------------------------------------- |
| Authorization   | string | Jeton bearer JWT (obligatoire)                      |
| Accept          | string | `application/json`                                  |
| Content-Type    | string | `application/json` (pour les requêtes contenant un corps) |

**Authentification** – L’API exige un jeton bearer OAuth2/JWT. Obtenez un jeton à partir de `https://api.aspose.cloud/connect/token` à l’aide de votre client-id et client-secret, puis incluez l’en-tête `Authorization: Bearer <jeton jwt>` dans chaque requête.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API Aspose.Cells Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "chaîne de caractères",
  "Names": {
    "link": {
      "Href": "chaîne de caractères",
      "Rel": "chaîne de caractères",
      "Title": "chaîne de caractères",
      "Type": "chaîne de caractères"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "chaîne de caractères",
          "Rel": "chaîne de caractères",
          "Title": "chaîne de caractères",
          "Type": "chaîne de caractères"
        }
      }
    ]
  }
}
```

**Champs de la réponse**

- **Status** _(string)_ – Message indiquant le statut de l’opération.
- **Names.link** _(object)_ – Informations d’hyperlien concernant la collection.
- **Names.Count** _(integer)_ – Nombre total de noms définis retournés.
- **Names.NameList** _(array)_ – Liste des objets nom ; chaque objet contient un objet **link** avec les détails de navigation.

**Gestion des erreurs** – Le service peut renvoyer les codes de statut HTTP suivants :

| Code | Signification              | Action recommandée                                               |
| ---- | -------------------------- | ---------------------------------------------------------------- |
| 401  | Non autorisé               | Vérifiez qu’un jeton JWT valide est fourni.                      |
| 404  | Introuvable                | Vérifiez que le nom du classeur, le dossier et le stockage sont corrects. |
| 500  | Erreur interne du serveur  | Réessayez ultérieurement ou contactez le support Aspose si le problème persiste. |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}
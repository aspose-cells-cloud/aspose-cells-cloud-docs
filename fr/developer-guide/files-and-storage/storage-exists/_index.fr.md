---
title: "Vérifier si un stockage existe – API Aspose.Cells Cloud (v4.0)"
second_title: "Document"
ArticleTitle: "Gestion cloud des fichiers Excel – Vérifier l’existence d’un stockage"
linktitle: "Le stockage existe"
type: docs
url: /storage-exists/
keywords: "Aspose.Cells, stockage existe, API de stockage cloud, REST, Excel"
description: "Vérifiez l’existence d’un conteneur de stockage dans Aspose.Cells Cloud. Découvrez le point de terminaison GET /v4.0/cells/storage/{storageName}/exist, les paramètres requis, le format de la réponse, et voyez des exemples de SDK en C#, Java, Python et plus encore."
weight: 100
---

L’API `storageExists` permet de vérifier si un stockage spécifié existe dans le service cloud Aspose.Cells. Cette fonctionnalité est essentielle pour garantir que toutes les opérations dépendant du stockage peuvent s’exécuter sans erreur.
**Résumé** – Le point de terminaison `storageExists` vous permet de confirmer si un conteneur de stockage spécifique est disponible dans Aspose.Cells Cloud. Utilisez-le avant d’effectuer des opérations liées aux fichiers afin d’éviter les erreurs à l’exécution.

## Vérifier l’existence d’un stockage (storageExists)

### API Web

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                           |
| ---------------- | ------ | ----------- | ----------------------------------------------------- |
| storageName      | String | Path        | Le nom du stockage dont on souhaite vérifier l’existence. |

### **Réponse**

```json
{
  "Name": "StorageExist",
  "Description": ["Indique si le stockage spécifié existe."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indique si le stockage existe.",
        "Cette propriété renvoie true si le stockage est présent ; sinon, elle renvoie false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**Codes d’état HTTP**

| Code | Signification         | Description                                                      |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.         |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                  |

## Comment utiliser l’API de vérification d’existence de stockage avec les SDK ?

### Spécification OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement, permettant aux développeurs d’interagir facilement avec l’API REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus efficace pour accélérer le développement. Un SDK masque les détails d’implémentation de bas niveau, permettant aux développeurs de se concentrer sur les tâches de leur projet. Pour une liste complète des SDK disponibles d’Aspose.Cells Cloud, veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">dépôt GitHub</a>.

Les exemples de code suivants montrent comment effectuer des appels API aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}
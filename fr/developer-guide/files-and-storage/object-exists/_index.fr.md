---
title: "API Object Exists – Vérifier la présence d’un fichier/dossier dans Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "API Object Exists – Vérifier la présence d’un fichier ou d’un dossier dans Aspose.Cells Cloud"
linktype: "docs"
url: /fr/object-exists/
keywords: "Aspose.Cells, stockage cloud, objet existant, existence de fichier, existence de dossier, API"
description: "Utilisez l’API Object Exists pour vérifier rapidement si un fichier ou un dossier existe dans le stockage Aspose.Cells Cloud. Prend en charge le nom de stockage et l’ID de version optionnels, et fonctionne avec des objets versionnés."
weight: 100
---

L’**API Object Exists** permet aux développeurs de déterminer si un fichier ou un dossier spécifique est présent dans le stockage Aspose.Cells Cloud. Elle renvoie une valeur booléenne simple indiquant l’existence et si le chemin pointe vers un dossier.

## **API Excel : Object Exists**

### API Web

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ est le chemin complet vers le fichier ou le dossier dans le stockage.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Obligatoire | Description                                                                 |
| ---------------- | ------ | ----------- | ----------- | --------------------------------------------------------------------------- |
| `path`           | string | Chemin      | Oui         | Chemin complet vers le fichier ou le dossier.                               |
| `storageName`    | string | Requête     | Non         | Nom du stockage ; utilise le stockage principal par défaut si omis.        |
| `versionId`      | string | Requête     | Non         | Identifiant spécifique de la version du fichier (si la gestion des versions est activée). |

**Codes de statut HTTP**

| Code HTTP | Statut HTTP           | Description                                                           |
| --------- | --------------------- | --------------------------------------------------------------------- |
| 200       | OK                    | L’API Web a été appelée avec succès ; la réponse contient les détails de l’opération. |
| 400       | Mauvaise requête      | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401       | Non autorisé          | Jeton JWT invalide ou manquant.                                       |
| 413       | Charge utile trop volumineuse | Le fichier envoyé dépasse la limite de taille.                     |
| 500       | Erreur interne du serveur | Erreur inattendue du serveur.                                        |

### **Réponse**

Un appel réussi renvoie une charge utile JSON contenant deux propriétés :

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – `true` si le fichier ou le dossier existe ; sinon `false`.
- **IsFolder** – `true` si le chemin pointe vers un dossier ; `false` pour un fichier.

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment passer des appels à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

L’utilisation d’un SDK constitue la meilleure approche pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment passer des appels aux services web Aspose.Cells à l’aide de divers SDK. Si un Gist ne se charge pas, un exemple statique est fourni sous chaque onglet.
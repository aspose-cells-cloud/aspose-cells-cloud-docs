---
title: "Aspose.Cells Cloud – API de suppression de fichier"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud – API de suppression de fichier"
linktype: "docs"
url: /fr/delete-file/
keywords: "Aspose Cells, API de suppression de fichier, stockage cloud Excel, API REST, gestion de fichiers"
description: "Supprimez un fichier Excel depuis le stockage cloud Aspose.Cells Cloud à l'aide de l'API REST de suppression de fichier. Inclut le point de terminaison, les paramètres, l'authentification et un exemple de code."
weight: 100
---

L'API **deleteFile** supprime le fichier spécifié du stockage cloud, vous permettant ainsi de gérer efficacement vos ressources et vos données.

## **API Excel : suppression de fichier**

### API Web

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                                                      |
| :---------------- | :----- | :---------- | :----------------------------------------------------------------------------------------------- |
| `path`            | string | Path        | Le chemin URL-encodé vers le fichier à supprimer.                                               |
| `storageName`     | string | Query       | Le nom du stockage où réside le fichier. Omettez ce paramètre si le stockage par défaut est utilisé. |
| `versionId`       | string | Query       | Identifiant de la version spécifique du fichier à supprimer. Si omis, la version la plus récente est supprimée. |

### Description de la réponse

Une requête réussie renvoie **HTTP 200** avec un corps de réponse vide. Aucune charge utile JSON n’est renvoyée.

```json
{}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                        |
| ---- | -------------------------- | ------------------------------------------------------------------ |
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT non valide ou manquant.                                  |
| 413  | Charge utile trop grande   | Le fichier envoyé dépasse la taille limite.                        |
| 500  | Erreur interne du serveur  | Erreur inattendue du serveur.                                      |

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) définit une interface de programmation publiquement accessible et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer VOTRE_JETON_D_ACCÈS" \
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

### Utilisation des SDK Aspose.Cells Cloud

L'utilisation d'un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK.
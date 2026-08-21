---
title: "API Aspose.Cells Cloud Move File – Interface pour le déplacement rapide de fichiers dans le cloud"
second_title: "Document"
ArticleTitle: "Solution efficace de gestion des fichiers Excel basée sur le cloud – Interface pour le déplacement rapide de fichiers dans le cloud"
linktitle: "Déplacer un fichier"
type: docs
url: /move-file/
keywords: "Aspose.Cells, API Move File, Stockage cloud, API Excel, Gestion de fichiers"
description: "Comment déplacer des fichiers entre dossiers dans le stockage Aspose.Cells Cloud à l’aide de l’API Move File v4.0 – point de terminaison, paramètres, exemples et liens vers les SDK."
weight: 100
---

L’API **moveFile** permet de déplacer un fichier d’un emplacement à un autre au sein du stockage Aspose.Cells Cloud. Elle vous aide à organiser vos fichiers et à gérer efficacement l’espace de stockage.

## **API Excel : Déplacer un fichier**

### API Web

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Les paramètres de la requête de l’API **moveFile** sont les suivants

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                    |
| ---------------- | ------ | ------------------------------------------------------ | -------------------------------------------------------------- |
| srcPath          | String | Chemin                                                 | Le chemin source du fichier à déplacer.                        |
| destPath         | String | Chaîne de requête                                       | Le chemin de destination vers lequel le fichier sera déplacé. |
| srcStorageName   | String | Chaîne de requête                                       | Le nom du stockage source, le cas échéant.                    |
| destStorageName  | String | Chaîne de requête                                       | Le nom du stockage de destination, le cas échéant.            |
| versionId        | String | Chaîne de requête                                       | L’identifiant de version du fichier, le cas échéant.          |

### **Réponse**

Une requête réussie renvoie **HTTP 200 OK** accompagné d’un corps JSON vide.

```json
{}
```

**Codes de statut HTTP**

| Code HTTP | Statut HTTP           | Description                                                                      |
| --------- | --------------------- | -------------------------------------------------------------------------------- |
| 200       | OK                    | L’API Web a été appelée avec succès ; la réponse contient les détails de l’opération. |
| 400       | Bad Request           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401       | Unauthorized          | Jeton JWT invalide ou manquant.                                                  |
| 413       | Payload Too Large     | Le fichier téléchargé dépasse la taille maximale autorisée.                    |
| 500       | Internal Server Error | Erreur interne du serveur inattendue.                                           |

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/MoveFile) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels vers l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

---
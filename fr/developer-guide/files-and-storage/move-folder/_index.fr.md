---
title: "API Aspose.Cells Cloud Move Folder – Déplacer rapidement des dossiers dans le cloud"
second_title: "Document"
ArticleTitle: "Gestion des fichiers Excel basée sur le cloud – Déplacer rapidement des dossiers dans le cloud"
linktitle: "Déplacer un dossier"
type: docs
url: /fr/move-folder/
keywords: "Aspose.Cells, Déplacer un dossier, Stockage cloud, API Excel"
description: "Découvrez comment déplacer des dossiers dans le stockage Aspose.Cells Cloud via l'API RESTful Move Folder. Inclut l'endpoint, les paramètres, un exemple cURL, les codes d’erreur et des exemples de SDK pour C#, Java, Python, etc."
weight: 100
---

Cette API permet de déplacer un dossier d’un emplacement à un autre dans le stockage Aspose.Cells Cloud. Elle facilite l’organisation des fichiers et la gestion efficace du stockage cloud.

## **API Excel : Déplacer un dossier**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**Exemple de requête cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête de l’API **moveFolder**

| Nom du paramètre | Type   | Emplacement | Description                                                       |
| ---------------- | ------ | ----------- | ----------------------------------------------------------------- |
| srcPath          | string | Path        | Chemin complet du dossier à déplacer, par ex. `FolderA/`.        |
| destPath         | string | Query       | Chemin cible vers lequel le dossier sera déplacé, par ex. `FolderB/`. |
| srcStorageName   | string | Query       | (Facultatif) Nom du stockage source.                             |
| destStorageName  | string | Query       | (Facultatif) Nom du stockage de destination.                     |

**Détails des paramètres**

- **srcPath** – obligatoire. Chemin du dossier source.
- **destPath** – obligatoire. Chemin du dossier de destination.
- **srcStorageName** – facultatif. Identifiant du stockage source.
- **destStorageName** – facultatif. Identifiant du stockage de destination.

### **Réponse**

En cas de succès, l’API renvoie un corps de réponse vide avec le code d’état HTTP **200 OK**. Les erreurs sont renvoyées sous forme d’objets JSON contenant un champ `error`.

**Codes d’état HTTP**

| Code HTTP | Statut HTTP           | Description                                                       |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | OK                    | L’API Web a été appelée avec succès ; la réponse contient les détails de l’opération. |
| 400       | Mauvaise requête      | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401       | Non autorisé          | Jeton JWT non valide ou manquant.                                |
| 413       | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.           |
| 500       | Erreur interne du serveur | Erreur serveur inattendue.                                      |

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment passer des appels à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment passer des appels aux services web Aspose.Cells à l’aide de divers SDK :

---
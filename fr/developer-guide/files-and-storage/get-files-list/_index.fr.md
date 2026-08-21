---
title: "Aspose.Cells Cloud API – Obtenir la liste des fichiers (contenu d’un dossier)"
description: "Récupérer la liste des fichiers et des sous-dossiers à partir d’un dossier spécifique du stockage cloud Aspose.Cells."
keywords:
  - Aspose.Cells
  - API
  - Obtenir la liste des fichiers
  - Stockage cloud
  - Excel
  - REST
type: docs
weight: 100
---

L’opération **Obtenir la liste des fichiers** renvoie la collection de fichiers et de sous-dossiers stockés dans un dossier spécifié du stockage cloud Aspose.Cells.  
Elle constitue le point d’entrée principal pour parcourir les classeurs Excel, les archives et autres types de fichiers pris en charge hébergés dans le cloud.

## Aspose.Cells Cloud API – Obtenir la liste des fichiers (contenu d’un dossier)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom               | Emplacement | Type    | Obligatoire | Description                                                              |
| ----------------- | ----------- | ------- | ----------- | ------------------------------------------------------------------------ |
| **path**          | Chemin      | string  | Oui         | Chemin vers le dossier dans le stockage cloud.                          |
| **storageName**   | Requête     | string  | Non         | Nom du stockage à utiliser. Si omis, le stockage par défaut est utilisé.|
| **pageSize**      | Requête     | integer | Non         | Nombre maximum d’éléments à renvoyer par page (par défaut : 100).        |
| **pageNumber**    | Requête     | integer | Non         | Numéro de la page à récupérer (commence à 1, par défaut : 1).            |

- **Valeur** – Tableau d’objets `StorageFile`. Chaque objet contient :
  - `Name` – Nom du fichier ou du dossier.
  - `IsFolder` – `true` si l’entrée correspond à un dossier.
  - `Size` – Taille en octets (les dossiers renvoient `0`).
  - `ModifiedDate` – Horodatage de la dernière modification (au format ISO 8601).

### **Réponse**

**Codes de statut HTTP**

| Code HTTP | Statut HTTP           | Description                                                          |
| --------- | --------------------- | -------------------------------------------------------------------- |
| 200       | OK                    | L’API web a été appelée avec succès ; la réponse contient les détails de l’opération. |
| 400       | Mauvaise requête      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401       | Non autorisé          | Jeton JWT invalide ou manquant.                                      |
| 413       | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.                     |
| 500       | Erreur interne du serveur | Erreur serveur inattendue.                                          |

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

---
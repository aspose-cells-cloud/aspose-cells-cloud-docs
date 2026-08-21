---
title: "API Aspose.Cells Cloud de téléchargement de fichier – Une interface pour le téléchargement rapide de fichiers dans le cloud"
second_title: "Document"
ArticleTitle: "API Aspose.Cells Cloud de téléchargement de fichier – Une interface pour le téléchargement rapide de fichiers dans le cloud"
linktitle: "Télécharger un fichier"
type: docs
url: /upload-file/
keywords: "Aspose.Cells, téléchargement de fichier, API Excel, stockage cloud, API REST"
description: "Guide de téléchargement de fichiers à l’aide de l’API Aspose.Cells Cloud, couvrant les paramètres de requête, les codes d’état HTTP, la gestion des erreurs et des exemples de code."
weight: 100
---

L’**API uploadFile** permet aux développeurs de télécharger directement des fichiers vers un stockage cloud afin de les traiter avec Aspose Cells.

## **API Aspose Cells : Télécharger un fichier**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Les paramètres de la requête de l’API **uploadFile** sont les suivants :

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                   |
| :--------------- | :----- | :---------------------------------------------------- | :-------------------------------------------------------------------------------------------- |
| UploadFiles      | Fichier | FormData                                             | Télécharger des fichiers vers le stockage cloud.                                             |
| path             | Chaîne  | Chemin                                               | Le chemin de destination dans le stockage cloud. Indiquez l’emplacement où le fichier doit être téléversé. |
| storageName      | Chaîne  | Chaîne de requête                                    | Le nom du stockage dans lequel le fichier sera téléversé.                                    |

### **Réponse**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["Résultat du téléchargement de fichier"],
  "Type": "Classe",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["Liste des noms de fichiers téléchargés"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["Liste des erreurs."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

L’API renvoie les codes d’état HTTP suivants :

| Code d’état                   | Description                                         |
| ----------------------------- | --------------------------------------------------- |
| **200 OK**                    | Fichier téléchargé avec succès.                    |
| **400 Bad Request**           | Paramètres invalides ou requête mal formée.        |
| **401 Unauthorized**          | Jeton d’authentification manquant ou invalide.     |
| **403 Forbidden**             | Permissions insuffisantes pour le stockage spécifié. |
| **500 Internal Server Error** | Erreur serveur inattendue.                         |

## Comment utiliser l’API de téléchargement de fichier avec les SDK ?

### Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) fournit une description détaillée de l’API, permettant aux développeurs d’interagir directement avec celle-ci via un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK améliore l’efficacité du développement en gérant les détails de bas niveau, permettant ainsi aux développeurs de se concentrer sur les tâches de leur projet. Visitez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**Voir aussi**

- [API de téléchargement de fichier](/download-file/) – Récupérer un fichier depuis le stockage cloud.
- [API de copie de fichier](/copy-file/) – Dupliquer un fichier dans le stockage cloud.
- [API de suppression de fichier](/delete-file/) – Supprimer un fichier du stockage cloud.

---
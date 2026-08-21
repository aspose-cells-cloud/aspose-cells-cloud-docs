---
title: "Supprimer les métadonnées des fichiers Excel"
second_title: "Document"
linktitle: "Suppression sans utiliser le stockage"
type: docs
url: /metadata/delete/
keywords: "Aspose.Cells, suppression des métadonnées, API Excel, propriétés du classeur"
description: "Supprimer les métadonnées du classeur (auteur, titre, données personnalisées) via l'API Aspose.Cells Cloud. Inclut l'endpoint, l'authentification, les paramètres, ainsi que des exemples cURL et SDK."
weight: 55
ArticleTitle: "Supprimer les métadonnées des fichiers Excel – Documentation Aspose.Cells Cloud"
---

**Vue d'ensemble**  
L'opération *Supprimer les métadonnées* supprime définitivement toutes les propriétés du classeur (standard et personnalisées) à partir du(s) fichier(s) Excel téléchargé(s) et renvoie le(s) fichier(s) traité(s) dans la réponse.

**Prérequis**  
- Un jeton JWT valide Aspose.Cells Cloud (obtenible via le flux d’authentification OAuth 2.0).  
- Version de l’API **v3.0** (l’endpoint utilisé dans cet exemple).  
- Pour l’utilisation des SDK, installez le SDK Aspose.Cells Cloud adapté à votre langage (par exemple via NuGet, Maven, npm, pip, CPAN ou les modules Go).

Cette API REST supprime les **métadonnées** d’un ou plusieurs fichiers Excel. Elle supprime les propriétés du classeur telles que l’auteur, le titre et les données personnalisées, puis renvoie les fichiers nettoyés.

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                               |
| ---------------- | ------ | ----------- | --------------------------------------------------------- |
| file             | fichier | formData    | Fichier Excel à télécharger pour la suppression des **métadonnées** |
| type             | chaîne  | query       | Type d’opération ; définir sur **all** pour supprimer toutes les **métadonnées** |

La <a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">Spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels vers l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "file=@fichier1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "fichier1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

Les **réponses d’erreur** peuvent inclure :

- **400 Bad Request** – fichier manquant ou valeur `type` invalide.
- **401 Unauthorized** – jeton JWT invalide ou manquant.
- **500 Internal Server Error** – erreur de traitement côté serveur.

L’API renvoie un objet JSON contenant un champ `Error` avec les détails correspondants dans chaque cas.

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | Métadonnées supprimées, fichier renvoyé |
| 400  | Bad Request   | Fichier manquant ou `type` invalide |
| 401  | Unauthorized  | Jeton JWT invalide ou manquant |
| 500  | Internal Server Error | Échec du traitement côté serveur |

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur vos tâches de projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
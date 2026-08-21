---
title: "API Aspose.Cells Cloud de téléchargement de fichier – Interface pour un téléchargement rapide de fichiers dans le cloud"
second_title: "Document"
ArticleTitle: "API Aspose.Cells Cloud de téléchargement de fichier – Interface pour un téléchargement rapide de fichiers dans le cloud"
linktype: "Téléchargement de fichier API"
type: docs
url: /download-file/
keywords: "Aspose.Cells, API de téléchargement de fichier, stockage cloud Excel, API REST, téléchargement de fichier, PDF, CSV, SDK"
description: "Téléchargez des fichiers Excel, PDF, CSV et autres à partir du stockage cloud Aspose.Cells à l’aide de l’API de téléchargement de fichier (v4.0). Inclut le point de terminaison, les paramètres, les détails d’authentification et des exemples de code."
weight: 100
---

L’**API DownloadFile** vous permet de récupérer des fichiers stockés dans le stockage cloud Aspose.Cells. L’API de téléchargement de fichier est essentielle pour accéder directement depuis le cloud aux feuilles de calcul Excel, aux fichiers PDF, aux fichiers CSV et aux autres formats pris en charge.

## **API Excel : Téléchargement de fichier**

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête de l’API **DownloadFile**

| Nom du paramètre | Type   | Emplacement (Chemin / Requête) | Description                                                    |
| ---------------- | ------ | ------------------------------ | -------------------------------------------------------------- |
| path             | String | Chemin                         | Le chemin virtuel vers le fichier que vous souhaitez télécharger. |
| storageName      | String | Requête                        | Le nom du stockage à partir duquel le fichier sera récupéré. |
| versionId        | String | Requête                        | L’identifiant de version du fichier à télécharger, le cas échéant. |

### **Réponse**

L’API renvoie un **flux binaire de fichier**. L’en-tête `Content-Type` correspond au format du fichier (par exemple, `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` pour XLSX). Aucune charge utile JSON n’est renvoyée.

**Codes de statut HTTP**

| Code | Signification           | Description                                                     |
| ---- | ----------------------- | --------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.             |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                   |

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer VOTRE_JETON_D_ACCÈS" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}
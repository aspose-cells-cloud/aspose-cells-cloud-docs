---
title: "Ajouter une image d'arrière-plan à un classeur"
second_title: "Document"
linktitle: "Ajouter"
type: docs
url: /fr/add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, ajouter une image d'arrière-plan, API Excel, REST, SDK cloud, cURL, arrière-plan du classeur"
description: "Découvrez comment ajouter une image d'arrière-plan à un classeur Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut les paramètres requis, les détails d'authentification, un exemple complet en cURL et des informations sur la gestion des erreurs."
weight: 160
---

## API REST

Cette API REST ajoute une **image d'arrière-plan** à un classeur Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.


### Paramètres de requête

| Nom du paramètre | Type   | Description                                                |
| ---------------- | ------ | ---------------------------------------------------------- |
| `picPath`        | string | Chemin du fichier image à utiliser comme arrière-plan.    |
| `folder`         | string | Dossier contenant le classeur original.                   |
| `storageName`    | string | Nom du stockage où se trouve le fichier.                 |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description                                            |
| ---------------- | ---- | ------------------------------------------------------ |
| `datafile`       | file | Fichier du classeur auquel l'arrière-plan sera appliqué. |

**Paramètre de chemin** – `{name}` dans l’URL représente le **nom du fichier du classeur** (par exemple, `Book1.xlsx`).


### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                            |
| 413  | Charge utile trop grande    | Fichier téléchargé dépassant la limite de taille.         |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                          |

## Comment utiliser l’API PutWorkbookBackground avec les SDK

### Spécification de l’API PutWorkbookBackground

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) définit une interface de programmation accessible publiquement qui permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre une requête complète, incluant l’indicateur de téléchargement de fichier multipart et l’en-tête d’authentification requis.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Utiliser les SDK Aspose.Cells Cloud

Utiliser un SDK est le moyen le plus rapide de développer. Un SDK abstractise les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}

---
---
title: "Supprimer l'arrière-plan d'un classeur Excel"
second_title: "Document"
linktitle: "Supprimer"
type: docs
url: /fr/delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells supprimer l'arrière-plan, API Excel supprimer l'arrière-plan, Aspose.Cells Cloud, DELETE /cells background"
description: "Supprimer une image d’arrière-plan d’un classeur Excel à l’aide de l’API Aspose.Cells Cloud. Découvrez le point de terminaison DELETE, les paramètres requis, l’exemple cURL et le code SDK en C#, Java, Python, etc."
weight: 170
ArticleTitle: "Supprimer l’image d’arrière-plan d’un classeur Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cet API REST supprime l’image d’arrière-plan d’un classeur Excel.

## API DeleteWorkbookBackground

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de requête**

| Nom du paramètre | Type   | Description                                         | Obligatoire |
| ---------------- | ------ | --------------------------------------------------- | ----------- |
| folder           | string | Dossier contenant le classeur d’origine.           | Non         |
| storageName      | string | Nom du service de stockage à utiliser.             | Non         |

### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                     |
|------|-----------------------------|-----------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                              |

## Comment utiliser l’API DeleteWorkbookBackground à l’aide des SDK

### Spécification de l’API DeleteWorkbookBackground

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation publiquement accessible qui permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre une requête DELETE complète avec l’en-tête d’authentification requis ; aucun corps de requête n’est nécessaire.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
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

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
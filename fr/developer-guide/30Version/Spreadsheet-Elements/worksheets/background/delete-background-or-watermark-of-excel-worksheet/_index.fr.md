---
title: "Supprimer l’arrière-plan d’une feuille de calcul Excel"
second_title: "Document"
linktitle: "Supprimer"
type: docs
url: /fr/worksheets/background/delete/
aliases: [  /fr/delete-background-or-watermark-of-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Supprimer l’arrière-plan d’une feuille de calcul, Excel, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Utilisez l’API REST Aspose.Cells Cloud pour supprimer l’image d’arrière-plan d’une feuille de calcul Excel. Des SDK sont disponibles pour C#, Java, PHP, Ruby, Node.js, Python, Perl et Go."
weight: 210
ArticleTitle: "Supprimer l’arrière-plan d’une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cet API REST supprime l’image d’arrière-plan d’une feuille de calcul.

**Prérequis :** Vous devez avoir le classeur stocké dans le stockage Aspose Cloud et posséder un jeton d’accès JWT valide pour l’authentification.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                            |
| ---------------- | ------ | ----------- | ------------------------------------------------------ |
| name             | string | path        | Le nom du fichier Excel.                              |
| sheetName        | string | path        | Le nom de la feuille de calcul dont l’arrière-plan est supprimé. |
| folder           | string | query       | Le dossier dans le stockage où le fichier est situé. |
| storageName      | string | query       | Le nom du stockage (si ce n’est pas le stockage par défaut). |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. Toutes les requêtes nécessitent un jeton JWT valide. Obtenez le jeton via le point de terminaison OAuth2, comme décrit dans le guide d’authentification.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande      | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue. |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

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
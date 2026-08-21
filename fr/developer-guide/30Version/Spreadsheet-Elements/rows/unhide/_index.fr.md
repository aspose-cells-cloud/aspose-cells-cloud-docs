---
title: "Afficher des lignes masquées sur une feuille Excel"
second_title: "Document"
linktitle: "Afficher"
type: docs
url: /fr/rows/unhide/
aliases: [  /fr/unhide-rows-in-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, afficher des lignes, API REST, classeur, .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl, Swift, API REST Aspose.Cells Cloud"
description: "Utilisez l’API REST Aspose.Cells Cloud pour afficher des lignes masquées sur une feuille Excel. L’API est accessible via plusieurs SDK tels que .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl et Swift."
weight: 50
ArticleTitle: "Afficher des lignes masquées sur une feuille Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST affiche des lignes masquées sur une feuille Excel.

**Prérequis :** Obtenez un jeton d’accès JWT valide auprès du service d’authentification Aspose Cloud et assurez-vous que le classeur cible a été téléchargé vers un espace de stockage pris en charge avant d’appeler ce point de terminaison.

## API PostUnhideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/unhide
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                           |
| ---------------- | ------- | ----------- | ----------------------------------------------------- |
| name             | string  | path        | Nom du classeur.                                      |
| sheetName        | string  | path        | Nom de la feuille de calcul.                          |
| startrow         | integer | query       | Index de la première ligne à afficher (à partir de 0).|
| totalRows        | integer | query       | Nombre de lignes à afficher.                          |
| height           | number  | query       | Hauteur de ligne (par défaut : 15,0).                 |
| folder           | string  | query       | Dossier contenant le document.                        |
| storageName      | string  | query       | Nom de l’espace de stockage.                          |

La <a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetRows" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

**Authentification**  
Toutes les requêtes doivent être authentifiées à l’aide d’un jeton d’accès JWT obtenu auprès du service d’authentification Aspose Cloud. Incluez ce jeton dans l’en-tête `Authorization: Bearer <jeton JWT>`.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/unhide?startrow=1&totalRows=1&height=15" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jeton JWT>"
# Remarque : le corps de la requête POST est vide pour ce point de terminaison
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

**Codes de statut HTTP**

| Code | Signification               | Description                                                  |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                              |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.           |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                   |

Pour un dépannage détaillé, consultez le [guide de gestion des erreurs](/error-handling/).

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur vos tâches de projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
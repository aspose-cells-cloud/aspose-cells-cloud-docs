---
title: "Mettre à jour une image dans un fichier Excel"
second_title: "Document"
linktitle: "Mettre à jour"
type: docs
url: /fr/pictures/update/
aliases: [  /fr/update-a-specific-picture-from-excel-workshee/ ]
keywords: "Aspose.Cells Cloud, Excel, Mettre à jour une image, API REST, SDK"
description: "Découvrez comment mettre à jour une image dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails de la requête, un exemple cURL et des extraits de code SDK pour plusieurs langages."
ArticleTitle: "Mettre à jour une image dans un fichier Excel à l’aide de l’API REST Aspose.Cells Cloud"
weight: 70
---

Cette API REST met à jour une image, identifiée par son index, dans une feuille de calcul Excel.

**Prérequis :** Vous devez disposer d’un jeton JWT Aspose Cloud valide, du fichier Excel cible stocké dans votre espace de stockage Aspose Cloud, et utiliser la version 3.0 ou ultérieure de l’API.

## API PostWorksheetPicture

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                     |
| ---------------- | ------- | ----------- | --------------------------------------------------------------- |
| name             | string  | path        | Le nom du fichier Excel.                                        |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant l’image.              |
| pictureIndex     | integer | path        | Index de base zéro de l’image à mettre à jour.                  |
| picture          | object  | body        | Objet JSON décrivant les propriétés de l’image à mettre à jour. |
| folder           | string  | query       | Le dossier dans lequel le document est stocké.                 |
| storageName      | string  | query       | Le nom du service de stockage.                                  |

**Remarque :** L’index de l’image est de base zéro. Les formats d’image pris en charge incluent JPEG, PNG, BMP et GIF. La taille maximale d’une image est de 10 Mo.

### Réponses d’erreur

| Code HTTP | Description                                                        |
| --------- | ------------------------------------------------------------------ |
| 401       | Non autorisé – jeton manquant ou non valide.                      |
| 404       | Non trouvé – le fichier, la feuille de calcul ou l’index d’image spécifié n’existe pas. |
| 400       | Requête incorrecte – syntaxe de requête mal formée ou paramètres invalides. |
| 500       | Erreur interne du serveur – une condition inattendue est survenue. |

La <a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">Spécification OpenAPI</a> définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*Voir aussi :* Ajouter une image, Supprimer une image, Obtenir une image, Effacer les images – autres opérations liées aux images dans l’API Aspose.Cells Cloud.
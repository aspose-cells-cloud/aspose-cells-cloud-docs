---
title: "Ajouter une image à un fichier Excel"
second_title: "Document"
linktitle: "Ajouter"
type: docs
url: /fr/pictures/add/
aliases: [  /fr/add-pictures-to-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, ajouter une image, API REST"
description: "Utilisez l'API REST Aspose.Cells Cloud pour ajouter une image à une feuille de calcul Excel. Les SDK pour Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift simplifient l'intégration multiplateforme."
weight: 20
ArticleTitle: "Ajouter une image à une feuille de calcul Excel – Aspose.Cells Cloud API"
---

Cette API REST ajoute une nouvelle image à une feuille de calcul Excel.  
**Prérequis :** Vous devez posséder un jeton d'authentification Aspose Cloud valide, un classeur existant stocké dans un support pris en charge, ainsi que les autorisations appropriées pour modifier la feuille de calcul.

## API PutWorksheetAddPicture

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                                   |
| ---------------- | ------- | ----------- | --------------------------------------------------------------------------------------------- |
| name             | string  | chemin     | Nom du classeur.                                                                              |
| sheetName        | string  | chemin     | Nom de la feuille de calcul.                                                                  |
| picture          | object  | corps      | Objet image (données binaires).                                                               |
| upperLeftRow     | integer | requête    | Indice de ligne (à partir de zéro) du coin supérieur gauche où l’image sera placée.          |
| upperLeftColumn  | integer | requête    | Indice de colonne (à partir de zéro) du coin supérieur gauche où l’image sera placée.        |
| lowerRightRow    | integer | requête    | Indice de ligne (à partir de zéro) du coin inférieur droit de la zone d’image.               |
| lowerRightColumn | integer | requête    | Indice de colonne (à partir de zéro) du coin inférieur droit de la zone d’image.             |
| picturePath      | string  | requête    | Chemin vers le fichier image ; si omis, les données d’image doivent être fournies dans le corps de la requête. |
| folder           | string  | requête    | Dossier contenant le classeur.                                                                |
| storageName      | string  | requête    | Nom du service de stockage.                                                                   |

**Remarque concernant le corps de la requête :** Lorsque `picturePath` est omis, envoyez les données binaires de l’image dans le corps de la requête en utilisant `multipart/form-data`.

### Codes de statut HTTP

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille maximale autorisée.                |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                               |

**Exemple de schéma de réponse 200**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**Remarque :** La taille maximale autorisée pour une image est de 10 Mo ; les fichiers plus volumineux seront rejetés avec une réponse `400 Bad Request`.

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
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

L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Remarque :** Les formats d’image pris en charge incluent PNG, JPEG, BMP et GIF. La taille maximale autorisée pour une image est de 10 Mo ; les fichiers plus volumineux seront rejetés avec une réponse `400 Bad Request`.
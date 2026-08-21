---
title: "Excel vers TIFF"
second_title: "Document"
linketitle: "Excel vers TIFF"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/, /convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud, conversion Excel vers TIFF, API REST, cURL, SDK, .NET, Java, Python, export d’image"
description: "Découvrez comment convertir des classeurs Excel en images TIFF de haute qualité à l’aide de l’API Aspose.Cells Cloud. Commandes cURL détaillées, exemples de SDK (C#, Java, Python, etc.), étapes d’authentification et gestion des erreurs."
weight: 90
---

Les points de terminaison **Convert**, **SaveAs** et **Export** d’Aspose.Cells Cloud vous permettent de transformer un classeur Excel en image TIFF.  
Vous pouvez appeler ces points de terminaison directement via **cURL** ou à l’aide d’un des SDK pris en charge.

## API REST

| **API**                | **Méthode** | **Objectif**                                                                                              | **Lien Swagger**                                                                            |
| ---------------------- | ----------- | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT         | Convertit un classeur fourni dans le corps de la requête vers le format spécifié (TIFF).                | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET         | Exporte le classeur nommé vers un autre format (TIFF) et renvoie le résultat dans la réponse.           | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST        | Enregistre le classeur dans le format choisi (TIFF) et stocke le résultat dans le stockage cloud.      | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

Ces points de terminaison sont accessibles publiquement et peuvent être appelés directement depuis un navigateur web ou tout client HTTP.

### Exemples cURL

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<contenu-base64>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}
{{< /tabs >}}

> **Remarque :**
>
> - Le corps de la requête **Convert** doit contenir le fichier (ou une référence à un fichier stocké) ainsi que le `SaveFormat` souhaité.
> - La requête **Export** ne nécessite pas de corps de requête ; le format est fourni via la chaîne de requête (`format=tiff`).

## Gestion des erreurs

| **Code d’état** | **Signification**     | **Cause typique**                           |
| ----------------- | --------------------- | ------------------------------------------- |
| 200             | Succès                | L’image TIFF est renvoyée (flux binaire). |
| 400             | Requête incorrecte    | Paramètres manquants ou mal formés.        |
| 401             | Non autorisé          | Jeton JWT invalide ou manquant.            |
| 404             | Introuvable           | Le classeur spécifié n’existe pas.         |
| 500             | Erreur interne du serveur | Condition inattendue côté serveur.        |

En cas d’erreur, l’API renvoie une charge utile JSON contenant `Code`, `Message` et éventuellement `Description`.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
title: "Convertir Excel en Markdown"
second_title: "Document"
linktitle: "Excel vers Markdown"
type: docs
url: /convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, conversion, Aspose.Cells Cloud, API REST, conversion Excel vers Markdown, API Markdown Aspose Cells, export Excel vers Markdown"
description: "Convertir des feuilles Excel en Markdown à l’aide de l’API REST Aspose.Cells Cloud – inclut un exemple cURL, des extraits de code SDK, les paramètres requis et les détails d’authentification."
weight: 100
ArticleTitle: "Convertir Excel en Markdown – Documentation de l’API Aspose.Cells Cloud"
---

Cette API REST convertit un fichier de feuille de calcul au format Markdown.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de requête


| Nom du paramètre      | Type   | Emplacement | Description                                                                                                     |
| --------------------- | ------ | ----------- | --------------------------------------------------------------------------------------------------------------- |
| password              | string | query       | Mot de passe nécessaire pour ouvrir le fichier Excel.                                                          |
| storageName           | string | query       | Nom du stockage où le fichier est situé.                                                                       |
| checkExcelRestriction | bool   | query       | Indique s’il faut appliquer des restrictions spécifiques à Excel lors de la modification de cellules ou d’objets associés. |
| datafile              | file   | body        | Le fichier Excel à uploader comme première partie du contenu multipart.                                        |

### Réponse

L’API renvoie un objet JSON de type **FileInfo** :

- **FileInfo** – objet contenant le nom, la taille et le contenu encodé en base64 du fichier Markdown généré.

```json
{
  "Filename": "exemple.md",
  "FileSize": 12345,
  "FileContent": "chaine_encodée_en_base64"
}
```

### Réponses d’erreur

| Code HTTP | Description                                                           | Corps JSON d’exemple                            |
| --------- | --------------------------------------------------------------------- | ----------------------------------------------- |
| 401       | Non autorisé – jeton manquant ou invalide.                           | `{"error":"Jeton d'accès invalide."}`          |
| 400       | Mauvaise requête – paramètres requis manquants ou format de fichier invalide. | `{"error":"Le champ 'datafile' est requis."}` |
| 500       | Erreur interne du serveur – problème inattendu sur le serveur.       | `{"error":"Une erreur inattendue est survenue."}` |



## Comment utiliser l’API PostConvertWorkbookToMarkdown avec les SDK

### Spécification de l’API PostConvertWorkbookToMarkdown

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <jeton_d'accès>" \
     -F "File=@votre_fichier_excel.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "exemple.md",
  "FileSize": 12345,
  "FileContent": "chaine_encodée_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Autres API implémentant cette fonctionnalité

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Enregistre un fichier Excel au format HTML avec des paramètres supplémentaires et stocke le résultat.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convertit un fichier Excel en HTML avec des options supplémentaires et renvoie le résultat dans la réponse.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Récupère un fichier Excel et peut le convertir en HTML avec des paramètres optionnels.
---
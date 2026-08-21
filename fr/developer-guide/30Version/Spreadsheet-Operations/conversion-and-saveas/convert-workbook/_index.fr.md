---
title: "Convertir un fichier Excel en différents formats"
second_title: "Document"
linktitle: "Convertir un classeur"
type: docs
url: /fr/convert-a-spread-file-to-different-formats/
keywords: "conversion Excel, conversion de classeur, Aspose.Cells Cloud, API REST, PDF, CSV, JSON, Markdown, conversion de format de fichier"
description: "Utilisez l’API REST Aspose.Cells Cloud pour convertir des classeurs Excel en divers formats tels que PDF, CSV, JSON et Markdown. L’API prend en charge plusieurs SDK pour des langages tels que C#, Java, Python, et plus encore."
weight: 10
ArticleTitle: "Convertir un fichier Excel en différents formats – Guide de l’API Aspose.Cells Cloud"
---

Cet API REST permet de convertir un fichier Excel dans un autre format. Il prend en charge un large éventail de formats de sortie et vous permet de définir les options de configuration de page et d’enregistrement avant la conversion.

## API PostConvertWorkBook

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

Avant d’utiliser cette API, assurez-vous de disposer d’un jeton JWT valide et d’avoir installé le SDK Aspose.Cells Cloud approprié pour votre langage de programmation.

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## Comment utiliser l’API PostConvertWorkBook avec les SDK

### Spécification de l’API PostConvertWorkBook

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer. Un SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
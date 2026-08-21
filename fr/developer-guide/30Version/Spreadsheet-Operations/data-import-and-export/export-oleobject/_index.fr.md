---
title: "Exporter un objet OLE – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Objet OLE"
type: docs
url: /export-excel-ole-object/
aliases: [/export/excel-ole-object/]
keywords: "Aspose.Cells, objet OLE, exportation, Excel, API cloud, PDF, PNG, DOCX, PPTX"
description: "Exporter des objets OLE à partir d’un classeur Excel à l’aide de l’API Aspose.Cells Cloud. Découvrez le format de requête, les paramètres, un exemple cURL et la gestion des erreurs."
weight: 20
ArticleTitle: "Exporter un objet OLE – Aspose.Cells Cloud API"
---

## **API REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.


### Paramètres de la requête

| Paramètre       | Emplacement   | Type   | Obligatoire | Description                                                                      |
| --------------- | ------------- | ------ | ----------- | -------------------------------------------------------------------------------- |
| `file`          | Données de formulaire | fichier | Oui         | Le classeur Excel (`.xlsx`, `.xls`, etc.) contenant les objets OLE.             |
| `outputFormat`  | Requête       | chaîne  | Oui         | Format cible des objets exportés (`pdf`, `png`, `jpeg`, `docx`, `pptx`).        |
| `objectType`    | Requête       | chaîne  | Oui         | Valeur fixe `oleobject`.                                                        |


### Réponse

Une requête réussie renvoie un objet JSON listant les fichiers exportés :

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                               |
|------|-----------------------------|---------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                                         |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.                      |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                             |

## Comment utiliser l’API PostExport à l’aide des SDK

### Spécification de l’API PostExport

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### Qu’est-ce qu’un objet OLE ?

Un **objet OLE (Object Linking and Embedding)** intégrera du contenu externe — tel que des documents Word, des diapositives PowerPoint, des images ou d’autres fichiers — à l’intérieur d’un classeur Excel. Lors de l’exportation, le contenu intégré est extrait et enregistré dans le format de sortie demandé.

### Aperçu du point de terminaison

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – Doit être défini sur `oleobject`.
- `format` – Format de sortie souhaité (par exemple, `pdf`, `png`, `jpeg`, `docx`, `pptx`).

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---
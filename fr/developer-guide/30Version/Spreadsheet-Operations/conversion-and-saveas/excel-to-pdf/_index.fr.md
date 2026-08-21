---
title: "Convertir Excel en PDF – API Aspose.Cells Cloud"
ArticleTitle: "Convertir Excel en PDF – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "Convertir Excel en PDF"
type: docs
url: /fr/convert-excel-file-to-pdf-file/
aliases: [  /fr/convert-excel-file-to-pdf-in-cloud/ , /fr/convert/excel-to-pdf/ ]
keywords: "Aspose, Cells, Excel, PDF, conversion, API Cloud"
description: "Découvrez comment convertir des classeurs Excel en PDF à l'aide de l'API REST Aspose.Cells Cloud. Inclut des exemples cURL et SDK (C#, Java, Python) ainsi qu'un guide d'authentification."
weight: 80
---

Cette API REST convertit un fichier de feuille de calcul au format PDF. **Prérequis :** Obtenez un jeton d’accès JWT valide, assurez-vous que le fichier Excel source est stocké dans un espace de stockage pris en charge, et disposez des autorisations appropriées pour appeler le point de terminaison de conversion.

## API PostConvertWorkbookToPDF

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètre de requête**

| Nom du paramètre      | Type   | Description                                                                   |
| :-------------------- | :----- | :---------------------------------------------------------------------------- |
| password              | string | Mot de passe permettant d’ouvrir le fichier Excel.                           |
| storageName           | string | Nom de l’espace de stockage dans lequel le fichier est situé.                |
| checkExcelRestriction | bool   | Indique s’il faut appliquer les restrictions du fichier Excel lors de la modification d’objets liés aux cellules. |

`checkExcelRestriction` vaut `false` par défaut si omis.

### **Paramètre du corps de la requête**

| Nom du paramètre | Type | Description                                                   |
| :--------------- | :--- | :------------------------------------------------------------ |
| datafile         | file | Fichier de données enregistré comme première partie du contenu multipart. |

### **Réponse**

[FileInfo](/cells/file-info/)

La réponse renvoie un objet JSON contenant les métadonnées du fichier. Le fichier PDF lui-même peut être téléchargé à l’aide du champ `FileContent` (encodé en base64) ou via le lien `FileInfo`. L’API renvoie un objet JSON de type **FileInfo** :

- **FileInfo** – objet contenant le nom, la taille et le contenu encodé en base64 du fichier **PDF** généré.

```json
{
  "Filename": "exemple.pdf",
  "FileSize": 12345,
  "FileContent": "chaîne_encodée_en_base64"
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                                   |
|------|-----------------------------|---------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                               |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille limite.             |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                 |

## Comment utiliser l’API PostConvertWorkbookToPDF à l’aide des SDK

### Spécification de l’API PostConvertWorkbookToPDF

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

**En-têtes de requête**

| En-tête         | Type   | Description                                               |
| :-------------- | :----- | :-------------------------------------------------------- |
| Authorization   | string | Jeton « bearer » obtenu via l’authentification JWT.      |
| Content-Type    | string | Doit être `multipart/form-data` pour l’envoi de fichiers. |
| Accept          | string | `application/json` pour recevoir les métadonnées de réponse. |

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. Incluez un jeton d’accès dans l’en-tête `Authorization`, puis exécutez la requête suivante :

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "Contenu du fichier : chaîne_encodée_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}


### Utiliser les SDK Aspose.Cells Cloud


L’utilisation d’un SDK simplifie le développement en gérant les détails de bas niveau. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Autres API implémentant cette fonctionnalité

| **API**        | **Type** | **Description**                                                 | **Lien Swagger**                                                                            |
| :------------- | :------- | :-------------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT      | Convertit un classeur du contenu de la requête vers un format spécifié. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

L’API [POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) permet d’enregistrer un fichier Microsoft Excel au format PDF avec des paramètres supplémentaires et de stocker le résultat dans l’espace de stockage.

Cette API REST convertit un fichier Excel en PDF.

L’API [PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) permet de convertir un fichier Microsoft Excel en PDF avec des paramètres supplémentaires et de renvoyer le résultat dans la réponse.

L’API [GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) permet de convertir un fichier Microsoft Excel en PDF avec des paramètres supplémentaires et de renvoyer le résultat dans la réponse.

Ces API [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) et [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) définissent une interface de programmation accessible publiquement et permettent d’effectuer des interactions REST directement depuis un navigateur web.

Pour d’autres options de conversion, consultez la page [Options d’enregistrement](/cells/save-options/).
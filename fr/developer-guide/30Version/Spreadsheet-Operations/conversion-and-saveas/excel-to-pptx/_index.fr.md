---
title: "Convertir un fichier Excel en fichier PPTX à l’aide de l’API Aspose.Cells Cloud v3.0"
second_title: "Document"
linktitle: "Excel vers PPTX"
type: docs
url: /fr/convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, conversion, API REST, cloud"
description: "Découvrez comment convertir des classeurs Excel en présentations PPTX à l’aide de l’API REST Aspose.Cells Cloud v3.0. Inclut une requête cURL, des exemples de code SDK, l’authentification et la gestion des erreurs."
weight: 90
ArticleTitle: "Convertir un fichier Excel en fichier PPTX à l’aide de l’API Aspose.Cells Cloud v3.0"
---

Cette API REST permet de convertir un fichier de feuille de calcul au format PPTX.

## API PostConvertWorkbookToPptx

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de requête

| Nom du paramètre        | Type   | Description                                                                                      |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------ |
| `password`              | string | Mot de passe requis pour ouvrir le classeur Excel.                                              |
| `storageName`           | string | Nom du stockage où se trouve le fichier source.                                                 |
| `checkExcelRestriction` | bool   | Indique s’il faut appliquer les restrictions des fichiers Excel lors de la modification d’objets liés aux cellules. |

### Paramètre du corps de la requête

| Nom du paramètre | Type        | Description                                                         |
| ---------------- | ----------- | ------------------------------------------------------------------- |
| `datafile`       | fichier de données | Le fichier Excel inclus dans la première partie du corps de requête multipart. |

**Exemple de corps de requête multipart (simplifié) :**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<contenu binaire de input.xlsx>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### Réponse

L’API renvoie un objet **FileInfo** contenant le fichier pptx généré.

| Champ             | Type   | Description                                           |
| ----------------- | ------ | ----------------------------------------------------- |
| **Filename**      | string | Nom du fichier pptx (par exemple, `exemple.pptx`).   |
| **FileSize**      | int    | Taille du fichier en octets.                          |
| **FileContent**   | string | Contenu du fichier pptx codé en Base64.              |

[FileInfo](/cells/file-info/)


**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                            |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille limite.                           |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                                 |

*Remarques :* Le point de terminaison prend en charge les formats Excel courants (`.xlsx`, `.xls`, `.xlsm`). La taille maximale du fichier est limitée à 50 Mo. La conversion peut être restreinte pour les classeurs contenant des macros ou des feuilles protégées, sauf si les paramètres appropriés sont fournis.

## Comment utiliser l’API PostConvertWorkbookToPptx avec les SDK

### Spécification de l’API PostConvertWorkbookToPptx

La <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST à partir d’un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "exemple.pptx",
  "FileSize": 123456,
  "FileContent": "Contenu du fichier : chaîne_encodée_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud" rel="noopener noreferrer") pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Autres API implémentant cette fonctionnalité

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Convertit un fichier Excel en PDF.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Convertit un fichier Excel en images PNG.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Convertit un fichier Excel au format SVG.
---
title: "Convertir un fichier Excel vers différents formats"
ArticleTitle: "Convertir un fichier Excel vers différents formats"
second_title: "Document"
linktype: "Convert Excel"
type: docs
url: /fr/convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud, conversion Excel, conversion de format de fichier, API REST, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Convertir des classeurs Excel vers des formats tels que CSV, PDF, HTML, JSON, Markdown et d'autres à l’aide de l’API REST Aspose.Cells Cloud."
weight: 10
---

Avant d’appeler cette API, assurez-vous d’avoir obtenu un jeton JWT valide et que le classeur source est stocké dans un emplacement pris en charge (par exemple, Aspose Cloud Storage). Incluez le jeton dans l’en-tête `Authorization` et, si nécessaire, spécifiez le paramètre de requête `storageName`.

Cette API REST permet de convertir un fichier Excel vers divers formats de sortie.

## API PutConvertWorkBook

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

La requête est une requête HTTP **PUT** avec un contenu multipart (voir [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La première partie du corps multipart contient le **fichier de données**, tandis que la deuxième partie contient les **options d’enregistrement**.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de requête

| Nom du paramètre        | Type   | Description                                                                                                                |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | Format cible du fichier (par exemple, CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.).      |
| `password`              | string | Mot de passe requis pour ouvrir le fichier Excel source.                                                                           |
| `outPath`               | string | Chemin complet (y compris le nom de fichier et l’extension) pour un fichier de sortie unique, ou chemin de dossier lors de la génération de plusieurs fichiers. |
| `storageName`           | string | Nom du stockage où réside le fichier source.                                                                         |
| `checkExcelRestriction` | bool   | Si **true**, valide les restrictions Excel avant de modifier les cellules ou les objets associés.                                     |
| `streamFormat`          | string | Format du flux de fichier d’entrée.                                                                                           |
| `region`                | string | Paramètres régionaux appliqués au classeur.                                                                                 |
| `pageWideFitOnPerSheet` | bool   | Ajuste la largeur de page pour qu’elle s’adapte à chaque feuille de calcul lors de la conversion en PDF.                                                           |
| `pageTallFitOnPerSheet` | bool   | Ajuste la hauteur de page pour qu’elle s’adapte à chaque feuille de calcul lors de la conversion en PDF.                                                          |
| `sheetName`             | string | Nom de la feuille de calcul à convertir.                                                                                          |
| `pageIndex`             | string | Index de la page à convertir (nécessite `sheetName`).                                                                       |
| `onePagePerSheet`       | bool   | Si **true**, génère une page PDF par feuille de calcul.                                                                       |
| `AutoRowsFit`           | bool   | Ajuste automatiquement la hauteur de toutes les lignes du classeur.                                                                                        |
| `AutoColumnsFit`        | bool   | Ajuste automatiquement la largeur des colonnes du classeur.                                                                                   |

### Paramètres du corps de la requête

| Nom du paramètre | Type      | Description                                                    |
| ---------------- | --------- | -------------------------------------------------------------- |
| `datafile`       | data file | Le fichier Excel placé dans la première partie du corps multipart. |
| `SaveOptions`    | object    | Options d’enregistrement placées dans la deuxième partie du corps multipart.  |

### **Réponse**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille limite. |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue. |

## Comment utiliser l’API PutConvertWorkBook avec les SDK

### Spécification de l’API PutConvertWorkBook

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) définit une interface accessible publiquement qui permet des interactions REST directes depuis un navigateur web.

### Exemple cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK accélère le développement en gérant les détails de bas niveau, ce qui vous permet de vous concentrer sur la logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
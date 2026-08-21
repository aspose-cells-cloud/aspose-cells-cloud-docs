---
title: "Aspose.Cells Cloud Web API - Convertir une feuille de calcul vers un autre format - Outil gratuit en ligne"
second_title: "Document"
ArticleTitle: "Comment convertir une feuille de calcul vers un autre format : Guide étape par étape"
linktitle: "Convertir une feuille de calcul"
type: docs
url: /convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, conversion de feuille de calcul, Excel vers PDF, API Excel, conversion de fichiers cloud"
description: "Convertir un fichier de feuille de calcul vers un autre format à l'aide de l'API Web Aspose.Cells Cloud."
weight: 100
---

Convertissez une feuille de calcul ou un fichier Excel local vers un autre format à l'aide de l'API Web Aspose.Cells Cloud.

## **API de conversion de feuille de calcul**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                      |
| :--------------- | :----- | :----------------------------------------------------- | :----------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                               | Télécharger le fichier de feuille de calcul à convertir.                                        |
| format           | Chaîne  | Chaîne de requête                                      | (Obligatoire) Format de sortie souhaité (par exemple, « XLSX », « PDF », « CSV »).              |
| outPath          | Chaîne  | Chaîne de requête                                      | (Facultatif) Chemin du dossier où le classeur converti sera enregistré. La valeur par défaut est null. |
| outStorageName   | Chaîne  | Chaîne de requête                                      | Spécifier le nom du stockage de sortie.                                                         |
| fontsLocation    | Chaîne  | Chaîne de requête                                      | Utiliser des polices personnalisées pour la feuille de calcul.                                  |
| region           | Chaîne  | Chaîne de requête                                      | Spécifier le paramètre de région de la feuille de calcul.                                       |
| password         | Chaîne  | Chaîne de requête                                      | Mot de passe pour ouvrir le fichier de feuille de calcul s’il est protégé.                     |

### **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Statut de réussite**

- **200 OK** – La conversion a réussi ; le corps de la réponse contient le flux du fichier converti.
- L’en-tête `Content-Type` reflète le type MIME du format de sortie demandé (par exemple, `application/pdf` pour le PDF).

**Codes d’état HTTP**

| Code | Signification         | Description                                                    |
| ---- | --------------------- | -------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête      | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                |
| 413  | Payload trop volumineux | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur | Erreur inattendue sur le serveur.                             |

## Formats de sortie

| **Format de sortie**                                                                                   | **Description**                                                                                                             |
| :----------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Classeur Excel 95/5.0 – 2003.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Format de fichier Excel Open XML SpreadsheetML.                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Classeur binaire Excel.                                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Classeur Excel avec macros.                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Modèle Excel 97 – 2003.                                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Modèle Excel.                                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Modèle Excel avec macros.                                                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | Fichier complémentaire Excel avec macros, utilisé pour ajouter des fonctions à Excel.                                        |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | Fichier CSV (Comma-Separated Values).                                                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | Fichier TSV (Tab-Separated Values).                                                                                          |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | Fichier texte délimité.                                                                                                      |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | Format HTML.                                                                                                                 |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | Fichier MHTML.                                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ODS (OpenDocument Spreadsheet).                                                                                              |
| SpreadsheetML                                                                                          | Fichier Excel 2003 XML.                                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | Document créé par l'application « Numbers » d'Apple, partie de la suite iWork pour macOS et iOS.                             |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | Notation d'objet JavaScript.                                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | Format d'échange de données (Data Interchange Format).                                                                       |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | Fichier .dbf utilisé par le système de gestion de bases de données dBASE.                                                    |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Format de document portable Adobe (Adobe Portable Document Format).                                                          |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | Format XML Paper Specification.                                                                                              |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | Format de graphiques vectoriels évolutifs (Scalable Vector Graphics).                                                        |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | Format de fichier image balisé (Tagged Image File Format).                                                                   |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | Format d’images graphiques réseau portable (Portable Network Graphics).                                                      |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | Format d’image bitmap.                                                                                                       |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | Format de métafichier amélioré (Enhanced Metafile).                                                                          |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG est un format d’image utilisant une compression avec perte.                                                            |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | Format d’échange de graphismes (Graphics Interchange Format).                                                                |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Représente un document Markdown.                                                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | Format basé sur XML utilisé par OpenOffice et StarOffice.                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | Format Open Document stocké en XML plat.                                                                                     |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | Format bien connu pour les documents Microsoft Word, combinant fichiers XML et binaires.                                    |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | Format PPTX basé sur le format de fichier de présentation Open XML de Microsoft PowerPoint.                                 |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | Langage de requête structurée (Structured Query Language).                                                                   |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML est un format de fichier texte basé sur XML, réutilisant HTML 4.0.                                                    |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | Fichiers .epub : format de livre numérique standardisé pour éditeurs et consommateurs.                                      |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML (Extensible Markup Language) ; similaire à HTML, mais utilise des balises pour définir des objets.                      |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Fichier de modèle de feuille Open Document (OTS).                                                                            |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW est un format de livre numérique développé par Amazon pour les appareils Kindle ; AZW3 est également connu sous le nom de Kindle Format 8 (KF8). |

## Où utiliser l’API de conversion de feuille de calcul ?

- **Migration de systèmes hérités** : Convertir des milliers de fichiers XLS hérités vers XLSX pour les systèmes modernes.
- **Standardisation des archives** : Normaliser divers formats de feuilles de calcul (XLS, XLSM, ODS, CSV) vers un seul format pour l’archivage.
- **Interopérabilité entre suites bureautiques** : Convertir des fichiers Excel vers des formats compatibles avec LibreOffice, Google Sheets ou Apple Numbers.
- **Normalisation des sources de données** : Convertir divers formats de feuilles de calcul vers CSV ou JSON pour ingestion dans des bases de données.
- **Publication web** : Convertir des modèles financiers en HTML pour affichage sur le web.

## Pourquoi utiliser l’API de conversion de feuille de calcul ?

- **Facile à utiliser pour les développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide, accompagné d'une documentation complète. Comparé à la création de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de développement.
- **Économique** : Vous pouvez convertir des données de tableau sans avoir à télécharger préalablement le classeur, ce qui économise de l’espace de stockage et réduit les coûts.
- **Support complet des formats** : Conversion entre plus de 20 formats de feuilles de calcul.
- **Préservation de la fidélité des données et du formatage.**

## Comment utiliser l’API de conversion de feuille de calcul avec les SDK ?

Les exemples de code suivants montrent comment utiliser l’API de conversion de feuille de calcul avec divers SDK.

### Spécification de l’API de conversion de feuille de calcul

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">Spécification de l’API de conversion de feuille de calcul</a> définit une interface de programmation accessible publiquement, vous permettant d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir un fichier de feuille de calcul vers un autre format à l’aide d’un code concis. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "Convert a spreadsheet file to another format using Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Convert a spreadsheet to the specified format."
    }
  ]
}
</script>

---
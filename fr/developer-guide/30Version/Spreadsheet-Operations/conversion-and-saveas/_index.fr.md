---
title: "Convertir un fichier Excel dans un autre format ou l’enregistrer différemment."
second_title: "Document"
linktitle: "Conversion et Enregistrer sous"
type: docs
url: /conversion-and-save-as/
aliases: [/convert-excel/, /convert/]
keywords: "Aspose.Cells, API de conversion Excel, convertir Excel en PDF, Excel en CSV, Excel en JSON, conversion de feuilles de calcul dans le cloud"
description: "Découvrez comment convertir des classeurs Excel en PDF, CSV, JSON, HTML et plus de 15 autres formats à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails des points de terminaison, des exemples de commandes cURL et des extraits de code SDK pour Java, .NET, Python, etc."
weight: 30
ArticleTitle: "Convertir des fichiers Excel en PDF, CSV, JSON et plus encore avec Aspose.Cells Cloud"
---

Si vous avez initialement créé un fichier Excel dans un format spécifique—tel que [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), ou [CSV](https://docs.fileformat.com/spreadsheet/csv/)—il peut être utile de convertir ce fichier Excel dans un autre format afin de bénéficier de fonctionnalités spécifiques. Par exemple, convertir un fichier Excel en [PDF](https://docs.fileformat.com/pdf/) protège son contenu contre toute modification non autorisée et facilite sa lecture et son partage.

**Prérequis**  
Avant d’appeler les API de conversion, obtenez un jeton d’accès OAuth 2.0 auprès d’Aspose Cloud et assurez-vous que le classeur est stocké dans votre espace de stockage Aspose Cloud (ou inclus dans le corps de la requête pour le point de terminaison de conversion PUT).

La conversion de documents est un processus complexe. De nombreux facteurs contribuent à la complexité de ce processus et doivent être pris en compte lors de la transformation. Fournir une conversion précise et de qualité professionnelle entre formats Excel est une fonctionnalité clé d’Aspose.Cells Cloud.

Le service fonctionne de manière transparente pour toute conversion de document, quels que soient les formats. Vous pouvez à la fois importer et exporter des documents dans les formats suivants :

**Formats pris en charge**  
- Import/Export : [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- Export uniquement : [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### API de conversion

| API                         | Description                                                                 |
| :-------------------------- | :-------------------------------------------------------------------------- |
| `GET /cells/{name}`         | Récupère un classeur Excel depuis le stockage cloud et le convertit dans le format demandé. |
| `PUT /cells/convert`        | Convertit un classeur Excel fourni dans le corps de la requête dans le format de sortie spécifié. |
| `POST /cells/{name}/saveAs` | Enregistre un classeur Excel existant dans un autre format directement dans le stockage cloud. |

**Détails des API**

- **GET /cells/{name}**  
  - **Paramètres de chemin :** `name` – nom du fichier du classeur (obligatoire).  
  - **Paramètres de requête :** `format` – format cible (par exemple, pdf, csv, json) ; `storage` – nom du stockage cloud (facultatif) ; `folder` – chemin du dossier dans le stockage (facultatif).  
  - **Réponse :** Flux de fichier du classeur converti ; `Content-Type` correspond au format cible.  
  - **Codes de statut :** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **Corps de la requête :** multipart/form‑data contenant le fichier source du classeur (`file`) et un champ obligatoire `format` indiquant le format de sortie souhaité.  
  - **Réponse :** Flux binaire du fichier converti.  
  - **Codes de statut :** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **Paramètres de chemin :** `name` – nom du classeur existant.  
  - **Paramètres de requête :** `format` – format cible ; `outPath` – chemin de destination dans le stockage cloud (facultatif) ; `storage` – nom du stockage (facultatif).  
  - **Réponse :** Objet JSON contenant le résultat de l’opération et le chemin du fichier enregistré. Exemple de réponse :  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "Fichier enregistré avec succès.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **Codes de statut :** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

**Exemple de cURL pour la conversion en PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Extrait de code pour le SDK Java (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**Extrait de code pour le SDK .NET (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Extrait de code pour le SDK Python (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

Les articles suivants expliquent chaque API en détail et incluent des exemples supplémentaires de cURL et de SDK :

- [Convertir un fichier Excel dans un format différent](/cells/convert-an-excel-file-to-different-formats)
- [Enregistrer un fichier Excel dans un format différent](/cells/save-an-excel-file-as-other-formats-files)
- [Convertir un fichier Excel en fichier CSV](/cells/convert-excel-file-to-csv-file)
- [Convertir un fichier Excel en fichier DOCX](/cells/convert-excel-file-to-docx-file)
- [Convertir un fichier Excel en fichier HTML](/cells/convert-excel-file-to-html-file)
- [Convertir un fichier Excel en fichier JSON](/cells/convert-excel-file-to-json-file)
- [Convertir un fichier Excel en fichier Markdown](/cells/convert-excel-file-to-markdown-file)
- [Convertir un fichier Excel en fichier PDF](/cells/convert-excel-file-to-pdf-file)
- [Convertir un fichier Excel en fichier PNG](/cells/convert-excel-file-to-png-file)
- [Convertir un fichier Excel en fichier PPTX](/cells/convert-excel-file-to-pptx-file)
- [Convertir un fichier Excel en fichier SQL](/cells/convert-excel-file-to-sql-file)
- [Convertir un fichier Excel en fichier TIFF](/cells/convert-excel-file-to-tiff-file)
---
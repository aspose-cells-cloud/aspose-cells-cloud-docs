---
title: "Arbet med kalkylark"
second_title: "Dokument"
type: docs
url: /sv/spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, arbet med kalkylark, autojustera, batchbehandling, filskydd, konvertering, import/export, textbehandling"
description: "Lär dig hur du utför arbeten med kalkylark såsom autojustering, batchkonvertering, skydd, sammanfogning och sök-ersätt med Aspose.Cells Cloud REST API. Innehåller kortfattade användningsnoteringar och kodexempel."
weight: 100
ArticleTitle: "Arbet med kalkylark – Aspose.Cells Cloud API-guide"
---

Arbet med kalkylark erbjuder en kortfattad guide till de vanligaste åtgärderna du kan utföra på Excel-arbetsböcker med **Aspose.Cells Cloud** (v3.0). Oavsett om du behöver autojustera kolumner, bearbeta flera filer i ett batch, skydda kalkylblad eller manipulera text – REST API:t erbjuder dedikerade slutpunkter som fungerar över flera språk, såsom Python, C# och Java. Listan nedan innehåller länkar till detaljerad dokumentation för varje åtgärd samt korta användningsnoteringar för att hjälpa dig komma igång snabbt.

**Förutsättningar**: För att kunna anropa dessa slutpunkter behöver du en giltig Aspose.Cells Cloud API-nyckel och inkludera `Authorization`-huvudet (`Bearer <access-token>`). Exemplen antar API-version v3.0.

- **[Alternativ för autojustering](/sv/cells/auto-fitter-options/)** – Justerar automatiskt kolumnbredder och radhöjder. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MinArbetsbok.xlsx/worksheets/Blad1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Batchbehandling av Excel-filer: konvertering, låsning, skydd, delning och upplåsning](/sv/cells/batch/)** – Utför bulkåtgärder (konvertera, låsa, skydda, dela, upplåsa) på upp till 100 filer per begäran. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Bok1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Bok2.xlsx", "action": "protect", "password": "Hemligt123" }
    ]
  }
  ```
- **[Komprimera och reparera Excel-filer](/sv/cells/compress-and-repair-excel-files/)** – Minskar fillstorlek och åtgärdar strukturella problem. `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Rapport.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[Konvertera en Excel-fil till ett annat format eller spara den på ett annat sätt](/sv/cells/conversion-and-save-as/)** – Konvertera Excel till PDF, CSV, HTML etc., eller ändra utdataformatet. `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Finansiella.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[Alternativ för konvertering av arbetsbok](/sv/cells/convert-workbook-options/)** – Finjustera konverteringsinställningar såsom sidstorlek, renderingsoptioner och lösenordsskydd. `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Skapa Excel-filer eller bygga Excel-rapporter](/sv/cells/creating-files-and-reports/)** – Skapa nya arbetsböcker från grunden eller från mallar. `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NyRapport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Mall.xlsx",
    "dataSource": { "name": "Q1-försäljning", "value": 12345 }
  }
  ```
- **[Importera data till Excel-filer och exportera data från Excel-filer](/sv/cells/data-import-and-export/)** – Ladda in data från CSV, JSON eller databaser och exportera kalkylbladsdata. `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Ordrar.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Kryptera, dekryptera och digitalt signera Excel-filer](/sv/cells/protect/)** – Tillämpa lösenordsskydd, kryptering eller digitala signaturer. `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Privat.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "SthetLösenord!23",
    "encryptionType": "Standard"
  }
  ```
- **[Filinformation](/sv/cells/file-info/)** – Hämta metadata såsom filstorlek, format och skapelsedatum. `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Arkiv.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[Sammanfoga och dela Excel-filer](/sv/cells/merge-and-split/)** – Kombinera flera arbetsböcker till en eller dela en arbetsbok i separata filer. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "HelÅret.xlsx"
  }
  ```
- **[Sök och ersätt textinnehåll i Excel-filer](/sv/cells/search-and-replace/)** – Hitta och ersätt strängar över kalkylblad. `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Rapport.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Utkast",
    "newText": "Slutgiltig",
    "options": { "matchCase": false }
  }
  ```
- **[Textbehandling i Excel: lägg till text, ta bort tecken, trimma text, ändra versal/ gemenskap etc.](/sv/cells/text-processing/)** – Utför avancerade textmanipulationer på cellvärden. `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Noteringar.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Infoga vattenstämplar eller ange bakgrundsbilder i Excel-filer](/sv/cells/watermark-and-background/)** – Lägg till bild- eller textvattenstämplar och ange kalkylbladsbakgrund. `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Konfidentiellt",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Arbeta med Excel-filer: formelberäkning, autojustering, rensa objekt etc.](/sv/cells/workbook/)** – Utför vanliga arbetsboksåtgärder såsom beräkna formler, rensa objekt och autojustera. `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytik.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```
---
---
title: "Vad är skillnaden mellan lokal filbearbetning och molnfilbearbetning i Aspose.Cells Cloud?"
second_title: "Dokument"
ArticleTitle: "Vad är skillnaden mellan lokal filbearbetning och molnfilbearbetning i Aspose.Cells Cloud?"
linktitle: "Lokal filbearbetning jämfört med molnfilbearbetning"
type: docs
url: /learn/local-file-processing-vs-cloud-file-processing/
description: "Jämför lokal filbearbetning och molnfilbearbetning i Aspose.Cells Cloud: lagring, kostnad, säkerhet och typiska användningsfall. Förstå vilket tillvägagångssätt som passar bäst din arbetsflödesmodell."
keywords: "Aspose.Cells Cloud, lokal filbearbetning, molnfilbearbetning, kalkylbladskonvertering, API"
weight: 10
---

Lokal filbearbetning och molnfilbearbetning är olika datahanteringsparadigm, med avsevärt olika arkitekturer när det gäller fil lagringsinfrastruktur, affärsprocesser, åtkomst, kostnadsstruktur, säkerhet och lämpliga användningsfall. De huvudsakliga skillnaderna mellan de två är:

**Förutsättningar:** Innan du använder exemplen, se till att du har ett giltigt Aspose.Cells Cloud-konto, den senaste versionen av SDK installerad samt ditt Client Id och Client Secretredo för autentisering.

## 1. Filens lagringsplats och infrastruktur

- Lokal fil:

  - Filer lagras på fysiska enheter som användaren själv äger eller hanterar, t.ex. hårddisken på en personlig dator, interna servrar eller externa hårddiskar. **Du kan peka Cells Cloud-klienten direkt på en fil som finns på valfri lokal lagringsenhet.**
  - Kunden har fullständig fysisk kontroll över hårdvaran.
  - Inköp, underhåll, uppgradering och nedtagning av infrastrukturen ligger i kundens eller deras organisations ansvar.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# Initiera CellsApi
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# Konvertera lokal Excel-fil till PDF
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**API-referens – Konvertera kalkylblad**

| Metod                 | HTTP-metod | Endpoint            | Parametrar (nyckel)                              | Svar                         |
|-----------------------|------------|---------------------|--------------------------------------------------|------------------------------|
| `convert_spreadsheet` | POST       | `/cells/convert`    | `inputFile` – sökväg till källfil<br>`format` – målformat (t.ex. `pdf`) | `200 OK` – konvertering lyckades<br>`400 Bad Request` – ogiltiga parametrar<br>`401 Unauthorized` – autentiseringsfel |

- Molnfil:

  - Filer lagras i fjärrdatacenter som driftas av tredjeparts molntjänsteleverantörer (Aspose molnlagring, Dropbox, AWS, Google Cloud, Microsoft Azure). **AWS, Dropbox, Google Cloud och Microsoft Azure kan alla anslutas till Asposes molnlagring.**
  - Kunden får åtkomst till dessa filer via internet, oavsett var den underliggande hårdvaran fysiskt finns eller vem som underhåller den.
  - Infrastrukturen ligger i leverantörens ansvar, och användarna använder den efter behov.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheet_asRequest,
)

# Initiera CellsApi
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# Ladda upp lokal fil till molnlagring
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# Exportera molnfil till angivet format på lokal lagring
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# Definiera fjärrmappen (ersätt med din faktiska mappnamn om annorlunda)
RemoteFolder = "PythonSDK"

# Spara en Excel-fil i Aspose.Cells Cloud som ett annat filformat i Aspose.Cells Cloud
api.save_spreadsheet_as(
    SaveSpreadsheet_asRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**API-referens – Molnfiloperationer**

| Metod                        | HTTP-metod | Endpoint                     | Parametrar (nyckel)                                                                                   | Svar                                     |
|------------------------------|------------|------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------------------|
| `upload_file`                | PUT        | `/cells/storage/file`        | `localPath` – lokal filsökväg<br>`remotePath` – målplats i molnlagring                                | `200 OK` – uppladdning lyckades<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST       | `/cells/{name}/export`       | `name` – molnfilsnamn<br>`format` – målformat (t.ex. `pdf`)<br>`folder` – valfri mapp                 | `200 OK` – export lyckades<br>`400 Bad Request` |
| `save_spreadsheet_as`        | POST       | `/cells/{name}/saveas`       | `name` – molnfilsnamn<br>`format` – målformat<br>`folder` – målmapp                                     | `200 OK` – sparning lyckades<br>`401 Unauthorized` |

## 2. Affärsprocesser

Oavsett om lokal eller molnfilbearbetning sker all affärsbearbetning på Cells Cloud-servrar, **så internetanslutning krävs alltid**.

## 3. Dataåtkomst

- Lokal filbearbetning:

  - Åtkomst är vanligtvis begränsad till själva enheten.
  - Samarbete mellan flera personer är svårt.
  - Obekvämt vid byte av enhet eller plats.

- Molnfilbearbetning:

  - Filer kan nås från valfri enhet (dator, telefon, surfplatta) när som helst och var som helst så länge det finns internetanslutning.
  - Naturlig stöd för realtidsambitionssamarbeten mellan flera användare; flera användare kan redigera samma dokument samtidigt, och systemet hanterar automatiskt versionskontroll.
  - Hög mobilitet, flexibel kontorsstöd och möjlighet till distansarbete.

## 4. Kostnadsstruktur och säkerhet

- Lokal fil:

  - Hög kapitalutgift i början. Detta leder till ytterligare driftskostnader senare.
  - Fysisk och nätverkssäkerhet styrks helt av användaren själv.

- Molnfil:

  - Låg initial investering, främst driftskostnader, betala för det du använder.
  - Säkerhet och integritet är leverantörens ansvar.

## 5. Lämpliga användningsfall

- Lokal fil: Filoperationer kan endast utföras lokalt.  
- Molnfil: Filoperationer kan utföras lokalt eller i molnet.  

**Anteckningar / Begränsningar:** API:t stöder filer upp till 200 MB för molnbearbetning, och endast de format som anges i dokumentationen kan konverteras. Nätverkslatens kan påverka bearbetningstiden för stora kalkylblad.

_Senast uppdaterad: 30 juli 2026_
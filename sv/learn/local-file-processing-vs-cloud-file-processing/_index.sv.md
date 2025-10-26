---
title: Vad är skillnaden mellan lokal filbehandling och molnbaserad filbehandling i Aspose.Cells Cloud?
second_title: Documen
ArticleTitle: What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud
linktitle: Lokal filbehandling kontra molnbaserad filbehandling
type: docs
url: /sv/learn/local-file-processing-vs-cloud-file-processing/
description: Vad är skillnaden mellan lokal filbehandling och molnbaserad filbehandling? Lokal filbehandling och molnbaserad filbehandling är två fundamentalt olika datahanteringsparadigmer, med betydande skillnader i lagringsinfrastruktur, affärsbehandling, åtkomst, kostnadsstruktur, säkerhet och tillämpliga scenarier.
weight: 10
kwords: Excel Moln API, REST, Kalkylblad, PDF, CSV, Json, Markdown, Lokal filbehandling kontra molnfilbehandling
---
Lokal filbehandling och molnbaserad filbehandling är olika datahanteringsparadigmer, med betydande skillnader i fillagringsinfrastruktur, affärsbehandling, åtkomst, kostnadsstruktur, säkerhet och tillämpliga scenarier. De viktigaste skillnaderna mellan de två är:

## 1. Fillagringsplats och infrastruktur

- Lokal fil:

 Filer lagras på fysiska enheter som användaren äger eller hanterar, såsom hårddisken på en persondator, interna servrar eller externa mobila hårddiskar. Dessa enheter kan nås direkt från Cells Cloud-klienten.
 - Kunden har fullständig fysisk kontroll över hårdvaran.
 - Inköp, underhåll, uppgradering och avveckling av infrastrukturen är användarens eller deras organisations ansvar.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- Molnfil:

 - Filer lagras i fjärrdatacenter som drivs av tredjepartsleverantörer av molntjänster (Aspose molnlagring, Dropbox, AWS, Google Cloud, Microsoft Azure). AWS, Dropbox, Google Cloud och Microsoft Azure kan alla ansluta människor till Aspose molnlagring.
 – Kunder får åtkomst till dessa filer via internet, oavsett plats och underhåll av den underliggande hårdvaran.
 – Infrastrukturen är molntjänstleverantörens ansvar, och användarna använder den på begäran.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import UploadFileRequest, ExportSpreadsheetAsFormatRequest, SaveSpreadsheetAsRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Upload local file to cloud storage
api.upload_file( UploadFileRequest("D:\\Data\\EmployeeSalesSummary.xlsx", "PythonSDK/EmployeeSalesSummary.xlsx"))
# Export cloud file to specified format file to local storage
api.export_spreadsheet_as_format( ExportSpreadsheetAsFormatRequest( "EmployeeSalesSummary.xlsx","pdf" ,folder= "PythonSDK"  ) , local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf" )
# Or Save an Excel file of Cells Cloud as another format file of Cells Cloud. 
api.save_spreadsheet_as( SaveSpreadsheetAsRequest (  "EmployeeSalesSummary.xlsx","pdf" ,folder= RemoteFolder ) )

```

## 2. Affärsbehandling

Oavsett lokal filbehandling eller molnbaserad filbehandling, utförs all affärsbehandling i molnservern Cells,**så internetstöd behövs**.

## 3. Dataåtkomst

- Lokal filbehandling:

 - Åtkomsten är vanligtvis begränsad till själva enheten.
 – Samarbete med flera personer är svårt.
 - Olägenhet vid byte av utrustning eller plats.

- Molnfilbehandling:

 - Få åtkomst till filer från vilken enhet som helst (dator, telefon, surfplatta) när som helst, var som helst, så länge du har en internetanslutning.
 - Naturligt stöd för samarbete i realtid med flera personer, flera användare kan redigera samma dokument samtidigt, systemet hanterar automatiskt versionshantering.
 - Stark mobilitet, flexibel support office och distansarbete.
  
## 4. Kostnadsstruktur och säkerhet

- Lokal fil:
  
 - Höga kapitalutgifter i tidigt skede kräver vissa kostnader för operativt stöd i det senare skedet.
 Både fysisk säkerhet och nätverkssäkerhet kontrolleras av användarna själva.

- Molnfil:

 - Låga initiala investeringar, främst driftskostnader, betala på begäran.
 – Säkerhet och integritet är molntjänstleverantörens ansvar.

## 5. Tillämpliga scenarier

- Lokal fil: Filåtgärder kan endast utföras lokalt.
- Molnfil: Filåtgärder kan utföras lokalt eller i molnet.

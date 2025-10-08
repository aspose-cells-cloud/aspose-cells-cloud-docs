---
title: Qual è la differenza tra l'elaborazione dei file locali e l'elaborazione dei file cloud in Aspose.Cells Cloud
second_title: Documen
ArticleTitle: What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud
linktitle: Elaborazione file locale vs. Elaborazione file cloud
type: docs
url: /it/learn/local-file-processing-vs-cloud-file-processing/
description: Qual è la differenza tra l'elaborazione di file locali e l'elaborazione di file cloud? L'elaborazione di file locali e l'elaborazione di file cloud sono due paradigmi di gestione dei dati fondamentalmente diversi, con differenze significative in termini di infrastruttura di archiviazione, elaborazione aziendale, accesso, struttura dei costi, sicurezza e scenari applicabili.
weight: 10
kwords: Excel Cloud API, REST, Foglio di calcolo, PDF, CSV, Json, Markdown, Elaborazione file locale vs. Elaborazione file cloud
---
L'elaborazione dei file locali e l'elaborazione dei file nel cloud sono paradigmi di gestione dei dati diversi, con differenze significative nell'infrastruttura di archiviazione dei file, nell'elaborazione aziendale, nell'accesso, nella struttura dei costi, nella sicurezza e negli scenari applicabili. Le principali differenze tra i due sono:

## 1. Posizione e infrastruttura di archiviazione dei file

- File locale:

 I file vengono archiviati su dispositivi fisici di proprietà o gestiti dall'utente, come il disco rigido di un personal computer, server interni o dischi rigidi mobili esterni. Questi dispositivi sono accessibili direttamente dal client Cloud Cells.
 - Il cliente ha il controllo fisico completo sull'hardware.
 - L'acquisto, la manutenzione, l'aggiornamento e il disinvestimento dell'infrastruttura sono responsabilità dell'utente o della sua organizzazione.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- File cloud:

 - I file vengono archiviati in data center remoti gestiti da provider di servizi cloud di terze parti (Aspose cloud storage, Dropbox, AWS, Google Cloud, Microsoft Azure). AWS, Dropbox, Google Cloud e Microsoft Azure possono tutti connettere gli utenti a Aspose cloud storage.
 - I clienti accedono a questi file tramite Internet, indipendentemente dalla posizione e dalla manutenzione dell'hardware sottostante.
 - L'infrastruttura è responsabilità del fornitore di servizi cloud e gli utenti la utilizzano su richiesta.

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

## 2. Elaborazione aziendale

Indipendentemente dall'elaborazione dei file locali o dall'elaborazione dei file cloud, tutta l'elaborazione aziendale viene completata nel server cloud Cells,**quindi è richiesto il supporto di Internet**.

## 3. Accesso ai dati

- Elaborazione file locale:

 - L'accesso è solitamente limitato al dispositivo stesso.
 - La collaborazione tra più persone è difficile.
 - Disagio nel cambio di attrezzatura o di posizione.

- Elaborazione dei file nel cloud:

 - Accedi ai file da qualsiasi dispositivo (computer, telefono, tablet) in qualsiasi momento e ovunque, purché tu abbia una connessione Internet.
 - Supporto naturale per la collaborazione in tempo reale tra più persone: più utenti possono modificare lo stesso documento contemporaneamente, il sistema gestisce automaticamente il controllo delle versioni.
 - Elevata mobilità, supporto flessibile office e lavoro da remoto.
  
## 4. Struttura dei costi e sicurezza

- File locale:
  
 - Un'elevata spesa in conto capitale nella fase iniziale richiede determinati costi per il supporto operativo nella fase successiva.
 Sia la sicurezza fisica che quella della rete sono controllate dagli utenti stessi.

- File cloud:

 - Basso investimento iniziale, principalmente spese operative, pagamento a richiesta.
 - La sicurezza e l'integrità sono responsabilità del fornitore di servizi cloud.

## 5. Scenari applicabili

- File locale: le operazioni sui file possono essere eseguite solo localmente.
- File cloud: le operazioni sui file possono essere eseguite localmente o nel cloud.

---
title: "Qual è la differenza tra l'elaborazione dei file locali e l'elaborazione dei file nel cloud in Aspose.Cells Cloud?"
second_title: "Documento"
ArticleTitle: "Qual è la differenza tra l'elaborazione dei file locali e l'elaborazione dei file nel cloud in Aspose.Cells Cloud?"
linktitle: "Elaborazione dei file locali vs. elaborazione dei file nel cloud"
type: docs
url: /it/learn/local-file-processing-vs-cloud-file-processing/
description: "Confronta l’elaborazione dei file locali e dei file nel cloud di Aspose.Cells Cloud: archiviazione, costi, sicurezza e scenari tipici. Scopri quale approccio si adatta meglio al tuo flusso di lavoro."
keywords: "Aspose.Cells Cloud, elaborazione dei file locali, elaborazione dei file nel cloud, conversione di fogli di calcolo, API"
weight: 10
---

L'elaborazione dei file locali e l'elaborazione dei file nel cloud sono due paradigmi distinti di gestione dei dati, con differenze significative riguardo all’infrastruttura di archiviazione dei file, alla gestione aziendale, all’accesso, alla struttura dei costi, alla sicurezza e agli scenari applicabili. Le principali differenze tra i due approcci sono le seguenti:

**Prerequisiti:** Prima di utilizzare gli esempi, assicurati di disporre di un account valido di Aspose.Cells Cloud, della versione più recente dell'SDK installata e dei tuoi Client Id e Client Secret pronti per l'autenticazione.

## 1. Posizione di archiviazione dei file e infrastruttura

- File locali:

  - I file vengono archiviati su dispositivi fisici di proprietà o gestiti dall'utente, ad esempio sull’hard disk di un computer personale, su server interni o su unità esterne. **È possibile puntare direttamente il client Cells Cloud verso un file situato su qualsiasi dispositivo di archiviazione locale.**
  - Il cliente ha il controllo completo in termini fisici sull’hardware.
  - L’acquisto, la manutenzione, l’aggiornamento e la dismissione dell’infrastruttura sono di competenza dell’utente o della propria organizzazione.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# Inizializza CellsApi
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# Converti un file Excel locale in PDF
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**Riferimento API – Converti foglio di calcolo**

| Metodo                | Verbo HTTP | Endpoint            | Parametri (chiave)                               | Risposte                                                |
|-----------------------|------------|---------------------|--------------------------------------------------|---------------------------------------------------------|
| `convert_spreadsheet` | POST       | `/cells/convert`    | `inputFile` – percorso del file sorgente<br>`format` – formato di destinazione (es. `pdf`) | `200 OK` – conversione riuscita<br>`400 Bad Request` – parametri non validi<br>`401 Unauthorized` – errore di autenticazione |

- File nel cloud:

  - I file vengono archiviati in centri dati remoti gestiti da provider di servizi cloud di terze parti (archiviazione cloud di Aspose, Dropbox, AWS, Google Cloud, Microsoft Azure). **AWS, Dropbox, Google Cloud e Microsoft Azure possono tutti connettersi all’archiviazione cloud di Aspose.**
  - I clienti accedono a questi file tramite Internet, indipendentemente dalla posizione e dalla gestione dell’hardware sottostante.
  - L’infrastruttura è di competenza del provider di servizi cloud, e gli utenti la utilizzano su richiesta.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheetAsRequest,
)

# Inizializza CellsApi
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# Carica un file locale nell’archiviazione cloud
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# Esporta un file nel cloud in un file di formato specificato, salvandolo localmente
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# Definisci la cartella remota (sostituisci con il nome effettivo della cartella, se diverso)
RemoteFolder = "PythonSDK"

# Salva un file Excel di Cells Cloud in un altro formato all'interno di Cells Cloud
api.save_spreadsheet_as(
    SaveSpreadsheetAsRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**Riferimento API – Operazioni con file nel cloud**

| Metodo                     | Verbo HTTP | Endpoint                     | Parametri (chiave)                                                                                   | Risposte                                             |
|----------------------------|------------|------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| `upload_file`              | PUT        | `/cells/storage/file`        | `localPath` – percorso locale del file<br>`remotePath` – percorso di destinazione nell’archiviazione cloud | `200 OK` – caricamento riuscito<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST     | `/cells/{name}/export`       | `name` – nome del file nel cloud<br>`format` – formato di destinamento (es. `pdf`)<br>`folder` – cartella opzionale | `200 OK` – esportazione riuscita<br>`400 Bad Request` |
| `save_spreadsheet_as`      | POST       | `/cells/{name}/saveas`       | `name` – nome del file nel cloud<br>`format` – formato di destinamento<br>`folder` – cartella di destinazione | `200 OK` – salvataggio riuscito<br>`401 Unauthorized` |

## 2. Elaborazione aziendale

Indipendentemente dall’elaborazione dei file locali o dall’elaborazione dei file nel cloud, **tutte le operazioni di elaborazione vengono completate sul server Cells Cloud**, pertanto è richiesto il supporto Internet.

## 3. Accesso ai dati

- Elaborazione dei file locali:

  - L’accesso è generalmente limitato al dispositivo stesso.
  - La collaborazione tra più utenti è difficile.
  - Inconvenienza nel cambiare dispositivo o posizione.

- Elaborazione dei file nel cloud:

  - Accesso ai file da qualsiasi dispositivo (computer, telefono, tablet), ovunque e in qualsiasi momento, purché sia disponibile una connessione Internet.
  - Supporto nativo per la collaborazione in tempo reale tra più utenti: più utenti possono modificare contemporaneamente lo stesso documento, e il sistema gestisce automaticamente il controllo delle versioni.
  - Elevata mobilità, supporto flessibile per l’ufficio e per il lavoro remoto.

## 4. Struttura dei costi e sicurezza

- File locali:

  - Richiede un’ingente spesa iniziale in termini di capitale. Ciò comporta costi aggiuntivi per il supporto operativo in seguito.
  - La sicurezza fisica e quella di rete sono controllate direttamente dagli utenti.

- File nel cloud:

  - Investimento iniziale ridotto, prevalentemente spese operative, con modello di pagamento in base all’uso.
  - La sicurezza e l’integrità sono di responsabilità del provider di servizi cloud.

## 5. Scenari applicabili

- File locali: Le operazioni sui file possono essere eseguite solo in locale.  
- File nel cloud: Le operazioni sui file possono essere eseguite sia in locale che nel cloud.  

**Note / Limitazioni:** L’API supporta file fino a 200 MB per l’elaborazione nel cloud, e solo i formati elencati nella documentazione possono essere convertiti. La latenza di rete può influire sui tempi di elaborazione per fogli di calcolo di grandi dimensioni.

_Ultimo aggiornamento: 30 luglio 2026_
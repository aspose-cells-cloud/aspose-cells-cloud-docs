---
title: "Manuale operativo Aspose.Cells Cloud Docker: ospita l'applicazione Aspose.Cells Cloud sulla propria infrastruttura privata."
second_title: "Documento"
ArticleTitle: "Manuale operativo Aspose.Cells Cloud Docker"
linktitle: "Docker"
type: docs
url: /docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: "Distribuisci Aspose.Cells Cloud come contenitore Docker su infrastrutture private o on-premises, abilitando l'elaborazione di fogli elettronici (Excel, PDF, CSV, JSON, Markdown) senza ricorrere al cloud pubblico di Aspose."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Immagine Docker",
    "API per fogli elettronici",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Cloud privato",
    "Distribuzione",
  ]
weight: 30
---

Aspose.Cells Cloud è un servizio di elaborazione di fogli elettronici basato sul cloud che supporta la creazione, la modifica, la conversione e la manipolazione di file nei formati, tra cui Excel. Può essere configurato rapidamente come ambiente di servizio autonomo tramite distribuzione Docker, semplificando la gestione delle dipendenze e i processi di distribuzione cross-platform.

Questo manuale fornisce una descrizione dettagliata delle fasi operative complete, dalla preparazione dell'ambiente alla verifica del servizio.

## Preparazione dell'ambiente

Prima di distribuire il contenitore Docker di Aspose.Cells Cloud, assicurati che l'ambiente locale soddisfi i requisiti di dipendenza riportati di seguito, per evitare errori di distribuzione causati da componenti mancanti.

### Componenti di dipendenza di base

- **Docker Engine:** motore principale per l'esecuzione dei contenitori, responsabile della creazione e della gestione dei container. La versione minima richiesta è **18.09.0**.
- **Sistemi operativi:** sistemi operativi mainstream che supportano Docker

  | Tipo di sistema operativo | Versione                  |
  | :------------------------ | :------------------------ |
  | Windows                   | Windows 10/11             |
  | Windows Server            | 2016 / 2019 / 2022        |
  | Linux                     | CentOS 7+ / Ubuntu 20.04+ |

- **Risorse hardware:** assicurati che il servizio funzioni correttamente per evitare arresti anomali dovuti a risorse insufficienti.
  - CPU: 2 core o più.
  - Memoria: 4 GB o più.
  - Disco: 10 GB di spazio disponibile.

### Condizioni preliminari essenziali

- **Licenza Aspose:** registra un account ufficiale Aspose per ottenere una licenza valida (puoi richiedere una versione di prova o acquistare una versione commerciale). Senza una licenza, le funzionalità del servizio potrebbero essere limitate. Consulta la pagina [Licenza](https://purchase.aspose.com/buy) per ulteriori dettagli.
- **Connettività di rete:** assicurati che l'ambiente di distribuzione possa accedere a Docker Hub (per il download delle immagini).

## Ottenere l'immagine Docker di Aspose.Cells Cloud

L'immagine di Aspose.Cells Cloud è ospitata su Docker Hub e può essere scaricata direttamente tramite il comando `docker pull`, senza necessità di compilazione manuale.

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## Eseguire il contenitore Docker di Aspose.Cells Cloud

### Parametri di esecuzione

| Nome                        | Descrizione                                                                 | Osservazione                                                  |
| --------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------- |
| LicensePublicKey            | Imposta la chiave pubblica della licenza quando si utilizza la modalità di fatturazione Metered. | Valido solo se si adotta la modalità di fatturazione Metered. |
| LicensePrivateKey           | Imposta la chiave privata della licenza quando si utilizza la modalità di fatturazione Metered. | Valido solo se si adotta la modalità di fatturazione Metered. |
| storagesCredentialsFilePath | Percorso del file di configurazione dello storage. Il file predefinito è `./storageResource.json`. |                                                               |
| LicenseFile                 | Imposta il file della licenza quando si utilizza la modalità di fatturazione LicenseFile. | Valido solo se si adotta la modalità di fatturazione LicenseFile. |
| AccessToken                 | Token per accedere all'API.                                                 | Se vuoto, non è richiesta alcuna verifica tramite token.      |

### Comando di esecuzione

Eseguire il contenitore in modalità di prova è semplice come questo:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Per un'esecuzione completa con tutte le funzionalità, ottieni una [licenza Metered](https://purchase.aspose.com/faqs/licensing/metered/) e monta una cartella dell'host per lo storage dei file. Di seguito è riportato come apparirebbe il comando di esecuzione in questo caso:

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### Riferimento API – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### Esporre la porta

| Porta | Descrizione                                    | Obbligatoria |
| ----- | ---------------------------------------------- | ------------ |
| 5000  | Cartella contenente i font utilizzati per il rendering dei documenti | sì           |

### Volume richiesto

| Percorso di mount nel contenitore | Descrizione                                    | Obbligatorio | Osservazione                                                    |
| --------------------------------- | ---------------------------------------------- | ------------ | --------------------------------------------------------------- |
| C:\fonts                          | Cartella contenente i font utilizzati per il rendering dei documenti | no           | Risolve problemi nei fogli elettronici/Excel causati da font mancanti. |
| C:\data                           | Cartella per lo storage dei file               | no           | Aumenta lo spazio di archiviazione per una gestione e accesso più semplici dei file. |

## Documentazione di riferimento

- [Funzionalità principali del contenitore Docker di Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker-container-features/)
- [Come configurare lo storage del contenitore Docker di Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/storage/)
- [Come eseguire il contenitore Docker di Aspose.Cells Cloud](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
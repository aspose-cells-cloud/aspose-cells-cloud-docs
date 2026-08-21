---
title: "Eseguire il contenitore Docker di Aspose.Cells Cloud – Pull, configurazione e avvio"
second_title: "Documento"
ArticleTitle: "Come eseguire il contenitore Docker di Aspose.Cells Cloud"
LinkTitle: "Contenitore Docker"
type: docs
url: /it/getting-started/how-to-run-docker-container/
aliases: [  /it/how-to-run-docker-container/ ]
description: "Scopri come eseguire il pull, configurare e avviare il contenitore Docker di Aspose.Cells Cloud su Windows o Linux. Include YAML di Docker Compose, configurazione della licenza, mappatura delle porte e suggerimenti per la risoluzione dei problemi."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Contenitore Docker"
  - "Docker Compose"
  - "Chiavi di licenza"
  - "Excel"
  - "Foglio di calcolo"
  - "API cloud"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

La tecnologia Docker è progettata per automatizzare la distribuzione delle applicazioni utilizzando container leggeri. Gli sviluppatori possono utilizzare un contenitore Docker per raggruppare un'applicazione con tutte le sue librerie e dipendenze e distribuirle come un unico pacchetto.

Il team Aspose.Cells Cloud ha pubblicato il contenitore Docker su <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> per facilitare l'utilizzo agli utenti Docker.

**Prerequisiti** – Assicurati che Docker Engine ≥ 20.x sia installato e che il tuo sistema operativo (Windows 10/Server 2019/2022 o una distribuzione Linux supportata) soddisfi i requisiti. È possibile fornire facoltativamente una chiave di licenza per eseguire in modalità con licenza.

- Docker Engine ≥ 20.x installato  
- Sistema operativo supportato (Windows 10/Server 2019/2022 o una distribuzione Linux)  
- Chiave di licenza facoltativa per la modalità con licenza  

## Configurazione del contenitore

### Volume richiesti

| Percorso di mount nel contenitore | Descrizione |
| :--- | :--- |
| C:\fonts | Cartella contenente i font da utilizzare per il rendering dei documenti |
| C:\data | Cartella di archiviazione dei file |

**Alternativa per Linux/macOS** – Utilizzare `/fonts` e `/data` all'interno del contenitore e mapparli alle directory host, ad esempio `/home/user/fonts` e `/home/user/data`, durante l’esecuzione del contenitore.

### Parametri

| Nome | Descrizione |
| :--- | :--- |
| LicensePublicKey | Chiave pubblica della licenza |
| LicensePrivateKey | Chiave privata della licenza |

Se i parametri **License** vengono omessi, l'applicazione viene eseguita in modalità di prova.

### 1. Eseguire il pull dell’immagine Aspose.Cells Cloud

```bash
# Eseguire il pull di una versione specifica dell'immagine Aspose.Cells Cloud
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Eseguire il pull dell'immagine Aspose.Cells Cloud per Windows Server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Eseguire il pull dell'immagine Aspose.Cells Cloud per Windows Server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Eseguire il pull dell'immagine Aspose.Cells Cloud per Windows 11
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **Nota:** Per ottenere sempre la versione più recente, puoi anche eseguire il pull del tag `latest`: `docker pull aspose/cells-cloud:latest`.

### 2. Configurazioni per lo strumento Docker‑Compose

Puoi scrivere la seguente configurazione in un file **docker‑compose.yml**:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # host 5000 → container 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **Nota:** La mappatura delle porte `5000:80` indica che l’API sarà raggiungibile all’indirizzo `http://localhost:5000`.

### 3. Eseguire un contenitore Docker tramite riga di comando

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**Risoluzione dei problemi:**  
- **Conflitto di porte:** Assicurati che la porta 5000 sull’host sia libera oppure modifica la mappatura su una porta non utilizzata.  
- **Errore nel caricamento della licenza:** Verifica che le chiavi pubblica e privata siano correttamente passate come variabili d’ambiente o montate come file.  
- **Font mancanti:** Se i documenti vengono renderizzati con font errati, conferma che la directory dei font sia correttamente montata e contenga i file font necessari.

**Risorse correlate:**  
- <a href="/cells/api/">Riferimento API</a> | <a href="/cells/license/">Guida all'attivazione della licenza</a> | <a href="/cells/getting-started/">Panoramica di base</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Eseguire il contenitore Docker di Aspose.Cells Cloud",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "Eseguire il pull dell’immagine Docker",
      "text": "Esegui `docker pull aspose/cells-cloud:<version>` per scaricare l’immagine richiesta."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "Creare un file docker‑compose",
      "text": "Definisci immagine, porte, volumi e variabili d’ambiente della licenza in `docker‑compose.yml`."
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "Eseguire il contenitore",
      "text": "Esegui `docker run` con le variabili d’ambiente, i mount dei volumi e la mappatura delle porte appropriate."
    }
  ]
}
```
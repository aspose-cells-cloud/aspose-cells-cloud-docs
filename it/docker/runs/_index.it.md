---
title: "Come avviare il contenitore Docker di Aspose.Cells Cloud"
second_title: "Documenti"
ArticleTitle: "Come avviare il contenitore Docker di Aspose.Cells Cloud"
linktitle: "Avvio contenitore"
type: docs
url: /it/run-aspose-cells-cloud-docker-container/
description: "Scopri come avviare Aspose.Cells Cloud all'interno di un contenitore Docker su Windows Server 2022. Comandi passo‑passo per le modalità di prova, a pagamento in base all'uso, a pagamento con licenza, per la configurazione dello spazio di archiviazione e per il controllo dello stato del servizio."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, modalità di prova, fatturazione a consumo, fatturazione con licenza, configurazione dell'archiviazione"
---

Aspose.Cells Cloud Docker fornisce un'immagine di contenitore pronta all'uso che ospita l'API di Aspose.Cells Cloud in locale o in una cloud privata. Questa guida illustra come avviare il contenitore in tre modalità di licenza comuni: **Prova**, **Fatturazione a consumo** e **Fatturazione con licenza**, e include anche una variante che utilizza un token di accesso. Tutti i comandi sono scritti per PowerShell su Windows Server 2022; adatta i percorsi dei volumi se utilizzi Linux.

**Prerequisiti**

- Docker Engine 20.10 o successivo installato e in esecuzione.  
- PowerShell 5.1 o PowerShell 7+.  
- Aprire la porta 5000 all'interno del contenitore (mappata alla porta 47900 dell'host) e assicurarsi che il firewall dell'host consenta il traffico in ingresso sulla porta 47900.  
- Per le modalità di fatturazione a consumo o con licenza, disporre di `LicensePublicKey`, `LicensePrivateKey` o di un file di licenza valido, oppure di un `AccessToken` se si utilizza la modalità basata su token.  
- Una cartella locale (ad esempio `C:\data`) da montare come archiviazione per il contenitore.

**Avvio rapido (modalità Prova)**  

Esegui il comando seguente per avviare il contenitore in modalità prova:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## Avviare il contenitore Docker di Aspose.Cells Cloud in modalità Prova

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Il contenitore viene eseguito in primo piano e ascola sulla porta dell'host **47900**, che viene inoltrata alla porta interna **5000** del contenitore.

## Avviare il contenitore Docker di Aspose.Cells Cloud in modalità Fatturazione a consumo

```powershell
# Windows Server 2022
# Modalità a pagamento in base all'uso: impostare LicensePublicKey e LicensePrivateKey come variabili d'ambiente.
# Montare una cartella di archiviazione (host → contenitore)
#   -v c:/data:c:/data
# Montare la cartella dei font di Windows affinché l'API possa accedere ai font di sistema
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=chiavePubblicaLicenza `
  -e LicensePrivateKey=chiavePrivataLicenza `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Il contenitore viene eseguito in modalità separata (`-d`). Dopo l'avvio, puoi verificare che il servizio sia raggiungibile con il comando:

```powershell
curl http://localhost:47900/v3.0/health
```

**Esempio di file `storageResource.json`**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## Avviare il contenitore Docker di Aspose.Cells Cloud in modalità Fatturazione con licenza

```powershell
# Windows Server 2022
# Modalità a pagamento con licenza: fornire un file di licenza tramite la variabile d'ambiente LicenseFile.
# Montare una cartella di archiviazione (host → contenitore)
#   -v c:/data:c:/data
# Montare la cartella dei font di Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## Avviare il contenitore Docker di Aspose.Cells Cloud tramite token di accesso

```powershell
# Windows Server 2022
# Modalità basata su token di accesso: impostare AccessToken insieme alle chiavi opzionali per la fatturazione a consumo.
# Montare una cartella di archiviazione
#   -v c:/data:c:/data
# Montare la cartella dei font di Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=chiavePubblicaLicenza `
  -e LicensePrivateKey=chiavePrivataLicenza `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Dopo aver avviato il contenitore, conferma che il servizio sia operativo utilizzando lo stesso comando di controllo dello stato visto in precedenza.

## Documentazione di riferimento

- [Come configurare l'archiviazione per il contenitore Docker di Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/docker/storage/)

---

### Risoluzione dei problemi

- **Controllo dello stato non riuscito** – Assicurati che la porta 47900 non sia bloccata dal firewall e che il contenitore sia in esecuzione (`docker ps`).  
- **Errori relativi alla licenza** – Verifica che i valori di `LicensePublicKey`, `LicensePrivateKey` o `LicenseFile` siano corretti e che le variabili d'ambiente siano passate senza spazi bianchi aggiuntivi.  
- **Archiviazione non accessibile** – Conferma che la cartella dell'host (`c:/data`) esista e che Docker disponga delle autorizzazioni per leggere e scrivere al suo interno.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Come avviare il contenitore Docker di Aspose.Cells Cloud",
  "description": "Guida passo‑passo per avviare Aspose.Cells Cloud all'interno di un contenitore Docker su Windows Server 2022, coprendo le modalità di prova, a pagamento in base all'uso, a pagamento con licenza e basata su token di accesso.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, modalità di prova, fatturazione a consumo, fatturazione con licenza, configurazione dell'archiviazione"
}
</script>
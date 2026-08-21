---
title: "Tag delle immagini Docker di Aspose.Cells Cloud"
second_title: "Documenti"
ArticleTitle: "Tag delle immagini Docker di Aspose.Cells Cloud"
linktitle: "Tag immagine"
type: docs
url: /docker/tag-list/
description: "Trova gli ultimi tag delle immagini Docker di Aspose.Cells Cloud per Windows Server (2016‑2022) e Linux. Ottieni i comandi di pull, i dettagli sull’architettura e le note di aggiornamento in un’unica posizione."
weight: 30
keywords:
  - "Tag delle immagini Docker di Aspose.Cells Cloud"
  - "Comandi docker pull"
  - "Tag Docker per Windows Server"
  - "Tag Docker per Linux"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud fornisce immagini Docker pronte all'uso per Windows Server (2016, 2019, 2022) e Linux.  
Ogni immagine è contrassegnata con un **tag** che identifica la versione del prodotto e il sistema operativo di destinazione.  
Usa i tag indicati di seguito per eseguire il pull dell'immagine esatta di cui hai bisogno e consulta gli esempi di pull e avvio forniti per un rapido avvio.

*Ultimo aggiornamento: 2026-07-01*

**Prerequisiti:** Assicurati che Docker Engine 20.10 o successiva sia installato e che tu disponga di una chiave di licenza valida per Aspose.Cells Cloud. Le immagini sono costruite per le specifiche versioni di Windows Server indicate o per Linux x64.

## Immagini per Windows Server 2016 ##

Tag | Architettura | Dockerfile | Note
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile non pubblicato – consulta le [note sulla versione](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016) per i dettagli sulla compilazione. | Non sono previsti tag successivi per Windows Server 2016; questa è l’ultima versione rilasciata.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

Risorse aggiuntive: [Download Docker](/cells/docker/downloads/), [Note sulla versione](/cells/release-notes/), [Prerequisiti](/cells/docker/prerequisites/).  
Consulta la [Panoramica Docker](/cells/docker/) per ulteriori dettagli.

## Immagini per Windows Server 2019 ##

Tag | Architettura | Dockerfile | Note
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile non pubblicato – consulta le [note sulla versione](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019) per i dettagli sulla compilazione. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

Risorse aggiuntive: [Download Docker](/cells/docker/downloads/), [Note sulla versione](/cells/release-notes/), [Prerequisiti](/cells/docker/prerequisites/).  
Consulta la [Panoramica Docker](/cells/docker/) per ulteriori dettagli.

## Immagini per Windows Server 2022 ##

Tag | Architettura | Dockerfile | Note
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile non pubblicato – consulta le [note sulla versione](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022) per i dettagli sulla compilazione. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

Risorse aggiuntive: [Download Docker](/cells/docker/downloads/), [Note sulla versione](/cells/release-notes/), [Prerequisiti](/cells/docker/prerequisites/).  
Consulta la [Panoramica Docker](/cells/docker/) per ulteriori dettagli.

## Immagini per Linux ##

Tag | Architettura | Dockerfile | Note
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile non pubblicato – consulta le [note sulla versione](https://github.com/aspose-cells/dockerfiles/tree/main/linux) per i dettagli sulla compilazione. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

Risorse aggiuntive: [Download Docker](/cells/docker/downloads/), [Note sulla versione](/cells/release-notes/), [Prerequisiti](/cells/docker/prerequisites/).  
Consulta la [Panoramica Docker](/cells/docker/) per ulteriori dettagli.

**Registro delle modifiche di versione**

Tag | Modifiche
---|---
`ltsc2016.23.5.0` | Ultima versione per Windows Server 2016; include patch di sicurezza e miglioramenti delle prestazioni.
`ltsc2019.25.10.0` | Aggiornato ad Aspose.Cells 25.10.0; aggiunge supporto per nuove formule e correzioni di bug.
`ltsc2022.25.10.0` | Identico al tag 2019, ottimizzato per l'ambiente di runtime di Windows Server 2022.
`linux.25.10.0` | Immagine Linux base con Aspose.Cells 25.10.0; include dipendenze aggiornate e ottimizzazioni specifiche per Linux.
---
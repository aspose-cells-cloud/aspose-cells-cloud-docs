---
title: "Aspose.Cells Cloud Docker-avbildsmärken"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Docker-avbildsmärken"
linktitle: "Avbildsmärken"
type: docs
url: /sv/docker/tag-list/
description: "Hitta de senaste Aspose.Cells Cloud Docker-avbildsmärkena för Windows Server (2016‑2022) och Linux. Få kommandon för att hämta avbild, arkitekturuppgifter och uppgraderingsinformation på en och samma plats."
weight: 30
keywords:
  - "Aspose.Cells Cloud Docker-avbildsmärken"
  - "Docker-hämtningskommandon"
  - "Windows Server Docker-märken"
  - "Linux Docker-märken"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud tillhandahåller klara att köra Docker-avbildar för Windows Server (2016, 2019, 2022) och Linux.  
Varje avbild är versionerad med ett **märke** som identifierar produktreleasen och måloperativsystemet.  
Använd märkena nedan för att hämta exakt den avbild du behöver, och se tillhörande exempel för att köra och starta snabbt.

*Senast uppdaterad: 2026-07-01*

**Förutsättningar:** Se till att Docker Engine 20.10 eller senare är installerat och att du har en giltig Aspose.Cells Cloud-licensnyckel. Avbildarna är byggda för de angivna Windows Server-versionerna eller Linux x64.

## Windows Server 2016-avbildar ##

Märken | Arkitektur | Dockerfil | Anmärkning
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfilen är inte tillgänglig – se [releaseanteckningarna](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016) för bygginformation. | Inget nyare märke är planerat för Windows Server 2016; detta är den sista släppta versionen.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

Ytterligare resurser: [Docker-hämtning](/cells/docker/downloads/), [Releaseanteckningar](/cells/release-notes/), [Förutsättningar](/cells/docker/prerequisites/).  
Se [Docker-översikt](/cells/docker/) för ytterligare information.

## Windows Server 2019-avbildar ##

Märken | Arkitektur | Dockerfil | Anmärkning
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfilen är inte tillgänglig – se [releaseanteckningarna](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019) för bygginformation. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

Ytterligare resurser: [Docker-hämtning](/cells/docker/downloads/), [Releaseanteckningar](/cells/release-notes/), [Förutsättningar](/cells/docker/prerequisites/).  
Se [Docker-översikt](/cells/docker/) för ytterligare information.

## Windows Server 2022-avbildar ##

Märken | Arkitektur | Dockerfil | Anmärkning
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfilen är inte tillgänglig – se [releaseanteckningarna](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022) för bygginformation. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

Ytterligare resurser: [Docker-hämtning](/cells/docker/downloads/), [Releaseanteckningar](/cells/release-notes/), [Förutsättningar](/cells/docker/prerequisites/).  
Se [Docker-översikt](/cells/docker/) för ytterligare information.

## Linux-avbildar ##

Märken | Arkitektur | Dockerfil | Anmärkning
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfilen är inte tillgänglig – se [releaseanteckningarna](https://github.com/aspose-cells/dockerfiles/tree/main/linux) för bygginformation. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

Ytterligare resurser: [Docker-hämtning](/cells/docker/downloads/), [Releaseanteckningar](/cells/release-notes/), [Förutsättningar](/cells/docker/prerequisites/).  
Se [Docker-översikt](/cells/docker/) för ytterligare information.

**Ändringslogg för versioner**

Märke | Ändringar
---|---
`ltsc2016.23.5.0` | Sista releasen för Windows Server 2016; innehåller säkerhetskorrigeringar och prestandaförbättringar.
`ltsc2019.25.10.0` | Uppdaterad till Aspose.Cells 25.10.0; lägger till stöd för nya formler och buggfixar.
`ltsc2022.25.10.0` | Samma som märket 2019, optimerat för Windows Server 2022-körning.
`linux.25.10.0` | Bas-Linux-avbild med Aspose.Cells 25.10.0; innehåller uppdaterade beroenden och Linux-specifika optimeringar.
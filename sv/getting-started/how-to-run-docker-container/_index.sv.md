---
title: "Kör Aspose.Cells Cloud Docker-container – Hämta, konfigurera & starta"
second_title: "Dokument"
ArticleTitle: "Hur man kör Aspose.Cells Cloud Docker-container"
LinkTitle: "Docker-container"
type: docs
url: /sv/getting-started/how-to-run-docker-container/
aliases: [  /sv/how-to-run-docker-container/ ]
description: "Lär dig hur du hämtar, konfigurerar och kör Aspose.Cells Cloud Docker-container på Windows eller Linux. Innehåller Docker‑Compose YAML, licensinställning, portmappning och felsöknings tips."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker-container"
  - "Docker Compose"
  - "licensnycklar"
  - "Excel"
  - "kalkylark"
  - "moln-API"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

Docker-tekniken är utformad för att automatisera distributionen av program genom att använda lättviktiga containrar. Utvecklare kan använda en Docker-container för att bunda ett program tillsammans med alla dess bibliotek och beroenden och distribuera allt som en enda paket.

Aspose.Cells Cloud-teamet har publicerat Docker-containern på <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> för att underlätta för Docker-användare.  

**Förutsättningar** – Se till att Docker Engine ≥ 20.x är installerat och att ditt operativsystem (Windows 10/Server 2019/2022 eller en supporterad Linux-distribution) uppfyller kraven. En valfri licensnyckel kan tillhandahållas för att köra i licensläge.

- Docker Engine ≥ 20.x installerat  
- Stödd OS (Windows 10/Server 2019/2022 eller en Linux-distribution)  
- Valfri licensnyckel för licensläge  

## Containerns konfiguration

### Nödvändiga volymer

| Monteringsväg i containern | Beskrivning |
| :--- | :--- |
| C:\fonts | Mapp med typsnitt som kommer att användas för att rendera dokument |
| C:\data | Mapp för fillagring |

**Alternativ för Linux/macOS** – Använd `/fonts` och `/data` i containern och mappa dem till värdkataloger såsom `/home/user/fonts` och `/home/user/data` vid körning av containern.

### Parametrar

| Namn | Beskrivning |
| :--- | :--- |
| LicensePublicKey | Offentlig nyckel för licensen |
| LicensePrivateKey | Privat nyckel för licensen |

Om **License**-parametrarna utelämnas körs appen i provläge.

### 1. Hämta Aspose.Cells Cloud-avbildningen

```bash
# Hämta en specifik version av Aspose.Cells Cloud-avbildningen
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Hämta Aspose.Cells Cloud-avbildning för Windows Server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Hämta Aspose.Cells Cloud-avbildning för Windows Server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Hämta Aspose.Cells Cloud-avbildning för Windows 11
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **Obs:** För alltid att få den senaste utgåvan kan du också hämta `latest`-taggen: `docker pull aspose/cells-cloud:latest`.

### 2. Konfigurationer för Docker‑Compose-verktyget

Du kan skriva följande konfiguration i en **docker‑compose.yml**-fil:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # värd 5000 → container 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "dinOffentligaNyckel"
    LicensePrivateKey: "dinPrivataNyckel"
```

> **Obs:** Portmappningen `5000:80` innebär att API:et kommer att vara tillgängligt på `http://localhost:5000`.

### 3. Kör en Docker-container via kommandoraden

```bash
docker run \
  -e "LicensePublicKey=dinOffentligaNyckel" \
  -e "LicensePrivateKey=dinPrivataNyckel" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**Felsökning:**  
- **Portkonflikt:** Se till att port 5000 på värdmaskinen är ledig eller ändra mappningen till en oanvänd port.  
- **Misslyckad licensladdning:** Verifiera att den offentliga och privata nyckeln skickas korrekt som miljövariabler eller monteras som filer.  
- **Saknade typsnitt:** Om dokument renderas med felaktiga typsnitt, kontrollera att typsnittskatalogen är korrekt monterad och innehåller de nödvändiga typsnittsfilerna.

**Relaterade resurser:**  
- <a href="/sv/cells/api/">API-referens</a> | <a href="/sv/cells/license/">Licensaktiveringsguide</a> | <a href="/sv/cells/getting-started/">Kom igång-översikt</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Kör Aspose.Cells Cloud Docker-container",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "Hämta Docker-avbildningen",
      "text": "Kör `docker pull aspose/cells-cloud:<version>` för att ladda ner den nödvändiga avbildningen."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "Skapa en docker‑compose-fil",
      "text": "Definiera avbildningen, portar, volymer och licensmiljövariabler i `docker‑compose.yml`."
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "Kör containern",
      "text": "Kör `docker run` med lämpliga miljövariabler, volymmonteringar och portmappning."
    }
  ]
}
```
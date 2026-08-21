---
title: "Aspose.Cells Cloud Docker-användarhandbok: Drifta Aspose.Cells Cloud-applikationen på din egen privata infrastruktur."
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Docker-användarhandbok"
linktitle: "Docker"
type: docs
url: /docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: "Distribuera Aspose.Cells Cloud som en Docker-container på privat eller lokal infrastruktur, vilket möjliggör kalkylbladsbehandling (Excel, PDF, CSV, JSON, Markdown) utan att använda Asposes offentliga moln."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Docker-avbildning",
    "Spreadsheet-API",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Privat moln",
    "Distribuering",
  ]
weight: 30
---

Aspose.Cells Cloud är en molnbaserad tjänst för kalkylbladsbehandling som stöder skapande, redigering, konvertering och manipulation av filer i format som Excel. Den kan snabbt konfigureras som en oberoende tjänstemiljö genom Docker-distribution, vilket förenklar hantering av beroenden och plattformsoberoende distributionsprocesser.

Denna handbok innehåller en detaljerad introduktion till hela driftstegen – från förberedelse av miljö till tjänsteverifiering.

## Förberedelse av miljö

Innan du distribuerar Aspose.Cells Clouds Docker-container ska du se till att din lokala miljö uppfyller följande beroendekrav för att undvika distributionsfel på grund av saknade komponenter.

### Grundläggande beroendekomponenter

- **Docker Engine:** Den centrala körningsmotorn för containrar, ansvarig för att skapa och hantera containrar. Minsta version som krävs är **18.09.0**.
- **Operativsystem:** Vanliga operativsystem som stöder Docker

  | Operativsystemstyp | Version                   |
  | :----------------- | :------------------------ |
  | Windows            | Windows 10/11             |
  | Windows Server     | 2016 / 2019 / 2022        |
  | Linux              | CentOS 7+ / Ubuntu 20.04+ |

- **Hårdvaruresurser:** Se till att tjänsten körs stabil för att undvika krascher på grund av otillräckliga resurser.
  - CPU: 2 kärnor eller mer.
  - Minne: 4 GB eller mer.
  - Disk: 10 GB ledigt utrymme.

### Viktiga förutsättningar

- **Aspose-licens:** Registrera dig för ett officiellt Aspose-konto för att erhålla en giltig licens (du kan ansöka om en provversion eller köpa en kommersiell version). Utan licens kan tjänstens funktionalitet vara begränsad. Se [Licens](https://purchase.aspose.com/buy)-sidan för mer information.
- **Nätverksanslutning:** Se till att distributionsmiljön kan komma åt Docker Hub (för att hämta avbildningar).

## Hämta Aspose.Cells Cloud Docker-avbildningen

Aspose.Cells Cloud-avbildningen är värd på Docker Hub och kan hämtas direkt med kommandot `docker pull`, utan att behöva bygga den manuellt.

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

## Kör Aspose.Cells Cloud Docker-container

### Körparametrar

| Namn                        | Beskrivning                                                                 | Anmärkning                                                   |
| --------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------ |
| LicensePublicKey            | Ställ in licensens offentliga nyckel när du använder Metered-faktureringsläget. | Endast effektivt när Metered-faktureringsläget används.     |
| LicensePrivateKey           | Ställ in licensens privata nyckel när du använder Metered-faktureringsläget. | Endast effektivt när Metered-faktureringsläget används.     |
| storagesCredentialsFilePath | Sökväg till konfigurationsfilen för lagring. Standardfil är `./storageResource.json`. |                                                              |
| LicenseFile                 | Ställ in licensfilen när du använder LicenseFile-faktureringsläget.         | Endast effektivt när LicenseFile-faktureringsläget används. |
| AccessToken                 | Token för åtkomst till API:t.                                                | Om tomt krävs ingen tokenverifiering.                         |

### Körkommando

Att köra containern i provläge är så enkelt som detta:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

För full funktionalitet, erhåll en [Metered-licens](https://purchase.aspose.com/faqs/licensing/metered/) och montera en värdmapp för fillagring. Här är hur körkommandot ser ut i detta fall:

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

### API-referens – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### Exponera port

| Port | Beskrivning                                 | Krävs  |
| ---- | ------------------------------------------- | ------ |
| 5000 | Mapp med typsnitt som används för att rendera dokument | ja     |

### Krävda volymer

| Monteringssökväg i container | Beskrivning                                 | Krävs | Anmärkning                                                     |
| ---------------------------- | ------------------------------------------- | ----- | -------------------------------------------------------------- |
| C:\fonts                     | Mapp med typsnitt som används för att rendera dokument | nej   | Lös kalkylblads-/Excel-problem orsakade av saknade typsnitt.  |
| C:\data                      | Mapp för fillagring                         | nej   | Ökar lagringsutrymmet för enklare filhantering och åtkomst.   |

## Referensdokument

- [Aspose.Cells Cloud Docker-container – kärnfunktioner](https://docs.aspose.cloud/cells/docker-container-features/)
- [Hur man konfigurerar lagring för Aspose.Cells Cloud Docker-container](https://docs.aspose.cloud/cells/docker/storage/)
- [Hur man kör Aspose.Cells Cloud Docker-container](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
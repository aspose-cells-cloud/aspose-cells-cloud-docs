---
title: "Hämta Aspose.Cells Cloud Docker-avbildning"  
second_title: "Dokument"  
ArticleTitle: "Hämta Aspose.Cells Cloud Docker-avbildning"  
linktitle: "Hämta avbildning"  
type: docs  
url: /sv/docker/downloads/
description: "Hämta de senaste Aspose.Cells Cloud Docker-avbildningarna för Windows Server 2016/2019 och Linux. Följ steg-för-steg-instruktioner, förutsättningar och säkerhetstips för att köra containern lokalt."  
weight: 30  
keywords: "Aspose.Cells, moln, Docker, container, avbildning, hämta, Windows Server, Linux, REST API"  
---  

## Översikt  

`aspose/cells-cloud` – den officiella Docker-avbildningen som värdar **Aspose.Cells Clouds** REST API. Avbildningen låter dig köra den fullständiga kalkylbladshandteringsmotorn inom en container, vilket möjliggör offlinelägen eller privata molndistributioner utan att behöva förlita sig på Asposes offentliga molntjänster.  

**Senast uppdaterad:** 2026‑06‑30  

**Snabbstartskontrollista**

- Verifiera att Docker Engine-versionen är 20.10 eller senare.  
- Hämta lämplig avbildning för ditt operativsystem (se avsnitten nedan).  
- Ställ in miljövariablerna `ASPOSE_CLIENT_ID` och `ASPOSE_CLIENT_SECRET`.  
- Kör containern med port 8080 mappad till den interna porten 80.  

---  

## Förutsättningar  

| Krav | Detaljer |
|------|----------|
| **Docker Engine** | Docker 20.10 eller senare installerat på värdens operativsystem. |
| **Operativsystem** | Windows Server 2016, Windows Server 2019 eller någon modern Linux-distribution. |
| **Docker Hub-åtkomst** | Ett aktivt Docker Hub-konto (valfritt men rekommenderas för privata avbildningar). Kör `docker login` om du behöver hämta från ett privat förråd. |
| **Aspose Cloud-referensuppgifter** | `ASPOSE_CLIENT_ID` och `ASPOSE_CLIENT_SECRET` – skaffa dem från Aspose Clouds instrumentpanel. |

> **Tips:** Verifiera Docker-installationen med `docker --version`.  

---  

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---  

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---  

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---  

## Kör containern  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=DIN_KLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=DIN_KLIENT_HEMLIGHET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **Miljövariabler** – `ASPOSE_CLIENT_ID` och `ASPOSE_CLIENT_SECRET` anger referensuppgifterna som krävs av API:et.  
* **Portmappning** – Containern exponerar port 80; mappa den till en värdport (t.ex. 8080) för att nå tjänsten.  
* **Fördjupat läge (`-d`)** – Kör containern i bakgrunden.  

---  

## Versionering och uppdateringar  

| OS | Tagg | Utgivningsdatum | Sätt att hämta den senaste |
|----|------|-----------------|----------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:linux.latest` |

> **Obs!** Taggen `21.9` är den aktuella stabila utgåvan. Använd taggen `latest` eller se [Aspose.Cells Clouds utgivningsanteckningar](/cells/release-notes/) för nyare versioner.  

---  

## Verifikation och säkerhet  

* **Kontroll av avbildningsdigest**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **Sårbarhetsskanning** (rekommenderas)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **Bästa praxis** – Håll Docker uppdaterat, kör containrar med minsta nödvändiga behörigheter och skanna regelbundet avbildningar efter kända CVE.  

* **Strukturerat dataexempel (JSON‑LD)**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker-avbildning",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---  

## Vanliga problem och felsökning  

| Symptom | Möjlig orsak | Lösning |
|---------|--------------|---------|
| `docker: kommandot hittades inte` | Docker inte installerat eller PATH inte inställt | Installera Docker och starta om terminalen. |
| Autentiseringsfel vid hämtning | Saknad eller felaktig `docker login` | Kör `docker login` med giltiga Docker Hub-referensuppgifter. |
| Container avslutas omedelbart | Saknade nödvändiga miljövariabler | Ange `ASPOSE_CLIENT_ID` och `ASPOSE_CLIENT_SECRET` enligt beskrivningen i avsnittet **Kör containern**. |
| Portkonflikt på värd | Värdporten används redan | Välj en annan värdport (t.ex. `-p 8081:80`). |

---  

## Se även  

* [Aspose.Cells Cloud API-dokumentation](/cells/cloud/api/)  
* [Aspose.Cells Clouds utgivningsanteckningar](/cells/release-notes/) – detaljerad ändringslogg för version 21.9 och nyare.  
* [Aspose.Cells Docker-containerfunktioner](/cells/docker/features/)  
* [Aspose.Cells Docker-avbildningstagger](/cells/docker/tag-list/)  

---  

*Skapat av Aspose Clouds ingenjörsteam.*
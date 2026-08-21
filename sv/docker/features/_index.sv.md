---
title: "Aspose.Cells Cloud Docker – Core-funktionalitet: Konvertering av kalkylark, sammanslagning, delning, skyddning, datahantering med mera."
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Docker – Core-funktionalitet"
linktitle: "Funktioner"
type: docs
url: /sv/docker-container-features/
description: "Kör Aspose.Cells Cloud API lokalt med Aspose.Cells Cloud Docker Container – en Docker-baserad, containerniserad tjänst som erbjuder fullständig bearbetning av kalkylark, sekretess och offline-funktionalitet utan att använda Asposes offentliga molntjänster."
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - Konvertering av kalkylark
  - Excel- bearbetning
  - PDF-export
  - CSV-hantering
  - REST API
  - Containeriserad tjänst
  - Privat molntjänst
  - Offlinebearbetning
---

## Vad är Aspose.Cells Cloud Docker Container?

Aspose.Cells Cloud Docker Container är en containerniserad tjänst från Aspose som är baserad på Docker och som gör det möjligt att distribuera Aspose.Cells Cloud API-funktionalitet i lokala eller privata molnmiljöer utan att behöva använda Asposes offentliga molntjänster.

## Varför använda Aspose.Cells Cloud Docker Container?

Aspose.Cells Cloud Docker Container är en kraftfull containertjänst för kalkylarksbearbetning som stöder:

### Core-funktioner

- Läsning och skrivning av Excel-filer (XLS, XLSX, CSV, ODS etc.)
- Formelberäkningar, diagram, villkorsformatering, pivottabeller etc.
- Filformatskonvertering (t.ex. Excel till PDF, HTML, bilder etc.)
- Celloperationer, stilinställningar, arbetsblads hantering etc.

Aspose.Cells Cloud Docker Container inkapslar dessa funktioner som ett RESTful API och paketerar dem till en Docker-image, så att du kan köra dem på din egen infrastruktur.

### Huvudfördelar

| Fördelar                     | Beskrivning                                                                 |
| ---------------------------- | --------------------------------------------------------------------------- |
| Datasekretess och säkerhet   | All filbearbetning sker inom ditt privata nätverk; ingen behov av att ladda upp till en tredjeparts molntjänst. |
| Offline-tillgänglighet        | Fungerar oberoende av Aspose offentliga molntjänster, lämplig för intranät eller isolerade miljöer. |
| Skalbarhet                   | Enkel skalning uppåt via Docker/Kubernetes.                                |
| Enhetligt API                | Fullständig kompatibilitet med Aspose.Cells Cloud offentliga API; inga kodändringar krävs. |
| Licenstyrning                 | Stödjer två typer av auktorisering; välj den som passar din situation.     |

## Hur man använder Aspose.Cells Cloud Docker Container

Se användarhandboken — [Hur man använder Aspose.Cells Cloud Docker Container](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container).

**Förutsättningar**

- Docker Engine 20.10 eller senare installerat på värddatorn.  
- Minst 2 GB RAM och 2 CPU-kärnor tilldelade till containern för typiska arbetsbelastningar.  
- En giltig Aspose.Cells Cloud-licensfil (eller åtkomsttoken) placerad i en katalog som kommer att monteras i containern.

**Snabbstart**

1. Hämta Docker-image: `docker pull aspose/cells-cloud`.  
2. Kör containern och montera licens- och datakataloger, t.ex.:  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. Kom åt REST API via `http://localhost:8080/v3.0/`. För detaljerad API-användning, se [Aspose.Cells Cloud API-referens](https://docs.aspose.cloud/cells/api-reference/).

## Referensdokumentation

- [Hur man konfigurerar lagring för Aspose.Cells Cloud Docker Container.](https://docs.aspose.cloud/cells/docker/storage/)
---
title: "Så här kör du Aspose.Cells Cloud Docker-container"
second_title: "Dokument"
ArticleTitle: "Så här kör du Aspose.Cells Cloud Docker-container"
linktitle: "Kör container"
type: docs
url: /run-aspose-cells-cloud-docker-container/
description: "Lär dig hur du startar Aspose.Cells Cloud i en Docker-container på Windows Server 2022. Steg-för-steg-kommandon för utvärderingsläge, förbrukningsbaserad fakturering, licensbaserad fakturering, lagringskonfiguration och hälsokontroll."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, utvärderingsläge, förbrukningsbaserad fakturering, licensbaserad fakturering, lagringskonfiguration"
---

Aspose.Cells Cloud Docker tillhandahåller en klar-att-köra containeravbildning som värd för Aspose.Cells Cloud API lokalt eller i en privat molntjänst. Denna guide visar hur du startar container i tre vanliga licenseringslägen—**Utvärdering**, **Förbrukningsbaserad fakturering** och **Licensbaserad fakturering**—och inkluderar en variant som använder en åtkomsttoken. Alla kommandon är skrivna för PowerShell på Windows Server 2022; justera volymvägarna om du använder Linux.

**Förutsättningar**

- Docker Engine 20.10 eller senare installerad och igång.  
- PowerShell 5.1 eller PowerShell 7+.  
- Öppna port 5000 i containern (mappad till värddatorns port 47900) och se till att värdens brandvägg tillåter inkommande trafik på port 47900.  
- För lägen med förbrukningsbaserad eller licensbaserad fakturering, ha din `LicensePublicKey`, `LicensePrivateKey` eller en licensfil redo, eller en `AccessToken` om du använder token-läge.  
- En lokal mapp (t.ex. `C:\data`) som ska monteras som lagring för containern.

**Snabbstart (Utvärderingsläge)**  

Kör följande kommando för att starta containern i utvärderingsläge:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## Kör Aspose.Cells Cloud Docker-container i utvärderingsläge

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Containern körs i förgrunden och lyssnar på värddatorns port **47900**, som vidarebefordras till containerns interna port **5000**.

## Kör Aspose.Cells Cloud Docker-container i förbrukningsbaserat faktureringsläge

```powershell
# Windows Server 2022
# Förbrukningsbaserat faktureringsläge: ange LicensePublicKey och LicensePrivateKey som miljövariabler.
# Montera en lagringsmapp (värddator → container)
#   -v c:/data:c:/data
# Montera Windows-teckensnittsmappen så API:t kan komma åt systemteckensnitten
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Containern körs i bakgrundsläge (`-d`). Efter att den har startats kan du verifiera att tjänsten är nåbar:

```powershell
curl http://localhost:47900/v3.0/health
```

**Exempel på `storageResource.json`**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## Kör Aspose.Cells Cloud Docker-container i licensbaserat faktureringsläge

```powershell
# Windows Server 2022
# Licensbaserat faktureringsläge: ange en licensfil via miljövariabeln LicenseFile.
# Montera en lagringsmapp (värddator → container)
#   -v c:/data:c:/data
# Montera Windows-teckensnittsmappen
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

## Kör Aspose.Cells Cloud Docker-container med åtkomsttoken

```powershell
# Windows Server 2022
# Åtkomsttoken-läge: ange AccessToken tillsammans med eventuella nycklar för förbrukningsbaserad fakturering.
# Montera en lagringsmapp
#   -v c:/data:c:/data
# Montera Windows-teckensnittsmappen
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Efter att du har startat containern, bekräfta att tjänsten är operativ med samma hälsokontrollkommando som visades tidigare.

## Referensdokument

- [Så här konfigurerar du lagring för Aspose.Cells Cloud Docker-container.](https://docs.aspose.cloud/cells/docker/storage/)

---

### Felsökning

- **Hälsokontroll misslyckas** – Se till att port 47900 inte är blockerad av en brandvägg och att containern körs (`docker ps`).  
- **Licensfel** – Verifiera att värdena för `LicensePublicKey`, `LicensePrivateKey` eller `LicenseFile` är korrekta och att miljövariablerna skickas utan extra blanksteg.  
- **Lagring inte tillgänglig** – Bekräfta att värddatorns mapp (`c:/data`) finns och att Docker har behörighet att läsa/skriva till den.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Så här kör du Aspose.Cells Cloud Docker-container",
  "description": "Steg-för-steg-guide för att starta Aspose.Cells Cloud i en Docker-container på Windows Server 2022, med stöd för utvärderingsläge, förbrukningsbaserad fakturering, licensbaserad fakturering och åtkomsttoken-läge.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, utvärderingsläge, förbrukningsbaserad fakturering, licensbaserad fakturering, lagringskonfiguration"
}
</script>
---
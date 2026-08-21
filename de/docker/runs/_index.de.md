---
title: "So führen Sie den Aspose.Cells Cloud Docker-Container aus"
second_title: "Dokument"
ArticleTitle: "So führen Sie den Aspose.Cells Cloud Docker-Container aus"
linktitle: "Container ausführen"
type: docs
url: /run-aspose-cells-cloud-docker-container/
description: "Erfahren Sie, wie Sie Aspose.Cells Cloud in einem Docker-Container unter Windows Server 2022 starten. Schritt-für-Schritt-Befehle für Testmodus, verbrauchsbasierte Abrechnung, lizenzbasierte Abrechnung, Speicherkonfiguration und Gesundheitschecks."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, Testmodus, verbrauchsbasierte Abrechnung, lizenzbasierte Abrechnung, Speicherkonfiguration"
---

Aspose.Cells Cloud Docker stellt ein fertig ausführbares Container-Image bereit, das die Aspose.Cells Cloud-API lokal oder in einer privaten Cloud hostet. Dieser Leitfaden zeigt, wie Sie den Container in drei gängigen Lizenzierungsmodi – **Testmodus**, **verbrauchsbasierte Abrechnung** und **lizenzbasierte Abrechnung** – starten, sowie eine Variante, die ein Zugriffstoken verwendet. Alle Befehle sind für PowerShell unter Windows Server 2022 geschrieben; passen Sie die Volume-Pfade an, wenn Sie Linux verwenden.

**Voraussetzungen**

- Docker Engine 20.10 oder neuer installiert und ausgeführt.  
- PowerShell 5.1 oder PowerShell 7+.  
- Offener Port 5000 im Container (zugeordnet zum Hostport 47900), und stellen Sie sicher, dass die Host-Firewall eingehenden Datenverkehr auf Port 47900 zulässt.  
- Für verbrauchsbasierte oder lizenzbasierte Abrechnung: Bereiten Sie Ihren `LicensePublicKey`, `LicensePrivateKey` oder eine Lizenzdatei vor, oder verwenden Sie ein `AccessToken`, falls Sie den Token-Modus nutzen.  
- Ein lokaler Ordner (z. B. `C:\data`), der als Speicher für den Container eingebunden wird.

**Schnellstart (Testmodus)**  

Führen Sie den folgenden Befehl aus, um den Container im Testmodus zu starten:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## Aspose.Cells Cloud Docker-Container im Testmodus ausführen

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Der Container läuft im Vordergrund und lauscht am Hostport **47900**, der an den internen Containerport **5000** weitergeleitet wird.

## Aspose.Cells Cloud Docker-Container im verbrauchsbasierten Abrechnungsmodus ausführen

```powershell
# Windows Server 2022
# Verbrauchsbasierte Abrechnung: Legen Sie LicensePublicKey und LicensePrivateKey als Umgebungsvariablen fest.
# Binden Sie einen Speicherordner ein (Host → Container)
#   -v c:/data:c:/data
# Binden Sie den Windows-Schriftartenordner ein, damit die API auf Systemschriftarten zugreifen kann
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

Der Container läuft im Hintergrundmodus (`-d`). Nach dem Start können Sie überprüfen, ob der Dienst erreichbar ist:

```powershell
curl http://localhost:47900/v3.0/health
```

**Beispiel für `storageResource.json`**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## Aspose.Cells Cloud Docker-Container im lizenzbasierten Abrechnungsmodus ausführen

```powershell
# Windows Server 2022
# Lizenzbasierte Abrechnung: Geben Sie eine Lizenzdatei über die Umgebungsvariable LicenseFile an.
# Binden Sie einen Speicherordner ein (Host → Container)
#   -v c:/data:c:/data
# Binden Sie den Windows-Schriftartenordner ein
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

## Aspose.Cells Cloud Docker-Container mit Zugriffstoken ausführen

```powershell
# Windows Server 2022
# Zugriffstoken-Modus: Legen Sie AccessToken zusammen mit optionalen Schlüsseln für verbrauchsbasierte Abrechnung fest.
# Binden Sie einen Speicherordner ein
#   -v c:/data:c:/data
# Binden Sie den Windows-Schriftartenordner ein
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

Nach dem Start des Containers bestätigen Sie die Funktionsfähigkeit des Dienstes mit dem oben genannten Gesundheitscheck-Befehl.

## Referenzdokument

- [Konfiguration des Speichers für den Aspose.Cells Cloud Docker-Container.](https://docs.aspose.cloud/cells/docker/storage/)

---

### Fehlerbehebung

- **Gesundheitscheck fehlgeschlagen** – Stellen Sie sicher, dass Port 47900 nicht durch eine Firewall blockiert wird und der Container ausgeführt wird (`docker ps`).  
- **Lizenzfehler** – Überprüfen Sie, ob `LicensePublicKey`, `LicensePrivateKey` oder `LicenseFile` korrekt sind und ob die Umgebungsvariablen ohne zusätzliche Leerzeichen übergeben wurden.  
- **Speicher nicht erreichbar** – Bestätigen Sie, dass der Hostordner (`c:/data`) vorhanden ist und Docker Lese-/Schreibrechte darauf besitzt.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "So führen Sie den Aspose.Cells Cloud Docker-Container aus",
  "description": "Schritt-für-Schritt-Anleitung zum Starten von Aspose.Cells Cloud in einem Docker-Container unter Windows Server 2022, einschließlich Testmodus, verbrauchsbasierter Abrechnung, lizenzbasierter Abrechnung und Zugriffstoken-Modus.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, Testmodus, verbrauchsbasierte Abrechnung, lizenzbasierte Abrechnung, Speicherkonfiguration"
}
</script>
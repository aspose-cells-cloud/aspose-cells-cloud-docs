---
title: "Aspose.Cells Cloud Docker-Container ausführen – Pullen, Konfigurieren & Starten"
second_title: "Dokument"
ArticleTitle: "So führen Sie den Aspose.Cells Cloud Docker-Container aus"
LinkTitle: "Docker-Container"
type: docs
url: /de/getting-started/how-to-run-docker-container/
aliases: [/de/how-to-run-docker-container/]
description: "Erfahren Sie, wie Sie den Aspose.Cells Cloud Docker-Container unter Windows oder Linux pullen, konfigurieren und ausführen. Enthält Docker‑Compose YAML, Lizenzkonfiguration, Port-Mapping und Tipps zur Fehlerbehebung."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker-Container"
  - "Docker Compose"
  - "Lizenzschlüssel"
  - "Excel"
  - "Tabellenkalkulation"
  - "Cloud-API"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

Die Docker-Technologie wurde entwickelt, um den Bereitstellungsprozess von Anwendungen durch den Einsatz leichtgewichtiger Container zu automatisieren. Entwickler können mithilfe eines Docker-Containers eine Anwendung zusammen mit allen ihren Bibliotheken und Abhängigkeiten bündeln und alles als einzelnes Paket bereitstellen.

Das Team von Aspose.Cells Cloud hat den Docker-Container auf <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> veröffentlicht, um Docker-Nutzern die Arbeit zu erleichtern.

**Voraussetzungen** – Stellen Sie sicher, dass Docker Engine ≥ 20.x installiert ist und Ihr Betriebssystem (Windows 10/Server 2019/2022 oder eine unterstützte Linux-Distribution) die Anforderungen erfüllt. Optional kann ein Lizenzschlüssel bereitgestellt werden, um im lizenzierten Modus zu arbeiten.

- Docker Engine ≥ 20.x installiert  
- Unterstütztes Betriebssystem (Windows 10/Server 2019/2022 oder eine Linux-Distribution)  
- Optionaler Lizenzschlüssel für den lizenzierten Modus  

## Container-Konfiguration

### Erforderliche Volumes

| Mount-Pfad im Container | Beschreibung |
| :--- | :--- |
| C:\fonts | Ordner mit Schriftarten, die zur Darstellung von Dokumenten verwendet werden |
| C:\data | Ordner für Dateispeicherung |

**Alternative für Linux/macOS** – Verwenden Sie `/fonts` und `/data` im Container und ordnen Sie diese auf Host-Verzeichnisse wie `/home/user/fonts` und `/home/user/data` beim Ausführen des Containers ab.

### Parameter

| Name | Beschreibung |
| :--- | :--- |
| LicensePublicKey | Öffentlicher Schlüssel der Lizenz |
| LicensePrivateKey | Privater Schlüssel der Lizenz |

Wenn die **License**-Parameter weggelassen werden, läuft die Anwendung im Testmodus.

### 1. Aspose.Cells Cloud-Image pullen

```bash
# Spezifische Version des Aspose.Cells Cloud-Images pullen
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Aspose.Cells Cloud-Image für Windows Server 2019 pullen
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Aspose.Cells Cloud-Image für Windows Server 2022 pullen
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Aspose.Cells Cloud-Image für Windows 11 pullen
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **Hinweis:** Um immer die neueste Version zu erhalten, können Sie auch das Tag `latest` pullen: `docker pull aspose/cells-cloud:latest`.

### 2. Konfiguration für das Docker‑Compose-Tool

Sie können die folgende Konfiguration in einer Datei **docker‑compose.yml** schreiben:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # Host 5000 → Container 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **Hinweis:** Die Port-Zuordnung `5000:80` bedeutet, dass die API unter `http://localhost:5000` erreichbar ist.

### 3. Docker-Container über die Kommandozeile ausführen

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**Fehlerbehebung:**  
- **Portkonflikt:** Stellen Sie sicher, dass Port 5000 auf dem Host verfügbar ist, oder ändern Sie die Zuordnung auf einen ungenutzten Port.  
- **Lizenzladefehler:** Überprüfen Sie, ob öffentlicher und privater Schlüssel korrekt als Umgebungsvariablen übergeben oder als Dateien eingebunden wurden.  
- **Fehlende Schriftarten:** Wenn Dokumente mit falschen Schriftarten dargestellt werden, bestätigen Sie, dass das Schriftartenverzeichnis korrekt eingebunden ist und die erforderlichen Schriftartdateien enthält.

**Verwandte Ressourcen:**  
- <a href="/de/cells/api/">API-Referenz</a> | <a href="/de/cells/license/">Anleitung zur Lizenzaktivierung</a> | <a href="/de/cells/getting-started/">Übersicht „Erste Schritte“</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Aspose.Cells Cloud Docker-Container ausführen",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "Docker-Image pullen",
      "text": "Führen Sie `docker pull aspose/cells-cloud:<version>` aus, um das erforderliche Image herunterzuladen."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "Docker-Compose-Datei erstellen",
      "text": "Definieren Sie Image, Ports, Volumes und Lizenz-Umgebungsvariablen in `docker‑compose.yml`."
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "Container ausführen",
      "text": "Führen Sie `docker run` mit den entsprechenden Umgebungsvariablen, Volume-Mounts und Port-Zuordnungen aus."
    }
  ]
}
```
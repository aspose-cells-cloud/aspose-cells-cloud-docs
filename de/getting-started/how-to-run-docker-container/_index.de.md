---
title: "So führen Sie den Aspose.Cells Cloud Docker Container aus: Führen Sie den offiziellen Aspose.Cells Cloud Container in 3 Schritten aus: Pullen, Konfigurieren, Starten"
second_title: Documen
ArticleTitle: How to Run Aspose.Cells Cloud Docker Containe
LinkTitle: Docker Containe
type: docs
url: /de/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: So führen Sie den Docker Aspose.Cells Cloud-Container aus. Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Teilen, Schützen, für interne Objektvorgänge usw.
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, So führen Sie einen Docker-Container aus
---
 Der**Docker** Die Technologie ist darauf ausgelegt, die Bereitstellung der Anwendungen durch den Einsatz von leichtgewichtigen Containern zu automatisieren. Entwickler können einen**Docker-Container** um eine Anwendung mit allen ihren Bibliotheken und Abhängigkeiten zusammenzufassen und alles als einzelnes Paket bereitzustellen.

 Aspose.Cells Cloud-Team hat den Docker Container veröffentlicht auf[Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) um Docker-Benutzern die Arbeit zu erleichtern. In den folgenden Abschnitten erfahren Sie, wie Sie Docker-Befehle ausführen oder eine Konfiguration in eine YAML-Datei für das Docker-Compose-Tool schreiben.

## Containerkonfiguration

### Erforderliche Mengen

|Mount-Pfad im Container|Beschreibung|
|:- |:- |
|C:\Schriftarten|Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden|
|C:\data|Dateispeicherordner|

### Parameter

|Name|Beschreibung|
|:- |:- |
|LizenzPublicKey|Öffentlicher Schlüssel der Lizenz|
|LizenzPrivater Schlüssel|Privater Schlüssel der Lizenz|

Wenn die Parameter „Lizenz“ weggelassen werden, funktioniert die App im Testmodus.

### 1. Ziehen Sie das Cloud-Image Aspose.Cells

```bash
# Pull Aspose.Cells Cloud Image latest version
docker pull aspose/cells-cloud:latest
```

```powershell
# Pull Aspose.Cells Cloud Image  version on windows server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
# Pull Aspose.Cells Cloud Image  version on windows server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0 

# Pull Aspose.Cells Cloud Image  version on windows 11
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
```

### 2. Konfigurationen für das Docker-Compose-Tool

Sie können die folgenden Konfigurationen in Ihre YAML-Datei für das Docker-Compose-Tool schreiben:

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```

### 3. Führen Sie einen Docker-Container über die Befehlszeile aus

 Sie können einfach den folgenden Docker-Befehl ausführen, nachdem Sie den Container aus[Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

---
title: So führen Sie Docker Containe aus
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: So führen Sie den Docker Aspose.Cells Cloud-Container aus. Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Teilen, Schützen, für den Betrieb innerer Objekte usw
weight: 100
---
 Der**Docker** Die Technologie ist darauf ausgelegt, die Bereitstellung der Anwendungen mithilfe leichter Container zu automatisieren. Entwickler können a**Docker-Container** um eine Anwendung mit all ihren Bibliotheken und Abhängigkeiten zusammenzufassen und alles als ein einziges Paket bereitzustellen.

 Aspose.Cells Das Cloud-Team hat den Docker-Container veröffentlicht[Docker-Hub](https://hub.docker.com/r/aspose/cells-cloud) um den Docker-Benutzern die Arbeit zu erleichtern. In den folgenden Abschnitten erfahren Sie, wie Sie Docker-Befehle ausführen oder die Konfiguration in eine Yaml-Datei für das Docker-Compose-Tool schreiben.

## Containerkonfiguration

### Erforderliche Mengen

|Mountpfad im Container|Beschreibung|
|:- |:- |
|C:\fonts|Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden|
|C:\Daten|Dateispeicherordner|

### Parameter

|Name|Beschreibung|
|:- |:- |
|LicensePublicKey|Öffentlicher Schlüssel der Lizenz|
|LicensePrivateKey|Privater Schlüssel der Lizenz|


Wenn die Parameter „Lizenz“ weggelassen werden, funktioniert die App im Testmodus.


### Führen Sie einen Docker-Container über die Befehlszeile aus

 Sie können einfach den folgenden Docker-Befehl ausführen, nachdem Sie den Container abgerufen haben[Docker-Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Konfigurationen für das Docker-Compose Tool

Sie können die folgenden Konfigurationen in Ihre Yaml-Datei für das Docker-Compose-Tool schreiben:

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

---
title: So führen Sie Docker-Containe aus
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: So führen Sie Docker Aspose.Cells Cloud-Container aus. Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Aufteilen, Schützen, für interne Objektvorgänge usw.
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, So führen Sie einen Docker-Container aus
---
 Der**Docker**Die Technologie ist darauf ausgelegt, die Bereitstellung der Anwendungen durch den Einsatz von leichten Containern zu automatisieren. Entwickler können einen**Docker-Container** um eine Anwendung mit allen ihren Bibliotheken und Abhängigkeiten zusammenzufassen und alles als einzelnes Paket bereitzustellen.

 Aspose.Cells Cloud-Team hat den Docker Container veröffentlicht auf[Docker-Hub](https://hub.docker.com/r/aspose/cells-cloud) um es den Docker-Benutzern zu erleichtern. Die folgenden Abschnitte erklären Ihnen, wie Sie Docker-Befehle ausführen oder eine Konfiguration in eine YAML-Datei für das Docker-Compose-Tool schreiben.

## Containerkonfiguration

### Erforderliche Mengen

|Einhängepfad im Container|Beschreibung|
|:- |:- |
|C:\Schriftarten|Ordner mit Schriftarten, die zum Rendern von Dokumenten verwendet werden|
|C:\Daten|Dateiablageordner|

### Parameter

|Name|Beschreibung|
|:- |:- |
|LizenzPublicKey|Öffentlicher Schlüssel der Lizenz|
|LizenzPrivater Schlüssel|Privater Schlüssel der Lizenz|


Wenn die „Lizenz“-Parameter weggelassen werden, funktioniert die App im Testmodus.


### Ausführen eines Docker-Containers über die Befehlszeile

Sie können einfach den folgenden Docker-Befehl ausführen, nachdem Sie den Container aus[Docker-Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Konfigurationen für das Docker-Compose-Tool

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

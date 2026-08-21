---
title: "Aspose.Cells Cloud Docker Core-Funktionalität: Tabellenkalkulationskonvertierung, Zusammenführung, Aufteilung, Schutz, Datenverarbeitung und mehr."
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Docker Core-Funktionalität"
linktitle: "Funktionen"
type: docs
url: /de/docker-container-features/
description: "Führen Sie die Aspose.Cells Cloud API lokal mit dem Aspose.Cells Cloud Docker Container aus – einem Docker-basierten, containerisierten Dienst, der vollständige Tabellenkalkulationsverarbeitung, Datenschutz und Offline-Fähigkeit ohne Nutzung des öffentlichen Aspose-Clouds bietet."
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - Tabellenkalkulationskonvertierung
  - Excel-Verarbeitung
  - PDF-Export
  - CSV-Verarbeitung
  - REST API
  - Containerisierter Dienst
  - Private Cloud
  - Offline-Verarbeitung
---

## Was ist der Aspose.Cells Cloud Docker Container?

Der Aspose.Cells Cloud Docker Container ist ein containerisierter Dienst von Aspose, der auf Docker basiert und es ermöglicht, die Funktionalitäten der Aspose.Cells Cloud API in lokalen oder privaten Cloud-Umgebungen bereitzustellen, ohne auf die öffentlichen Cloud-Dienste von Aspose angewiesen zu sein.

## Warum den Aspose.Cells Cloud Docker Container verwenden?

Der Aspose.Cells Cloud Docker Container ist ein leistungsstarker Container für die Tabellenkalkulationsverarbeitung, der Folgendes unterstützt:

### Kernfunktionen

- Lesen und Schreiben von Excel-Dateien (XLS, XLSX, CSV, ODS usw.)
- Formelberechnungen, Diagramme, bedingte Formatierungen, Pivot-Tabellen usw.
- Formatkonvertierung (z. B. Excel zu PDF, HTML, Bilder usw.)
- Zelloperationen, Formatierungseinstellungen, Arbeitsblattverwaltung usw.

Der Aspose.Cells Cloud Docker Container verpackt diese Funktionen als RESTful API und stellt sie in einem Docker-Image bereit, sodass Sie ihn auf Ihrer eigenen Infrastruktur ausführen können.

### Hauptvorteile

| Vorteile                | Beschreibung                                                                 |
| ----------------------- | --------------------------------------------------------------------------- |
| Datensicherheit und -schutz | Alle Dateiverarbeitungen erfolgen innerhalb Ihres privaten Netzwerks; kein Upload zu einer externen Cloud erforderlich. |
| Offline-Verfügbarkeit   | Keine Abhängigkeit vom öffentlichen Aspose-Cloud; geeignet für Intranets oder isolierte Umgebungen. |
| Skalierbarkeit          | Einfache Skalierung über Docker/Kubernetes.                                 |
| Einheitliche API        | Volle Kompatibilität mit der öffentlichen Aspose.Cells Cloud API; keine Codeänderungen erforderlich. |
| Lizenzverwaltung        | Unterstützt zwei Arten der Autorisierung; wählen Sie die für Ihre Situation passende aus. |

## Wie verwendet man den Aspose.Cells Cloud Docker Container?

Weitere Informationen finden Sie im Benutzerhandbuch — [Wie verwendet man den Aspose.Cells Cloud Docker Container](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container).

**Voraussetzungen**

- Docker Engine 20.10 oder höher auf dem Hostsystem installiert.  
- Mindestens 2 GB RAM und 2 CPU-Kerne für den Container bei typischen Arbeitslasten.  
- Eine gültige Aspose.Cells Cloud-Lizenzdatei (oder Zugriffstoken) in einem Verzeichnis abgelegt, das in den Container eingebunden wird.

**Schnellstart**

1. Docker-Image herunterladen: `docker pull aspose/cells-cloud`.  
2. Container starten, wobei die Lizenz- und Datenverzeichnisse eingebunden werden, z. B.:  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. Auf die REST API unter `http://localhost:8080/v3.0/` zugreifen. Für detaillierte API-Nutzung siehe [Aspose.Cells Cloud API-Referenz](https://docs.aspose.cloud/cells/api-reference/).

## Referenzdokumentation

- [Konfiguration des Speichers für den Aspose.Cells Cloud Docker Container.](https://docs.aspose.cloud/cells/docker/storage/)
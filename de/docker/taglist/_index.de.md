---
title: "Aspose.Cells Cloud Docker-Image-Tags"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Docker-Image-Tags"
linktitle: "Image-Tags"
type: docs
url: /de/docker/tag-list/
description: "Finden Sie die neuesten Aspose.Cells Cloud Docker-Image-Tags für Windows Server (2016–2022) und Linux. Holen Sie sich Pull-Befehle, Architekturdetails und Upgrade-Hinweise an einer Stelle."
weight: 30
keywords:
  - "Aspose.Cells Cloud Docker-Image-Tags"
  - "Docker-Pull-Befehle"
  - "Windows Server Docker-Tags"
  - "Linux Docker-Tags"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud stellt bereitsfertige Docker-Images für Windows Server (2016, 2019, 2022) und Linux zur Verfügung.  
Jedes Image ist mit einem **Tag** versehen, das die Produktfreigabe und das Zielbetriebssystem identifiziert.  
Nutzen Sie die nachfolgenden Tags, um genau das gewünschte Image abzurufen, und nutzen Sie die begleitenden Pull- und Ausführungsbeispiele für eine schnelle Inbetriebnahme.

*Letzte Aktualisierung: 2026-07-01*

**Voraussetzungen:** Stellen Sie sicher, dass Docker Engine 20.10 oder höher installiert ist und Sie über einen gültigen Aspose.Cells Cloud-Lizenzschlüssel verfügen. Die Images wurden für die angegebenen Windows Server-Versionen bzw. Linux x64 entwickelt.

## Windows Server 2016-Images ##

Tags | Architektur | Dockerfile | Hinweis
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile nicht veröffentlicht – Einzelheiten zur Erstellung finden Sie in den [Release Notes](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016). | Für Windows Server 2016 ist kein neueres Tag geplant; dies ist die letzte veröffentlichte Version.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

Zusätzliche Ressourcen: [Docker-Download](/cells/docker/downloads/), [Release Notes](/cells/release-notes/), [Voraussetzungen](/cells/docker/prerequisites/).  
Weitere Informationen finden Sie im [Docker-Überblick](/cells/docker/).

## Windows Server 2019-Images ##

Tags | Architektur | Dockerfile | Hinweis
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile nicht veröffentlicht – Einzelheiten zur Erstellung finden Sie in den [Release Notes](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019). | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

Zusätzliche Ressourcen: [Docker-Download](/cells/docker/downloads/), [Release Notes](/cells/release-notes/), [Voraussetzungen](/cells/docker/prerequisites/).  
Weitere Informationen finden Sie im [Docker-Überblick](/cells/docker/).

## Windows Server 2022-Images ##

Tags | Architektur | Dockerfile | Hinweis
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile nicht veröffentlicht – Einzelheiten zur Erstellung finden Sie in den [Release Notes](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022). | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

Zusätzliche Ressourcen: [Docker-Download](/cells/docker/downloads/), [Release Notes](/cells/release-notes/), [Voraussetzungen](/cells/docker/prerequisites/).  
Weitere Informationen finden Sie im [Docker-Überblick](/cells/docker/).

## Linux-Images ##

Tags | Architektur | Dockerfile | Hinweis
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile nicht veröffentlicht – Einzelheiten zur Erstellung finden Sie in den [Release Notes](https://github.com/aspose-cells/dockerfiles/tree/main/linux). | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

Zusätzliche Ressourcen: [Docker-Download](/cells/docker/downloads/), [Release Notes](/cells/release-notes/), [Voraussetzungen](/cells/docker/prerequisites/).  
Weitere Informationen finden Sie im [Docker-Überblick](/cells/docker/).

**Versionsänderungsprotokoll**

Tag | Änderungen
---|---
`ltsc2016.23.5.0` | Letzte Freigabe für Windows Server 2016; enthält Sicherheitspatches und Leistungsverbesserungen.
`ltsc2019.25.10.0` | Aktualisiert auf Aspose.Cells 25.10.0; neue Formelunterstützung und Fehlerbehebungen.
`ltsc2022.25.10.0` | Entsprechend dem 2019-Tag, optimiert für die Windows Server 2022-Laufzeitumgebung.
`linux.25.10.0` | Basis-Linux-Image mit Aspose.Cells 25.10.0; enthält aktualisierte Abhängigkeiten und Linux-spezifische Optimierungen.
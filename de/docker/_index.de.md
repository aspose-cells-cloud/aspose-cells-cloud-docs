---
title: "Aspose.Cells Cloud Docker-Bedienungsanleitung: Bereitstellen der Aspose.Cells Cloud-Anwendung auf Ihrer eigenen privaten Infrastruktur."
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Docker-Bedienungsanleitung"
linktype: "Docker"
type: docs
url: /de/docker-developer-guide/
aliases: [  /de/docker/ , /de/docker/run/ ]
description: "Bereitstellen von Aspose.Cells Cloud als Docker-Container auf privater oder on‑premises‑Infrastruktur, um die Verarbeitung von Tabellendokumenten (Excel, PDF, CSV, JSON, Markdown) ohne Nutzung des öffentlichen Cloud-Dienstes von Aspose zu ermöglichen."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Docker-Image",
    "Tabellen-API",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Private Cloud",
    "Bereitstellung",
  ]
weight: 30
---

Aspose.Cells Cloud ist ein cloudbasierter Dienst zur Verarbeitung von Tabellendokumenten, der die Erstellung, Bearbeitung, Konvertierung und Manipulation von Dateien in Formaten wie Excel unterstützt. Mithilfe einer Docker-Bereitstellung kann er schnell als eigenständige Serviceumgebung eingerichtet werden, was die Verwaltung von Abhängigkeiten und plattformübergreifende Bereitstellungsprozesse vereinfacht.

Diese Anleitung enthält eine detaillierte Einführung in alle Schritte – von der Umgebungsvorbereitung bis zur Dienstverifizierung.

## Umgebungsvorbereitung

Bevor Sie den Aspose.Cells Cloud Docker-Container bereitstellen, stellen Sie sicher, dass Ihre lokale Umgebung die folgenden Abhängigkeitsanforderungen erfüllt, um Bereitstellungsfehler aufgrund fehlender Komponenten zu vermeiden.

### Grundlegende Abhängigkeitskomponenten

- **Docker Engine:** Die Kern-Engine für Container-Laufzeitumgebungen, die für das Erstellen und Verwalten von Containern zuständig ist. Mindestanforderung an die Version: **18.09.0**.
- **Betriebssysteme:** gängige Betriebssysteme mit Docker-Unterstützung

  | Betriebssystemtyp     | Version                   |
  | :-------------------- | :------------------------ |
  | Windows               | Windows 10/11             |
  | Windows Server        | 2016 / 2019 / 2022        |
  | Linux                 | CentOS 7+ / Ubuntu 20.04+ |

- **Hardwareressourcen:** Stellen Sie sicher, dass der Dienst reibungslos läuft, um Abstürze aufgrund unzureichender Ressourcen zu vermeiden.
  - CPU: mindestens 2 Kerne
  - RAM: mindestens 4 GB
  - Festplatte: mindestens 10 GB freier Speicherplatz

### Wichtige Voraussetzungen

- **Aspose-Lizenz:** Registrieren Sie sich für einen Aspose-Konto, um eine gültige Lizenz zu erhalten (Sie können eine Testversion beantragen oder eine kommerzielle Lizenz erwerben). Ohne Lizenz kann die Funktionalität des Dienstes eingeschränkt sein. Weitere Informationen finden Sie auf der [Lizenz](https://purchase.aspose.com/buy)-Seite.
- **Netzwerkverbindung:** Stellen Sie sicher, dass Ihre Bereitstellungsumgebung Zugriff auf Docker Hub hat (zum Herunterladen von Images).

## Abrufen des Aspose.Cells Cloud Docker-Images

Das Aspose.Cells Cloud-Image ist auf Docker Hub gehostet und kann direkt mit dem Befehl `docker pull` abgerufen werden – eine manuelle Erstellung ist nicht erforderlich.

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## Ausführen des Aspose.Cells Cloud Docker-Containers

### Parameter für die Ausführung

| Name                        | Beschreibung                                                              | Anmerkung                                                    |
| --------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------ |
| LicensePublicKey            | Öffentlicher Schlüssel der Lizenz bei Verwendung des Metered-Abrechnungsmodus. | Nur wirksam, wenn der Metered-Abrechnungsmodus verwendet wird. |
| LicensePrivateKey           | Privater Schlüssel der Lizenz bei Verwendung des Metered-Abrechnungsmodus. | Nur wirksam, wenn der Metered-Abrechnungsmodus verwendet wird. |
| storagesCredentialsFilePath | Pfad zur Speicherkonfigurationsdatei. Standarddatei ist `./storageResource.json`. |                                                              |
| LicenseFile                 | Lizenzdatei bei Verwendung des LicenseFile-Abrechnungsmodus.              | Nur wirksam, wenn der LicenseFile-Abrechnungsmodus verwendet wird. |
| AccessToken                 | Token zum Zugriff auf die API.                                            | Falls leer, ist keine Token-Validierung erforderlich.        |

### Ausführungsbefehl

Das Ausführen des Containers im Testmodus ist so einfach wie folgt:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Für den vollen Funktionsumfang beschaffen Sie eine [Metered-Lizenz](https://purchase.aspose.com/faqs/licensing/metered/) und hängen einen Hostordner für die Dateispeicherung ein. Der Ausführungsbefehl sieht in diesem Fall wie folgt aus:

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### API-Referenz – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### Freigegebener Port

| Port | Beschreibung                                  | Erforderlich |
| ---- | --------------------------------------------- | ------------ |
| 5000 | Ordner mit Schriftarten zur Dokumentenrenderung | ja           |

### Erforderliche Volumes

| Mount-Pfad im Container | Beschreibung                                  | Erforderlich | Anmerkung                                                      |
| ----------------------- | --------------------------------------------- | ------------ | -------------------------------------------------------------- |
| C:\fonts                | Ordner mit Schriftarten zur Dokumentenrenderung | nein         | Behebt Probleme bei Tabellen/Excel aufgrund fehlender Schriftarten. |
| C:\data                 | Ordner für Dateispeicherung                   | nein         | Erhöht den Speicherplatz für einfachere Dateiverwaltung und -zugriff. |

## Referenzdokumentation

- [Kernfunktionen des Aspose.Cells Cloud Docker-Containers](https://docs.aspose.cloud/cells/docker-container-features/)
- [Konfigurieren des Speichers für Aspose.Cells Cloud Docker-Container](https://docs.aspose.cloud/cells/docker/storage/)
- [Ausführen des Aspose.Cells Cloud Docker-Containers](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
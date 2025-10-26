---
title: "Aspose.Cells Cloud SDK für Node.js: Konvertieren, Zusammenführen, Teilen, Schützen, Suchen, Ersetzen und mehr"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells Cloud SDK für Node.j
type: docs
url: /de/available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK für Node.js bietet echte plattformübergreifende Leistung: Ein Import bietet Windows, Linux- und macOS-Entwicklern die gleiche fließende API zum Erstellen, Konvertieren, Zusammenführen, Aufteilen, Schützen und Bearbeiten jedes Excel Objekts – keine Office Installation erforderlich und keine plattformspezifischen Anpassungen erforderlich"
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK für Node.js, Cloud SDK für Node.js, REST, Diagramm, Pivot-Tabelle, Tabellen-/Listenobjekt, Tabellenkalkulation konvertieren, PDF, CSV, Json, Markdown, Zusammenführen, Teilen, Schützen, Suchen, Ersetzen
---
Das SDK ist Open Source und steht unter der MIT-Lizenz. Sie können darauf zugreifen[der Quellcode der Node-Bibliothek für Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **So verwenden Sie die Node-Bibliothek der Aspose.Cells Cloud**

Aspose.Cells Cloud SDK für Node ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, Microsoft Excel-Dateien mit der Programmiersprache Node zu bearbeiten und zu verarbeiten. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.

In diesem Artikel erfahren Sie, wie Sie mit dem Aspose.Cells Cloud SDK für Node einige gängige Aufgaben ausführen, z. B. eine neue Excel-Arbeitsmappe erstellen, Daten in Zellen einfügen und die geänderte Arbeitsmappe in der Cloud speichern.

## Erste Schritte

 Bevor Sie das Aspose.Cells Cloud SDK für Go verwenden können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Weitere Informationen finden Sie unter[der Artikel](https://docs.aspose.cloud/cells/quickstart/) auf der Website Aspose, um Ihre Client-ID und Ihr Client-Geheimnis zu erhalten.

## So installieren Sie das Node-Paket für Aspose.Cells Cloud

Sie können das Aspose.Cells Cloud SDK für Node mit npm installieren. Nachfolgend finden Sie die Schritte für npm:

```Powershell

npm install asposecellscloud

```

## So fügen Sie Abhängigkeiten in der Paketkonfiguration für Aspose.Cells Cloud hinzu

Knotenkonfigurationsdatei: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## So verwenden Sie das Node-Paket zum Konvertieren von XLSX in andere Formate

- Importieren Sie Aspose.Cells Cloud-Bibliothek
 Beginnen Sie, indem Sie das erforderliche Paket aus dem Aspose.Cells Cloud NodeJS SDK in Ihr Projekt importieren.
- Konfigurieren Sie den API-Client mit Anmeldeinformationen
 Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Geheimnis.
- Konvertierungsparameter vorbereiten
 Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.
- Arbeitsmappenkonvertierung ausführen
 Rufen Sie den Konvertierungsprozess mit der Methode PostConvertWorkbook auf und verarbeiten Sie die Antwort.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}

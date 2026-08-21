---
title: "Aspose.Cells Cloud SDK für Node.js: Konvertieren, Zusammenführen, Teilen, Schützen, Suchen, Ersetzen und mehr."
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud SDK für Node.js: Konvertieren, Zusammenführen, Teilen, Schützen, Suchen, Ersetzen und mehr."
linktitle: "Aspose.Cells Cloud SDK für Node.js"
type: docs
url: /de/available-sdks/aspose-cells-cloud-node/
description: "Das Aspose.Cells Cloud SDK für Node.js bietet echte plattformübergreifende Leistung: Ein einziger Import stellt Windows-, Linux- und macOS-Entwicklern dieselbe flüssige API zur Verfügung, um jedes Excel-Objekt zu erstellen, zu konvertieren, zusammenzuführen, zu teilen, zu schützen und zu bearbeiten – keine Office-Installation erforderlich und keine plattformspezifischen Anpassungen nötig."
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK für Node.js, Cloud SDK für Node.js, REST, Diagramm, Pivot-Tabelle, Tabellen-/Listenobjekt, Tabellendokument konvertieren, PDF, CSV, JSON, Markdown, Zusammenführen, Teilen, Schützen, Suchen, Ersetzen
---

Das SDK ist Open Source und unter der MIT-Lizenz lizenziert. Sie können den Quellcode der Node-Bibliothek für Aspose.Cells Cloud [hier](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) abrufen.

# **So verwenden Sie die Node-Bibliothek von Aspose.Cells Cloud**

Das Aspose.Cells Cloud SDK für Node ist eine leistungsstarke Bibliothek, mit der Entwickler Microsoft Excel-Dateien mithilfe der Node-Programmiersprache bearbeiten und verarbeiten können. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.

In diesem Artikel zeigen wir Ihnen, wie Sie das Aspose.Cells Cloud SDK für Node nutzen, um einige gängige Aufgaben auszuführen, wie z. B. das Erstellen einer neuen Excel-Arbeitsmappe, das Einfügen von Daten in Zellen und das Speichern der bearbeiteten Arbeitsmappe in der Cloud.

## Erste Schritte

Bevor Sie mit der Verwendung des Aspose.Cells Cloud SDK für Go beginnen können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Weitere Informationen finden Sie im [Artikel](https://docs.aspose.cloud/cells/quickstart/) auf der Aspose-Website, um Ihre Client-ID und Ihren Client-Secret zu erhalten.

## So installieren Sie das Node-Paket für Aspose.Cells Cloud

Sie können das Aspose.Cells Cloud SDK für Node über npm installieren. Nachfolgend finden Sie die Schritte für npm:

```Powershell

npm install asposecellscloud

```

## So fügen Sie Abhängigkeiten in die Paketkonfiguration für Aspose.Cells Cloud hinzu

Node-Konfigurationsdatei: package.json

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

## So verwenden Sie das Node-Paket, um Xlsx in andere Formate zu konvertieren

- Aspose.Cells Cloud-Bibliothek importieren  
  Beginnen Sie damit, das erforderliche Paket aus dem Aspose.Cells Cloud NodeJS SDK in Ihr Projekt zu importieren.
- API-Client mit Anmeldeinformationen konfigurieren  
  Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Secret.
- Konvertierungsparameter vorbereiten  
  Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.
- Arbeitsmappenkonvertierung ausführen  
  Rufen Sie den Konvertierungsprozess mit der Methode PostConvertWorkbook auf und verarbeiten Sie die Antwort.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
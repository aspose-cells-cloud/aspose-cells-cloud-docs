---
title: Aspose.Cells Cloud SDK für G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/available-sdks/aspose-cells-cloud-go/
description: Aspose.Cells Cloud SDK für Go bietet starke plattformübergreifende Unterstützung für Go-Entwickler und erleichtert die Integration und Verwendung für Windows, Linux oder macOS. Es unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Aufteilen, Schützen, für interne Objektoperationen usw.
weight: 30
kwords: Go, Excel, Office Cloud, REST API, Diagramm, Pivot-Tabelle, Tabelle, Kalkulationstabelle, PDF, CSV, Json, Markdown
---
 Das SDK ist Open Source und unter der MIT-Lizenz lizenziert. Sie können auf den Quellcode der Go-Bibliothek für Aspose.Cells Cloud zugreifen[Hier](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **So verwenden Sie die Go-Bibliothek von Aspose.Cells Cloud**

Aspose.Cells Cloud SDK für Go ist eine leistungsstarke Bibliothek, mit der Entwickler Microsoft Excel-Dateien mit der Programmiersprache Go bearbeiten und verarbeiten können. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.

In diesem Artikel untersuchen wir, wie Sie mit dem Aspose.Cells Cloud SDK für Go einige gängige Aufgaben ausführen, z. B. eine neue Excel-Arbeitsmappe erstellen, Daten in Zellen einfügen und die geänderte Arbeitsmappe in der Cloud speichern.

## **Erste Schritte**

 Bevor Sie das Aspose.Cells Cloud SDK für Go verwenden können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Weitere Informationen finden Sie unter[der Artikel](https://docs.aspose.cloud/cells/quickstart/) auf der Website Aspose, um Ihre Client-ID und Ihr Client-Geheimnis zu erhalten.

## So installieren Sie das Go-Paket für Aspose.Cells Cloud

Sie können Aspose.Cells Cloud SDK für Go mit dem Befehl `go get` installieren. Öffnen Sie Ihr Terminal oder Ihre Eingabeaufforderung und führen Sie den folgenden Befehl aus:

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

Dadurch wird die neueste Version des SDK heruntergeladen und in Ihrem Go-Arbeitsbereich installiert.


## So importieren Sie die Go-Bibliothek in Ihr Projekt


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## So verwenden Sie das Go-Paket zum Konvertieren von Xlsx in PDF

- Importieren Sie Aspose.Cells Cloud-Bibliothek
Importieren Sie zunächst das erforderliche Paket aus dem Aspose.Cells Cloud Go SDK in Ihr Projekt.
- Konfigurieren Sie den API-Client mit Anmeldeinformationen
 Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Geheimnis.
- Konvertierungsparameter vorbereiten
 Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.
- Arbeitsmappenkonvertierung ausführen
 Rufen Sie den Konvertierungsprozess mit der Methode PostConvertWorkbook auf und verarbeiten Sie die Antwort.

### **Beispielcode**

```golang
package main

import (
	"os"
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
    remoteFolder := "TestData/In"

    localName := "Book1.xlsx"
    remoteName := "Book1.xlsx"

    format := "pdf"

    var mapFiles map[string]string       
    mapFiles = make(map[string]string)
    mapFiles[localName]=  localName 

    request := new (asposecellscloud.PutConvertWorkbookRequest)
    request.File =         mapFiles    
    request.Format =         format    
    _, httpResponse, err := instance.PutConvertWorkbook(request)
    if err != nil {
      print(err)
    } else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
      print("Test fail")
    }
}

```

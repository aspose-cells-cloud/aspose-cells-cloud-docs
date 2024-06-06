---
title: Aspose.Cells Cloud SDK für Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Aufteilen, Schützen, für interne Objektoperationen usw.
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Net
---
 Das SDK ist Open Source und unter der MIT-Lizenz lizenziert. Sie können auf den Quellcode der Net-Bibliothek für Aspose.Cells Cloud zugreifen[Hier](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).


# **So verwenden Sie die Net-Bibliothek von Aspose.Cells Cloud**

Aspose.Cells Cloud SDK für Net ist eine leistungsstarke Bibliothek, mit der Entwickler Microsoft Excel-Dateien mit der Programmiersprache Net bearbeiten und verarbeiten können. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.

In diesem Artikel untersuchen wir, wie Sie mit Aspose.Cells Cloud SDK for Net einige gängige Aufgaben ausführen, z. B. eine neue Excel-Arbeitsmappe erstellen, Daten in Zellen einfügen und die geänderte Arbeitsmappe in der Cloud speichern.

## Erste Schritte

 Bevor Sie das Aspose.Cells Cloud SDK für Go verwenden können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Weitere Informationen finden Sie unter[der Artikel](https://docs.aspose.cloud/cells/quickstart/) auf der Website Aspose, um Ihre Client-ID und Ihr Client-Geheimnis zu erhalten.

## So installieren Sie das Net-Paket für Aspose.Cells Cloud

Sie können Aspose.Cells Cloud SDK für Net mit nuget installieren. Unten sind die Schritte für nuget aufgeführt:

```nuget

Install-Package Aspose.Cells-Cloud

```

Sie können Aspose.Cells Cloud SDK für Net auch mit dotnet installieren. Nachfolgend finden Sie die Schritte für dotnet:

```powershell

dotnet add package Aspose.Cells-Cloud 

```

## So verwenden Sie das Net-Paket zum Konvertieren von Xlsx in PDF

- Importieren Sie Aspose.Cells Cloud-Bibliothek
 Importieren Sie zunächst das erforderliche Paket aus dem Aspose.Cells Cloud DotNet SDK in Ihr Projekt.
- Konfigurieren Sie den API-Client mit Anmeldeinformationen
 Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Geheimnis.
- Konvertierungsparameter vorbereiten
 Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.
- Arbeitsmappenkonvertierung ausführen
 Rufen Sie den Konvertierungsprozess mit der Methode PostConvertWorkbook auf und verarbeiten Sie die Antwort.

### **Beispielcode**

```CSharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Request;
using System;
using System.IO;
using System.Collections.Generic;

CellsApi cellsApi = new CellsApi("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx");
string remoteFolder = "TestData/In";

string localName = "Book1.xlsx";
string remoteName = "Book1.xlsx";

this.UploadFile( localName, remoteFolder + "/" + remoteName, "");

IDictionary<string, Stream> mapFiles =new Dictionary<string,Stream>(); 
AddFileParameter(localName,mapFiles);       
var request = new PutConvertWorkbookRequest(
    file: mapFiles,
    format: format
);
this.CellsApi.PutConvertWorkbook(request);
```

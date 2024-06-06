---
title: Aspose.Cells Cloud SDK für Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Aufteilen, Schützen, für interne Objektoperationen usw.
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Node
---
 Das SDK ist Open Source und unter der MIT-Lizenz lizenziert. Sie können auf den Quellcode der Node-Bibliothek für Aspose.Cells Cloud zugreifen[Hier](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).


# **So verwenden Sie die Node-Bibliothek von Aspose.Cells Cloud**

Aspose.Cells Cloud SDK für Node ist eine leistungsstarke Bibliothek, mit der Entwickler Microsoft Excel-Dateien mit der Programmiersprache Node bearbeiten und verarbeiten können. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.


In diesem Artikel untersuchen wir, wie Sie mit dem Aspose.Cells Cloud SDK für Node einige gängige Aufgaben ausführen, z. B. eine neue Excel-Arbeitsmappe erstellen, Daten in Zellen einfügen und die geänderte Arbeitsmappe in der Cloud speichern.

## Erste Schritte

 Bevor Sie das Aspose.Cells Cloud SDK für Go verwenden können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Weitere Informationen finden Sie unter[der Artikel](https://docs.aspose.cloud/cells/quickstart/) auf der Website Aspose, um Ihre Client-ID und Ihr Client-Geheimnis zu erhalten.

## So installieren Sie das Node-Paket für Aspose.Cells Cloud

Sie können Aspose.Cells Cloud SDK für Node mit npm installieren. Nachfolgend sind die Schritte für npm aufgeführt:


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

## So verwenden Sie das Node-Paket zum Konvertieren von Xlsx in PDF

- Importieren Sie Aspose.Cells Cloud-Bibliothek
 Beginnen Sie, indem Sie das erforderliche Paket aus dem Aspose.Cells Cloud NodeJS SDK in Ihr Projekt importieren.
- Konfigurieren Sie den API-Client mit Anmeldeinformationen
 Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Geheimnis.
- Konvertierungsparameter vorbereiten
 Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.
- Arbeitsmappenkonvertierung ausführen
 Rufen Sie den Konvertierungsprozess mit der Methode PostConvertWorkbook auf und verarbeiten Sie die Antwort.

```javascript
var fs = require('fs');
var path = require('path');
const _ = require('asposecellscloud');

const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret,"v3.0",process.env.CellsCloudApiBaseUrl);

var remoteFolder = "TestData/In"
  
var localName = "Book1.xlsx"
var remoteName = "Book1.xlsx"

var localNameRequest = new  model.UploadFileRequest();
localNameRequest.uploadFiles ={localName:fs.createReadStream(localPath  + localName)};
localNameRequest.path = remoteFolder + "/" + remoteName ;
localNameRequest.storageName ="";
cellsApi.uploadFile(localNameRequest );
 
var format = "csv"

var mapFiles = {};           

 mapFiles[localName]= fs.createReadStream(localPath  +localName) ;

var request = new model.PutConvertWorkbookRequest();
request.file =  mapFiles;
request.format =  format;
return cellsApi.putConvertWorkbook(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});
```

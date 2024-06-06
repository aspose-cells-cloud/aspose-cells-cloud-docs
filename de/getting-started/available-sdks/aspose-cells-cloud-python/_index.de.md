---
title: Aspose.Cells Cloud SDK für Python
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/available-sdks/aspose-cells-cloud-python/
description: Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Aufteilen, Schützen, für interne Objektoperationen usw.
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Python
---
 Das SDK ist Open Source und unter der MIT-Lizenz lizenziert. Sie können auf den Quellcode der Python-Bibliothek für Aspose.Cells Cloud zugreifen[Hier](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python).

# **So verwenden Sie Aspose.Cells Cloud SDK für Python**

Aspose.Cells Cloud SDK für Python ist eine leistungsstarke Bibliothek, mit der Entwickler Microsoft Excel-Dateien mit der Programmiersprache Python bearbeiten und verarbeiten können. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.

In diesem Artikel untersuchen wir, wie Sie mit dem Aspose.Cells Cloud SDK für Python einige gängige Aufgaben ausführen, z. B. eine neue Excel-Arbeitsmappe erstellen, Daten in Zellen einfügen und die geänderte Arbeitsmappe in der Cloud speichern.

## Erste Schritte

 Bevor Sie das Aspose.Cells Cloud SDK für Go verwenden können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Weitere Informationen finden Sie unter[der Artikel](https://docs.aspose.cloud/cells/quickstart/) auf der Website Aspose, um Ihre Client-ID und Ihr Client-Geheimnis zu erhalten.

## So installieren Sie das Paket Python für Aspose.Cells Cloud

Sie können Aspose.Cells Cloud SDK für Python mit dem folgenden Befehl installieren:

```bash

    pip3 install AsposeCellsCloud
  
 ```

## So verwenden Sie das Paket Python, um Xlsx in PDF zu konvertieren

- Importieren Sie Aspose.Cells Cloud-Bibliothek
 Importieren Sie zunächst das erforderliche Paket aus dem Aspose.Cells Cloud Python SDK in Ihr Projekt.
- Konfigurieren Sie den API-Client mit Anmeldeinformationen
 Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Geheimnis.
- Konvertierungsparameter vorbereiten
 Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.
- Arbeitsmappenkonvertierung ausführen
 Rufen Sie den Konvertierungsprozess mit der Methode PostConvertWorkbook auf und verarbeiten Sie die Antwort.

```python
import os
import sys
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import *
from asposecellscloud.requests import *

api  = CellsApi(os.getenv('CellsCloudClientId'),os.getenv('CellsCloudClientSecret'),"v3.0",os.getenv('CellsCloudApiBaseUrl'))
remote_folder = 'TestData/In'

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'

format = 'csv'

mapFiles = { 
    local_name: os.path.dirname(os.path.realpath(__file__)) + "/../TestData/" +local_name             
}
mapFiles = { 
    local_name:  local_name             
}
request =  UploadFileRequest( mapFiles, remote_folder + '/' + remote_name,storage_name= '')
api.upload_file(request)
 
request =  PutConvertWorkbookRequest( mapFiles,format= format)
api.put_convert_workbook(request)

```

---
title: "Was ist der Unterschied zwischen lokaler Dateiverarbeitung und Cloud-Dateiverarbeitung in Aspose.Cells Cloud?"
second_title: "Dokument"
ArticleTitle: "Was ist der Unterschied zwischen lokaler Dateiverarbeitung und Cloud-Dateiverarbeitung in Aspose.Cells Cloud?"
linktype: "docs"
url: /learn/local-file-processing-vs-cloud-file-processing/
description: "Vergleichen Sie die lokale und Cloud-basierte Dateiverarbeitung in Aspose.Cells Cloud hinsichtlich Speicher, Kosten, Sicherheit und typischer Anwendungsfälle. Ermitteln Sie, welche Herangehensweise am besten zu Ihrem Arbeitsablauf passt."
keywords: "Aspose.Cells Cloud, lokale Dateiverarbeitung, Cloud-Dateiverarbeitung, Tabellenkalkulationskonvertierung, API"
weight: 10
---

Lokale Dateiverarbeitung und Cloud-Dateiverarbeitung sind unterschiedliche Datenmanagementansätze mit wesentlichen Unterschieden hinsichtlich Speicherinfrastruktur, Geschäftsverarbeitung, Zugriff, Kostenstruktur, Sicherheit und geeigneter Anwendungsfälle. Die wichtigsten Unterschiede zwischen beiden sind:

**Voraussetzungen:** Stellen Sie vor der Verwendung der Beispiele sicher, dass Sie über ein gültiges Aspose.Cells Cloud-Konto verfügen, die neueste SDK-Version installiert haben und Ihre Client-ID sowie Client-Secret für die Authentifizierung bereit haben.

## 1. Speicherort und Infrastruktur der Dateien

- Lokale Datei:

  - Dateien werden auf physischen Geräten gespeichert, die vom Nutzer besessen oder verwaltet werden, z. B. auf der Festplatte eines persönlichen Computers, internen Servern oder externen Festplatten. **Sie können den Cells-Cloud-Client direkt auf eine Datei verweisen lassen, die sich auf einem beliebigen lokalen Speichergerät befindet.**
  - Der Kunde hat die vollständige physische Kontrolle über die Hardware.
  - Der Einkauf, die Wartung, Aktualisierung und Außerbetriebnahme der Infrastruktur liegt in der Verantwortung des Nutzers oder seiner Organisation.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# CellsApi initialisieren
api = CellsApi('IhreCellsCloudClientId', 'IhreCellsCloudClientSecret')

# Lokale Excel-Datei in PDF konvertieren
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**API-Referenz – Konvertieren einer Tabellenkalkulation**

| Methode                 | HTTP-Verb | Endpunkt             | Parameter (Schlüssel)                                  | Antworten                      |
|-------------------------|-----------|----------------------|--------------------------------------------------------|--------------------------------|
| `convert_spreadsheet`   | POST      | `/cells/convert`     | `inputFile` – Pfad zur Quelldatei<br>`format` – Zielformat (z. B. `pdf`) | `200 OK` – Konvertierung erfolgreich<br>`400 Bad Request` – ungültige Parameter<br>`401 Unauthorized` – Authentifizierungsfehler |

- Cloud-Datei:

  - Dateien werden in entfernten Rechenzentren gespeichert, die von externen Cloud-Dienstanbietern betrieben werden (Aspose Cloud-Speicher, Dropbox, AWS, Google Cloud, Microsoft Azure). **AWS, Dropbox, Google Cloud und Microsoft Azure können alle mit dem Aspose-Cloud-Speicher verbunden werden.**
  - Kunden greifen auf diese Dateien über das Internet zu, unabhängig vom Standort und der Wartung der zugrunde liegenden Hardware.
  - Die Infrastruktur liegt in der Verantwortung des Cloud-Dienstanbieters; Nutzer nutzen sie bedarfsgesteuert.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheet_asRequest,
)

# CellsApi initialisieren
api = CellsApi('IhreCellsCloudClientId', 'IhreCellsCloudClientSecret')

# Lokale Datei in Cloud-Speicher hochladen
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# Cloud-Datei in ein angegebenes Format exportieren und lokal speichern
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# Remoten Ordner definieren (ggf. durch Ihren tatsächlichen Ordnernamen ersetzen)
RemoteFolder = "PythonSDK"

# Excel-Datei in Aspose.Cells Cloud als ein anderes Format in Aspose.Cells Cloud speichern
api.save_spreadsheet_as(
    SaveSpreadsheetAsRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**API-Referenz – Cloud-Dateioperationen**

| Methode                        | HTTP-Verb | Endpunkt                       | Parameter (Schlüssel)                                                                                   | Antworten                                   |
|--------------------------------|-----------|--------------------------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------|
| `upload_file`                  | PUT       | `/cells/storage/file`          | `localPath` – lokaler Dateipfad<br>`remotePath` – Zielort im Cloud-Speicher                           | `200 OK` – Upload erfolgreich<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST      | `/cells/{name}/export`         | `name` – Cloud-Dateiname<br>`format` – Zielformat (z. B. `pdf`)<br>`folder` – optionaler Ordner        | `200 OK` – Export erfolgreich<br>`400 Bad Request` |
| `save_spreadsheet_as`          | POST      | `/cells/{name}/saveas`         | `name` – Cloud-Dateiname<br>`format` – Zielformat<br>`folder` – Zielordner                             | `200 OK` – Speichern erfolgreich<br>`401 Unauthorized` |

## 2. Geschäftsverarbeitung

Unabhängig davon, ob die Verarbeitung lokal oder in der Cloud erfolgt, wird die gesamte Geschäftsverarbeitung auf dem Cells-Cloud-Server durchgeführt; **daher ist eine Internetverbindung erforderlich**.

## 3. Datenzugriff

- Lokale Dateiverarbeitung:

  - Der Zugriff ist normalerweise auf das jeweilige Gerät selbst beschränkt.
  - Eine Zusammenarbeit mehrerer Personen ist schwierig.
  - Unbequem bei Geräte- oder Standortwechsel.

- Cloud-Dateiverarbeitung:

  - Zugriff auf Dateien von jedem Gerät (Computer, Smartphone, Tablet) jederzeit und überall, sofern eine Internetverbindung besteht.
  - Natürliche Unterstützung für Echtzeit-Zusammenarbeit mehrerer Benutzer; mehrere Nutzer können dasselbe Dokument gleichzeitig bearbeiten, wobei das System automatisch die Versionsverwaltung übernimmt.
  - Hohe Mobilität, flexible Büro-Unterstützung und Remote-Arbeit.

## 4. Kostenstruktur und Sicherheit

- Lokale Datei:

  - In der Anfangsphase sind hohe Kapitalkosten erforderlich. Dies führt zu zusätzlichen Betriebskosten später.
  - Physische und Netzwerksicherheit werden vollständig vom Nutzer selbst kontrolliert.

- Cloud-Datei:

  - Geringe Anfangsinvestition, hauptsächlich laufende Ausgaben, Pay-as-you-go.
  - Sicherheit und Integrität liegen in der Verantwortung des Cloud-Dienstanbieters.

## 5. Geeignete Anwendungsfälle

- Lokale Datei: Dateioperationen können ausschließlich lokal durchgeführt werden.  
- Cloud-Datei: Dateioperationen können lokal oder in der Cloud durchgeführt werden.  

**Hinweise / Einschränkungen:** Die API unterstützt Dateien bis zu 200 MB für die Cloud-Verarbeitung, und nur die in der Dokumentation aufgeführten Formate können konvertiert werden. Netzwerklatenz kann die Verarbeitungszeit für große Tabellenkalkulationen beeinträchtigen.

_Zuletzt aktualisiert: 30. Juli 2026_
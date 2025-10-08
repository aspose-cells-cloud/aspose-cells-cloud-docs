---
title: Was ist der Unterschied zwischen lokaler Dateiverarbeitung und Cloud-Dateiverarbeitung in Aspose.Cells Cloud
second_title: Documen
ArticleTitle: What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud
linktitle: Lokale Dateiverarbeitung vs. Cloud-Dateiverarbeitung
type: docs
url: /de/learn/local-file-processing-vs-cloud-file-processing/
description: Was ist der Unterschied zwischen lokaler Dateiverarbeitung und Cloud-Dateiverarbeitung? Lokale Dateiverarbeitung und Cloud-Dateiverarbeitung sind zwei grundlegend unterschiedliche Datenverwaltungsparadigmen mit erheblichen Unterschieden in Speicherinfrastruktur, Geschäftsabwicklung, Zugriff, Kostenstruktur, Sicherheit und anwendbaren Szenarien.
weight: 10
kwords: Excel Cloud API, REST, Tabellenkalkulation, PDF, CSV, Json, Markdown, lokale Dateiverarbeitung vs. Cloud-Dateiverarbeitung
---
Lokale und Cloud-Dateiverarbeitung sind unterschiedliche Datenverwaltungsparadigmen mit erheblichen Unterschieden in der Dateispeicherinfrastruktur, der Geschäftsabwicklung, dem Zugriff, der Kostenstruktur, der Sicherheit und den anwendbaren Szenarien. Die Hauptunterschiede zwischen den beiden sind:

## 1. Dateispeicherort und Infrastruktur

- Lokale Datei:

 Dateien werden auf physischen Geräten gespeichert, die dem Benutzer gehören oder von ihm verwaltet werden, z. B. auf der Festplatte eines PCs, auf internen Servern oder auf externen mobilen Festplatten. Auf diese Geräte kann direkt über den Cells Cloud-Client zugegriffen werden.
 - Der Kunde hat die vollständige physische Kontrolle über die Hardware.
 - Der Kauf, die Wartung, die Aktualisierung und die Außerbetriebnahme der Infrastruktur liegen in der Verantwortung des Benutzers oder seiner Organisation.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- Cloud-Datei:

 - Dateien werden in entfernten Rechenzentren gespeichert, die von Drittanbietern von Cloud-Diensten betrieben werden (Aspose Cloud-Speicher, Dropbox, AWS, Google Cloud, Microsoft Azure). AWS, Dropbox, Google Cloud und Microsoft Azure können alle Personen mit Aspose Cloud-Speicher verbinden.
 - Kunden greifen über das Internet auf diese Dateien zu, unabhängig vom Standort und der Wartung der zugrunde liegenden Hardware.
 - Die Infrastruktur liegt in der Verantwortung des Cloud-Service-Anbieters und wird von den Benutzern nach Bedarf genutzt.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import UploadFileRequest, ExportSpreadsheetAsFormatRequest, SaveSpreadsheetAsRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Upload local file to cloud storage
api.upload_file( UploadFileRequest("D:\\Data\\EmployeeSalesSummary.xlsx", "PythonSDK/EmployeeSalesSummary.xlsx"))
# Export cloud file to specified format file to local storage
api.export_spreadsheet_as_format( ExportSpreadsheetAsFormatRequest( "EmployeeSalesSummary.xlsx","pdf" ,folder= "PythonSDK"  ) , local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf" )
# Or Save an Excel file of Cells Cloud as another format file of Cells Cloud. 
api.save_spreadsheet_as( SaveSpreadsheetAsRequest (  "EmployeeSalesSummary.xlsx","pdf" ,folder= RemoteFolder ) )

```

## 2. Geschäftsabwicklung

Unabhängig von der lokalen Dateiverarbeitung oder der Cloud-Dateiverarbeitung werden alle Geschäftsprozesse auf dem Cloud-Server Cells abgeschlossen.**daher ist Internetunterstützung erforderlich**.

## 3. Datenzugriff

- Lokale Dateiverarbeitung:

 - Der Zugriff ist normalerweise auf das Gerät selbst beschränkt.
 - Die Zusammenarbeit mehrerer Personen ist schwierig.
 - Unannehmlichkeiten beim Wechseln der Ausrüstung oder des Standorts.

- Cloud-Dateiverarbeitung:

 - Greifen Sie jederzeit und überall von jedem Gerät (Computer, Telefon, Tablet) auf Dateien zu, solange Sie über eine Internetverbindung verfügen.
 - Natürliche Unterstützung für die Echtzeit-Zusammenarbeit mehrerer Personen, mehrere Benutzer können gleichzeitig dasselbe Dokument bearbeiten, das System übernimmt automatisch die Versionskontrolle.
 - Hohe Mobilität, flexibler office-Support und Remote-Arbeit.
  
## 4. Kostenstruktur und Sicherheit

- Lokale Datei:
  
 - Hohe Kapitalausgaben in der Frühphase erfordern bestimmte Kosten für die Betriebsunterstützung in der späteren Phase.
 Sowohl die physische Sicherheit als auch die Netzwerksicherheit werden von den Benutzern selbst kontrolliert.

- Cloud-Datei:

 - Geringe Vorabinvestition, hauptsächlich Betriebskosten, Zahlung auf Anfrage.
 - Sicherheit und Integrität liegen in der Verantwortung des Cloud-Dienstanbieters.

## 5. Anwendbare Szenarien

- Lokale Datei: Dateioperationen können nur lokal ausgeführt werden.
- Cloud-Datei: Dateivorgänge können lokal oder in der Cloud durchgeführt werden.

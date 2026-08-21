---
title: "Aspose.Cells Cloud PHP SDK – Excel-Dateien konvertieren, zusammenführen, teilen, schützen"  
second_title: "Dokument"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Excel-Dateien konvertieren, zusammenführen, teilen, schützen"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /de/available-sdks/aspose-cells-cloud-php/
description: "Laden Sie das Aspose.Cells Cloud PHP SDK (v24.3) herunter. Erfahren Sie, wie Sie es über Composer installieren, authentifizieren, XLSX in PDF/CSV konvertieren, Arbeitsmappen zusammenführen, Blätter schützen und mehr – alles ohne Installation von Office."  
keywords: "Aspose.Cells, Cloud, PHP, SDK, Excel, Konvertieren, Zusammenführen, Teilen, Schützen"  
weight: 30  
---  

Das SDK ist Open Source und unter der MIT-Lizenz lizenziert. Den Quellcode der PHP-Bibliothek für Aspose.Cells Cloud finden Sie <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">hier</a>.

# **Verwendung des Aspose.Cells Cloud SDK für PHP**

Das Aspose.Cells Cloud SDK für PHP ist eine leistungsstarke Bibliothek, die Entwicklern ermöglicht, Microsoft Excel-Dateien mithilfe der **PHP-Programmiersprache** zu bearbeiten und zu verarbeiten. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.

In diesem Artikel zeigen wir Ihnen, wie Sie das Aspose.Cells Cloud SDK für PHP verwenden, um einige gängige Aufgaben auszuführen, wie etwa das Erstellen einer neuen Excel-Arbeitsmappe, das Einfügen von Daten in Zellen und das Speichern der bearbeiteten Arbeitsmappe in der Cloud.

## Erste Schritte

Bevor Sie mit der Verwendung des Aspose.Cells Cloud SDK für **PHP** beginnen können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Lesen Sie <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">den Artikel</a> auf der Aspose-Website, um Ihre Client-ID und Ihren Client-Geheimschlüssel zu erhalten.

**Voraussetzungen**

- PHP 7.4 oder höher  
- Composer auf Ihrem Entwicklungsrechner installiert  
- Gültige Aspose Cloud Client-ID und Client-Geheimschlüssel  
- Zugriff auf einen Aspose Cloud-Speicherort (Standard oder benutzerdefiniert)  

## Installation des PHP-Pakets für Aspose.Cells Cloud

Sie können das Aspose.Cells Cloud SDK für PHP installieren. Die folgenden Schritte sind dafür notwendig:

- Fügen Sie Aspose.Cells Cloud als Abhängigkeit zu Ihrer `composer.json`-Datei hinzu:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Führen Sie Composer Update aus, um das SDK zu installieren:

   ```bash
   composer install
   ```

- Binden Sie den Autoloader von Composer in Ihren PHP-Code ein:

   ```php
   require 'vendor/autoload.php';
   ```

## Verwendung des PHP-Pakets zur Konvertierung von Xlsx in andere Formate

- Importieren Sie die Aspose.Cells Cloud-Bibliothek  
  Beginnen Sie damit, das erforderliche Paket aus dem Aspose.Cells Cloud PHP SDK in Ihr Projekt zu importieren.

- Konfigurieren Sie den API-Client mit Anmeldeinformationen  
  Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Geheimschlüssel.

- Bereiten Sie die Konvertierungsparameter vor  
  Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.

- Führen Sie die Arbeitsmappenkonvertierung aus  
  Rufen Sie den Konvertierungsvorgang mit der Methode `PostConvertWorkbook` auf und verarbeiten Sie die Antwort.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### API-Referenz für `PostConvertWorkbook`

| Parameter      | Beschreibung                                           | Typ    | Erforderlich |
|----------------|--------------------------------------------------------|--------|--------------|
| `file`         | Name der Quell-Excel-Datei (z. B. `sample.xlsx`).    | string | Ja           |
| `format`       | Gewünschtes Ausgabeformat (`pdf`, `csv`, `png`, usw.).| string | Ja           |
| `storage`      | Speichername oder Ordnerpfad, in dem sich die Quelldatei befindet. | string | Nein         |
| `outPath`      | Optionaler Pfad, um die konvertierte Datei direkt im Speicher zu speichern. | string | Nein         |

**HTTP-Methode:** POST  
**Endpunkt:** `/cells/convert/{format}`  

**Beispiel für Antwort (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**Statuscodes**

- `200` – Konvertierung erfolgreich.  
- `400` – Ungültige Anfrage (fehlende oder ungültige Parameter).  
- `401` – Authentifizierung fehlgeschlagen.  
- `500` – Serverfehler.
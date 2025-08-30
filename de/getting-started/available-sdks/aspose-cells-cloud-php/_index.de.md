---
title: Aspose.Cells Cloud SDK für PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Teilen, Schützen, für innere Objektoperationen usw.
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, PHP
---
Das SDK ist Open Source und steht unter der MIT-Lizenz. Sie können auf den Quellcode der Bibliothek PHP für Aspose.Cells Cloud zugreifen.[Hier](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **So verwenden Sie Aspose.Cells Cloud SDK für PHP**

Aspose.Cells Cloud SDK für PHP ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, Microsoft Excel-Dateien mit der Programmiersprache Go zu bearbeiten und zu verarbeiten. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.

In diesem Artikel erfahren Sie, wie Sie mit dem Aspose.Cells Cloud SDK für PHP einige gängige Aufgaben ausführen, z. B. eine neue Excel-Arbeitsmappe erstellen, Daten in Zellen einfügen und die geänderte Arbeitsmappe in der Cloud speichern.

## Erste Schritte

 Bevor Sie das Aspose.Cells Cloud SDK für Go verwenden können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Weitere Informationen finden Sie unter[der Artikel](https://docs.aspose.cloud/cells/quickstart/) auf der Website Aspose, um Ihre Client-ID und Ihr Client-Geheimnis zu erhalten.

## So installieren Sie das PHP-Paket für Aspose.Cells Cloud

Sie können Aspose.Cells Cloud SDK für PHP installieren. Nachfolgend sind die Schritte aufgeführt:

- Fügen Sie Aspose.Cells Cloud als Abhängigkeit zu Ihrer `composer.json`-Datei hinzu:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Führen Sie das Composer-Update aus, um das SDK zu installieren:

   ```bash

   composer install

   ```

- Fügen Sie den Autoloader von Composer in Ihren PHP-Code ein:

   ```php

   require 'vendor/autoload.php';

   ```

## So verwenden Sie das Paket PHP zum Konvertieren von XLSX in andere Formate

- Importieren Sie Aspose.Cells Cloud-Bibliothek
 Beginnen Sie, indem Sie das erforderliche Paket aus dem Aspose.Cells Cloud PHP SDK in Ihr Projekt importieren.
- Konfigurieren Sie den API-Client mit Anmeldeinformationen
 Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Geheimnis.
- Konvertierungsparameter vorbereiten
 Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.
- Arbeitsmappenkonvertierung ausführen
 Rufen Sie den Konvertierungsprozess mit der Methode PostConvertWorkbook auf und verarbeiten Sie die Antwort.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

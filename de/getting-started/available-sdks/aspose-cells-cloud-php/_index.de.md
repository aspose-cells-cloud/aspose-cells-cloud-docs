---
title: Aspose.Cells Cloud SDK für PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Aufteilen, Schützen, für interne Objektoperationen usw.
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, PHP
---
 Das SDK ist Open Source und unter der MIT-Lizenz lizenziert. Sie können auf den Quellcode der PHP-Bibliothek für Aspose.Cells Cloud zugreifen[Hier](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **So verwenden Sie Aspose.Cells Cloud SDK für PHP**

Aspose.Cells Cloud SDK für PHP ist eine leistungsstarke Bibliothek, mit der Entwickler Microsoft Excel-Dateien mit der Programmiersprache Go bearbeiten und verarbeiten können. Mit diesem SDK können Sie Excel-Dokumente in der Cloud erstellen, bearbeiten und konvertieren, ohne zusätzliche Software oder Abhängigkeiten auf Ihrem lokalen Computer installieren zu müssen.

In diesem Artikel untersuchen wir, wie Sie mit dem Aspose.Cells Cloud SDK für PHP einige gängige Aufgaben ausführen, z. B. eine neue Excel-Arbeitsmappe erstellen, Daten in Zellen einfügen und die geänderte Arbeitsmappe in der Cloud speichern.

## Erste Schritte

 Bevor Sie das Aspose.Cells Cloud SDK für Go verwenden können, müssen Sie Ihre Entwicklungsumgebung einrichten und die erforderlichen Abhängigkeiten installieren. Weitere Informationen finden Sie unter[der Artikel](https://docs.aspose.cloud/cells/quickstart/) auf der Website Aspose, um Ihre Client-ID und Ihr Client-Geheimnis zu erhalten.

## So installieren Sie das Paket PHP für Aspose.Cells Cloud

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

- Fügen Sie den Autoloader von Composer in Ihren Code PHP ein:

   ```php

   require 'vendor/autoload.php';

   ```

## So verwenden Sie das Paket PHP, um Xlsx in PDF zu konvertieren

- Importieren Sie Aspose.Cells Cloud-Bibliothek
 Importieren Sie zunächst das erforderliche Paket aus dem Aspose.Cells Cloud PHP SDK in Ihr Projekt.
- Konfigurieren Sie den API-Client mit Anmeldeinformationen
 Authentifizieren Sie Ihren API-Client mit Ihrer eindeutigen Client-ID und Ihrem Client-Geheimnis.
- Konvertierungsparameter vorbereiten
 Definieren Sie Parameter für die Konvertierungsaufgabe, einschließlich des Quelldateinamens, des gewünschten Ausgabeformats und des Speicherordnerpfads.
- Arbeitsmappenkonvertierung ausführen
 Rufen Sie den Konvertierungsprozess mit der Methode PostConvertWorkbook auf und verarbeiten Sie die Antwort.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```

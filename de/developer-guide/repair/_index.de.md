﻿---
title: Reparatur
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/repair/
keywords: Repair Excel, ODS, WPS, and so on files
description: Aspose.Cells Cloud REST API unterstützt die Reparatur von Excel-Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 39
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Reparatur
---
Dieser REST API weist auf `repair` Excel Dateien hin.

- Reparieren Sie XLS, XLSX, XLSM, XLSB, ODS usw.
- Unterstützt mehrere Dateien.

Aspose.Cells Cloud Excel Repair stellt Daten aus beschädigten Excel-Dateien online ohne Installation wieder her. Beschädigte Excel-Dateien können ein Problem darstellen, da Sie sie nicht öffnen können. Sie können die Aspose.Cells Cloud Excel Repair App ausprobieren, um Daten aus beschädigten Excel-Dateien wiederherzustellen.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/repair

```

 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Datei| Datei| Formulardaten| Hochzuladende Datei|
| Format| Schnur| Abfrage| Ausgabeformat, Standardwert ist null, das Ausgabeformat ist gleich dem Eingabedateiformat.|
 
 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.
 
Mit dem Befehlszeilentool cURL können Sie ganz einfach auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Anrufe an Cloud API tätigen.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/repair" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash

{
    "Files":
    [
        { 
            "Filename":"xxxx1.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxx2.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 


## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte lesen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an die Webdienste Aspose.Cells tätigen:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "" >}}
{{< /tab >}}

{{< /tabs >}}

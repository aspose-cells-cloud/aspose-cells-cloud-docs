---
title: Speichern unter Exce
second_title: Aspose.Cells Cloud Documen
linktitle: Speichern Sie eine
type: docs
url: /de/save-an-excel-file-as-other-formats-files/
aliases: [/convert-excel-workbook-to-different-file-formats/, /saveas-other-formats/]
keywords: Save excel files as kinds of format files
description: Aspose.Cells Cloud REST API unterstützt das Speichern von Excel-Dateien in verschiedenen Formatdateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, SaveAs Excel
---
Dieses REST API zeigt die Excel-Datei `save` als Datei in einem anderen Format an.

**Pfadparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Name|Schnur| Der Dateiname.|

**Abfrageparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|neuerDateiname|Schnur| neuer Dateiname|
|isAutoFitRows|Schnur| Passt alle Zeilen in dieser Arbeitsmappe automatisch an. Der Standardwert ist „false“.|
|isAutoFitColumns|Schnur| Passt die Spaltenbreite in dieser Arbeitsmappe automatisch an. Der Standardwert ist „false“.|
|Ordner|Schnur|Original-Arbeitsmappenordner.|
|Speichername|Schnur| Der Speichername, in dem sich die Datei befindet.|
|outStorageName|Schnur| Der Speichername, in dem sich die gespeicherte Datei befindet.|
|checkExcelRestriction|bool| Ob die Einschränkung der Excel-Datei überprüft wird, wenn der Benutzer zellenbezogene Objekte ändert.|
|Region|Schnur| Die regionalen Einstellungen für die Arbeitsmappe.|
|SeitenbreiteAnpassungAufProBlatt|bool| Die Seitenbreite passt auf das Arbeitsblatt.|
|pageTallFitOnPerSheet|bool| Die Seitenhöhe passt auf das Arbeitsblatt.|
|Blattname|Schnur| Konvertieren Sie das angegebene Arbeitsblatt.|
|Seitenindex|Schnur| Konvertieren Sie die angegebene Seite des Arbeitsblatts. Der Blattname ist erforderlich.|
|eineSeiteProBlatt|bool| Bei der Konvertierung in das Format PDF eine Seite pro Blatt.|

**Anforderungstextparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Speicheroptionen| Objekt|Mit der Speicheroption wird im zweiten Teil des mehrteiligen Inhalts gespeichert.|

## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcenlink**|
|:- |:- |:- |:- |
|/Zellen/{Name}/saveAs|POST|Arbeitsmappe in Format exportieren|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

 Sie können**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an Cloud API tätigen.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "SaveResult": {
    "SourceDocument": {
      "Href": "test.xlsx",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "DestDocument": {
      "Href": "test.pdf",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "AdditionalItems": []
  },
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

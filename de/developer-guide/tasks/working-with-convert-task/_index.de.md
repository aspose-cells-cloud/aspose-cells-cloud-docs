﻿---
title: Arbeiten mit Convert Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/tasks/convert/
aliases: [/working-with-convert-task/]
keywords: REST API, task, convert, spreadsheets, exce
description: "Cells.Cloud API für Excel betreiben: Aufgaben unterstützen Konvertierung von Excel-Dateien"
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Arbeiten mit Konvertierungsaufgaben
---
## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcenlink**|
|:- |:- |:- |:- |
|/Zellen/Aufgabe/Runtask|POST|Aufgabe ausführen|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

 Sie können**cURL**Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie mit cURL Anrufe an Cloud API tätigen.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<TaskData>\t<Tasks>\t<TaskDescription>\t\t<TaskType>SmartMarker</TaskType>\t\t<SmartMarkerTaskParameter>\t\t<SourceWorkbook>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>Book1.xlsx</FilePath>\t\t</SourceWorkbook>\t\t<DestinationWorkbook>\t\t\t<FileSourceType>InMemoryFiles</FileSourceType>\t\t\t<FilePath>ReportTask.xlsx</FilePath>\t\t</DestinationWorkbook>\t\t<xmlFile>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>ReportData.xml</FilePath>\t\t</xmlFile>\t\t</SmartMarkerTaskParameter>\t</TaskDescription>\t<TaskDescription>\t\t<TaskType>SaveResult</TaskType>\t\t<SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t\t<DestinationType>OutputStream</DestinationType>\t\t\t<InputFile>ReportTask.xlsx</InputFile>\t\t\t<OutputFile>Output.xlsx</OutputFile>\t\t</ResultDestination>\t\t</SaveResultTaskParameter>\t</TaskDescription>\t</Tasks></TaskData>}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte lesen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an die Webdienste Aspose.Cells tätigen:

{{< tabs tabTotal="1" tabID="4" tabName1="C#" >}}

{{< tab tabNum="1" >}}

```csharp

var xml = @"<TaskData>

                <Tasks>

                <TaskDescription>

                    <TaskType>SmartMarker</TaskType>

                    <SmartMarkerTaskParameter>

                    <SourceWorkbook>

                        <FileSourceType>CloudFileSystem</FileSourceType>

                        <FilePath>Book1.xlsx</FilePath>

                    </SourceWorkbook>

                    <DestinationWorkbook>

                        <FileSourceType>InMemoryFiles</FileSourceType>

                        <FilePath>ReportTask.xlsx</FilePath>

                    </DestinationWorkbook>

                    <xmlFile>

                        <FileSourceType>CloudFileSystem</FileSourceType>

                        <FilePath>ReportData.xml</FilePath>

                    </xmlFile>

                    </SmartMarkerTaskParameter>

                </TaskDescription>

                <TaskDescription>

                    <TaskType>SaveResult</TaskType>

                    <SaveResultTaskParameter>

                    <ResultSource>InMemoryFiles</ResultSource>

                    <ResultDestination>

                        <DestinationType>OutputStream</DestinationType>

                        <InputFile>ReportTask.xlsx</InputFile>

                        <OutputFile>Output.xlsx</OutputFile>

                    </ResultDestination>

                    </SaveResultTaskParameter>

                </TaskDescription>

                </Tasks>

            </TaskData>";


ServiceHelper helper = new ServiceHelper(sid, key);

using (HttpWebResponse response = helper.CallPost("http://api.aspose.com/v3.0/cells/task/runtask", xml, "application/xml"))

{

    if (response.StatusCode == HttpStatusCode.OK)

    {

        System.Console.WriteLine("OK");

        Stream st = response.GetResponseStream();

        FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate);

        st.CopyTo(fs);

    }

}//using


```

{{< /tab >}}

{{< /tabs >}}

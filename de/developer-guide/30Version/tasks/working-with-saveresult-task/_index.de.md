---
title: Arbeiten mit SaveResult Tas
second_title: Documen
type: docs
url: /de/tasks/save-result/
aliases: [/working-with-saveresult-task/]
keywords: REST API, task, save result, spreadsheets, exce
description: "Cells.Cloud API für Excel betreiben: Aufgaben unterstützen das Speichern des Ergebnisses in Antwortinhalten oder im Cloud-Speicher"
weight: 50
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Arbeiten mit SaveResult-Aufgabe
---
## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcenlink**|
|:- |:- |:- |:- |
|/Zellen/Aufgabe/Ausführen der Aufgabe|POST|Task ausführen|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

 Sie können**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an Cloud API tätigen.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ <Tasks>\t<TaskDescription>\t <TaskType>ImportData</TaskType>\t <ImportDataTaskParameter>\t\t<Workbook>\t\t <FileSourceType>CloudFileSystem</FileSourceType>\t\t <FilePath>TaskBook.xlsx</FilePath>\t\t</Workbook>\t\t<ImportBatchDataOption>\t\t <DestinationWorksheet>Sheet1</DestinationWorksheet>\t\t <IsInsert>true</IsInsert>\t\t <Source>\t\t\t<FileSourceType>RequestFiles</FileSourceType>\t\t\t<FilePath>Batch_data_xml.txt</FilePath>\t\t </Source>\t\t</ImportBatchDataOption>\t </ImportDataTaskParameter>\t</TaskDescription>\t<TaskDescription>\t <TaskType>ImportData</TaskType>\t <ImportDataTaskParameter>\t\t<Workbook>\t\t <FileSourceType>InMemoryFiles</FileSourceType>\t\t <FilePath>TaskBook.xlsx</FilePath>\t\t</Workbook>\t\t<ImportBatchDataOption>\t\t <DestinationWorksheet>Sheet2</DestinationWorksheet>\t\t <IsInsert>true</IsInsert>\t\t <Source>\t\t\t<FileSourceType>RequestFiles</FileSourceType>\t\t\t<FilePath>Batch_data_xml_2.txt</FilePath>\t\t </Source>\t\t</ImportBatchDataOption>\t </ImportDataTaskParameter>\t</TaskDescription>\t<TaskDescription>\t <TaskType>SaveResult</TaskType>\t <SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t <DestinationType>CloudFileSystem</DestinationType>\t\t <InputFile>TaskBook.xlsx</InputFile>\t\t <OutputFile>ImpDataBook.xlsx</OutputFile>\t\t</ResultDestination>\t </SaveResultTaskParameter>\t</TaskDescription> </Tasks></TaskData>}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="1" tabID="4" tabName1="Java" >}}

{{< tab tabNum="1" >}}
```java

var xml = @"

<TaskData>

  <Tasks>

    <TaskDescription>

      <TaskType>Convert</TaskType>

      <ConvertTaskParameter>

        <Workbook>

          <FileSourceType>CloudFileSystem</FileSourceType>

          <FilePath>Source.xlsx</FilePath>

        </Workbook>

        <DestinationFile>Temp.tiff</DestinationFile>

        <ImageSaveOptions>

          <HorizontalResolution>200</HorizontalResolution>

          <OnePagePerSheet>true</OnePagePerSheet>

          <VerticalResolution>100</VerticalResolution>

        </ImageSaveOptions>

      </ConvertTaskParameter>

    </TaskDescription>

    <TaskDescription>

      <TaskType>SaveResult</TaskType>

      <SaveResultTaskParameter>

        <ResultSource>InMemoryFiles</ResultSource>

        <ResultDestination>

          <DestinationType>OutputStream</DestinationType>

          <InputFile>Temp.tiff</InputFile>

          <OutputFile>Output.tiff</OutputFile>

        </ResultDestination>

      </SaveResultTaskParameter>

    </TaskDescription>

  </Tasks>

</TaskData>

";

ServiceHelper helper = new ServiceHelper(sid, key);

using (HttpWebResponse response = helper.CallPost("http://api.aspose.com/v3.0/cells/task/runtask", xml, "application/xml"))

{

    if (response.StatusCode == HttpStatusCode.OK)

    {

        System.Console.WriteLine("OK");

        Stream st = response.GetResponseStream();

        FileStream fs = new FileStream("Output.tiff", FileMode.OpenOrCreate);

        st.CopyTo(fs);

    }

}


```
{{< /tab >}}

{{< /tabs >}}

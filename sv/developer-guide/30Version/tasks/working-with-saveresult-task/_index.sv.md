---
title: "Arbeta med SaveResult-uppgift"
second_title: "Dokument"
type: docs
url: /tasks/save-result/
aliases: [/working-with-saveresult-task/]
keywords: "SaveResult-uppgift, Aspose.Cells Cloud API, exportera resultat, ladda ner kalkylark, molnlagring, REST API, kalkylark, Excel"
description: "Lär dig hur du använder SaveResult-uppgiften i Aspose.Cells Cloud API för att exportera bearbetade kalkylarksdata till molnlagring eller ladda ner den direkt. Innehåller exempel med cURL, Java och .NET samt en komplett parameterreferens."
weight: 50
---

## REST API

| **API** | **Typ** | **Beskrivning** | **Resurslänk** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Kör uppgift | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/xml" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d "<?xml version=\"1.0\" encoding=\"UTF-8\"?>
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>TaskBook.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet1</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <Source>
            <FileSourceType>RequestFiles</FileSourceType>
            <FilePath>Batch_data_xml.txt</FilePath>
          </Source>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>TaskBook.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <Source>
            <FileSourceType>RequestFiles</FileSourceType>
            <FilePath>Batch_data_xml_2.txt</FilePath>
          </Source>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>CloudFileSystem</DestinationType>
          <InputFile>TaskBook.xlsx</InputFile>
          <OutputFile>ImpDataBook.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HttpResponseMessage som innehåller åtgärdens resultat.
```

{{< /tab >}}

{{< /tabs >}}

Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:n:

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
---
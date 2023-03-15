---
title: "Working with SmartMarker Task"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "REST API, task, save result, spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: tasks support to smart marker."
weight: 60
---

## REST API

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/task/runtask|POST|Run Task|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. 

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<TaskData> <Tasks> <TaskDescription> <TaskType>SmartMarker</TaskType> <SmartMarkerTaskParameter> <SourceWorkbook> <FileSourceType>CloudFileSystem</FileSourceType> <FilePath>Designer.xlsx</FilePath> </SourceWorkbook> <DestinationWorkbook> <FileSourceType>InMemoryFiles</FileSourceType> <FilePath>Temp.xlsx</FilePath> </DestinationWorkbook> <xmlFile> <FileSourceType>CloudFileSystem</FileSourceType> <FilePath>DataSet.xml</FilePath> </xmlFile> </SmartMarkerTaskParameter> </TaskDescription> <TaskDescription> <TaskType>SaveResult</TaskType> <SaveResultTaskParameter> <ResultSource>InMemoryFiles</ResultSource> <ResultDestination> <DestinationType>OutputStream</DestinationType> <InputFile>Temp.xlsx</InputFile> <OutputFile>Output.xlsx</OutputFile> </ResultDestination> </SaveResultTaskParameter> </TaskDescription> </Tasks></TaskData>}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

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

            <FilePath>Designer.xlsx</FilePath>

        </SourceWorkbook>

        <DestinationWorkbook>

            <FileSourceType>InMemoryFiles</FileSourceType>

            <FilePath>Temp.xlsx</FilePath>

        </DestinationWorkbook>

        <xmlFile>

            <FileSourceType>CloudFileSystem</FileSourceType>

            <FilePath>DataSet.xml</FilePath>

        </xmlFile>

        </SmartMarkerTaskParameter>

    </TaskDescription>

    <TaskDescription>

        <TaskType>SaveResult</TaskType>

        <SaveResultTaskParameter>

        <ResultSource>InMemoryFiles</ResultSource>

        <ResultDestination>

            <DestinationType>OutputStream</DestinationType>

            <InputFile>Temp.xlsx</InputFile>

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

}

```
{{< /tab >}}

{{< /tabs >}}

---
title: "Working with SaveResult Task"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /tasks/save-result/
aliases: [/working-with-saveresult-task/]
keywords: "REST API, task, save result, spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: tasks support to save the result into response content or cloud storage."
weight: 50
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

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ <Tasks>\t<TaskDescription>\t <TaskType>ImportData</TaskType>\t <ImportDataTaskParameter>\t\t<Workbook>\t\t <FileSourceType>CloudFileSystem</FileSourceType>\t\t <FilePath>TaskBook.xlsx</FilePath>\t\t</Workbook>\t\t<ImportBatchDataOption>\t\t <DestinationWorksheet>Sheet1</DestinationWorksheet>\t\t <IsInsert>true</IsInsert>\t\t <Source>\t\t\t<FileSourceType>RequestFiles</FileSourceType>\t\t\t<FilePath>Batch_data_xml.txt</FilePath>\t\t </Source>\t\t</ImportBatchDataOption>\t </ImportDataTaskParameter>\t</TaskDescription>\t<TaskDescription>\t <TaskType>ImportData</TaskType>\t <ImportDataTaskParameter>\t\t<Workbook>\t\t <FileSourceType>InMemoryFiles</FileSourceType>\t\t <FilePath>TaskBook.xlsx</FilePath>\t\t</Workbook>\t\t<ImportBatchDataOption>\t\t <DestinationWorksheet>Sheet2</DestinationWorksheet>\t\t <IsInsert>true</IsInsert>\t\t <Source>\t\t\t<FileSourceType>RequestFiles</FileSourceType>\t\t\t<FilePath>Batch_data_xml_2.txt</FilePath>\t\t </Source>\t\t</ImportBatchDataOption>\t </ImportDataTaskParameter>\t</TaskDescription>\t<TaskDescription>\t <TaskType>SaveResult</TaskType>\t <SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t <DestinationType>CloudFileSystem</DestinationType>\t\t <InputFile>TaskBook.xlsx</InputFile>\t\t <OutputFile>ImpDataBook.xlsx</OutputFile>\t\t</ResultDestination>\t </SaveResultTaskParameter>\t</TaskDescription> </Tasks></TaskData>}"

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

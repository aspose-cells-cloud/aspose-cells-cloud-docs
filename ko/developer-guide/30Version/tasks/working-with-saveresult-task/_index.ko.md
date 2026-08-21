---
title: "SaveResult 작업 사용하기"
second_title: "문서"
type: docs
url: /tasks/save-result/
aliases: [/working-with-saveresult-task/]
keywords: "SaveResult 작업, Aspose.Cells Cloud API, 결과 내보내기, 워크북 다운로드, 클라우드 스토리지, REST API, 스프레드시트, Excel"
description: "Aspose.Cells Cloud API에서 SaveResult 작업을 사용하여 처리된 워크북 데이터를 클라우드 스토리지로 내보내거나 직접 다운로드하는 방법을 알아보세요. cURL, Java, .NET 예제 및 전체 매개변수 참조를 포함합니다."
weight: 50
---

## REST API

| **API** | **유형** | **설명** | **리소스 링크** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | 작업 실행 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 명세서](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

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
작업 결과를 포함하는 HttpResponse 메시지입니다.
```

{{< /tab >}}

{{< /tabs >}}

SDK를 사용하면 개발 속도를 높이는 데 가장 효과적입니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하시기 바랍니다.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

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
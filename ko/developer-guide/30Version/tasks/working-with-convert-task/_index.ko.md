---
title: "Convert 작업 사용하기"
second_title: "문서"
type: docs
url: /tasks/convert/
aliases: [/working-with-convert-task/]
keywords: "Aspose.Cells Cloud, REST API, Convert Task, Excel,Spreadsheet, PDF, CSV, JSON, Markdown"
description: "Cells Cloud API는 Excel 파일을 다양한 형식으로 변환하는 작업 지원을 제공합니다."
weight: 30
---

## REST API

|**API**|**유형**|**설명**|**리소스 링크**|
| :- | :- | :- | :- |
|/cells/task/runtask|POST|작업 실행|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```java
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<TaskData>\t<Tasks>\t<TaskDescription>\t\t<TaskType>SmartMarker</TaskType>\t\t<SmartMarkerTaskParameter>\t\t<SourceWorkbook>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>Book1.xlsx</FilePath>\t\t</SourceWorkbook>\t\t<DestinationWorkbook>\t\t\t<FileSourceType>InMemoryFiles</FileSourceType>\t\t\t<FilePath>ReportTask.xlsx</FilePath>\t\t</DestinationWorkbook>\t\t<xmlFile>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>ReportData.xml</FilePath>\t\t</xmlFile>\t\t</SmartMarkerTaskParameter>\t</TaskDescription>\t<TaskDescription>\t\t<TaskType>SaveResult</TaskType>\t\t<SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t\t<DestinationType>OutputStream</DestinationType>\t\t\t<InputFile>ReportTask.xlsx</InputFile>\t\t\t<OutputFile>Output.xlsx</OutputFile>\t\t</ResultDestination>\t\t</SaveResultTaskParameter>\t</TaskDescription>\t</Tasks></TaskData>}"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
작업 결과가 포함된 HttpResponse 메시지입니다.
```

{{< /tab >}}

{{< /tabs >}}

SDK를 사용하는 것이 개발 속도를 높이는 가장 좋은 방법입니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

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
---
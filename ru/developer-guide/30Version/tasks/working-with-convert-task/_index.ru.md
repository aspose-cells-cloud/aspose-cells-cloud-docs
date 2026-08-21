---
title: "Работа с задачей Convert"
second_title: "Документ"
type: docs
url: /tasks/convert/
aliases: [/working-with-convert-task/]
keywords: "Aspose.Cells Cloud, REST API, задача Convert, Excel, электронная таблица, PDF, CSV, JSON, Markdown"
description: "Облако API для Excel предоставляет поддержку задач по преобразованию файлов Excel в различные форматы."
weight: 30
---

## REST API

|**API**|**Тип**|**Описание**|**Ссылка на ресурс**|
| :- | :- | :- | :- |
|/cells/task/runtask|POST|Выполнение задачи|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) определяет общедоступное программное интерфейсное решение и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.  

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```java
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<TaskData>\t<Tasks>\t<TaskDescription>\t\t<TaskType>SmartMarker</TaskType>\t\t<SmartMarkerTaskParameter>\t\t<SourceWorkbook>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>Book1.xlsx</FilePath>\t\t</SourceWorkbook>\t\t<DestinationWorkbook>\t\t\t<FileSourceType>InMemoryFiles</FileSourceType>\t\t\t<FilePath>ReportTask.xlsx</FilePath>\t\t</DestinationWorkbook>\t\t<xmlFile>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>ReportData.xml</FilePath>\t\t</xmlFile>\t\t</SmartMarkerTaskParameter>\t</TaskDescription>\t<TaskDescription>\t\t<TaskType>SaveResult</TaskType>\t\t<SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t\t<DestinationType>OutputStream</DestinationType>\t\t\t<InputFile>ReportTask.xlsx</InputFile>\t\t\t<OutputFile>Output.xlsx</OutputFile>\t\t</ResultDestination>\t\t</SaveResultTaskParameter>\t</TaskDescription>\t</Tasks></TaskData>}"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
HttpResponseMessage, содержащий результат выполнения операции.
```

{{< /tab >}}

{{< /tabs >}}

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя работу с низкоуровневыми деталями и позволяет сосредоточиться на задачах вашего проекта. Ознакомьтесь со [репозиторием на GitHub](https://github.com/aspose-cells-cloud), где представлен полный список SDK для Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

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
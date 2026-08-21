---
title: "Работа с задачей SaveResult"
second_title: "Документ"
type: docs
url: /tasks/save-result/
aliases: [/working-with-saveresult-task/]
keywords: "задача SaveResult, API Aspose.Cells Cloud, экспорт результата, загрузка рабочей книги, облачное хранилище, REST API, электронные таблицы, Excel"
description: "Узнайте, как использовать задачу SaveResult в API Aspose.Cells Cloud для экспорта обработанных данных рабочей книги в облачное хранилище или прямой загрузки. Содержит примеры cURL, Java, .NET и полный справочник по параметрам."
weight: 50
---

## REST API

| **API** | **Тип** | **Описание** | **Ссылка на ресурс** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Выполнение задачи | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

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
HttpResponseMessage, содержащий результат выполнения операции.
```

{{< /tab >}}

{{< /tabs >}}

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

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
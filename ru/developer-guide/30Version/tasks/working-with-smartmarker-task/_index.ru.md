---
title: "Работа с задачей SmartMarker в Aspose.Cells Cloud API"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "задача SmartMarker, Aspose.Cells Cloud, REST API, Excel, автоматизация электронных таблиц"
description: "Узнайте, как использовать задачу SmartMarker в Aspose.Cells Cloud API с примерами на cURL и SDK, включая схему запроса и обработку ошибок."
weight: 60
ArticleTitle: "Работа с задачей SmartMarker в Aspose.Cells Cloud API"
---

## REST API

**SmartMarker** — это функция Aspose.Cells Cloud API, которая объединяет данные из XML- или JSON-источников в заполнители шаблона электронной таблицы Excel, создавая полностью заполненную рабочую книгу. Обычно используется для генерации отчётов, слияния по шаблону и создания электронных таблиц на основе данных.

**Необходимые условия**

- Aspose.Cells Cloud API версии 3.0 или выше.  
- Действующий токен доступа OAuth2/JWT (передаётся в заголовке `Authorization: Bearer <token>`).  
- Исходные файлы (рабочая книга-шаблон и файл с данными) загружены в облачное хранилище Aspose Cloud или доступны через поддерживаемый тип файловой системы.  
- HTTPS-endpoint (все запросы должны использовать TLS).

| **API** | **Тип** | **Описание** | **Ссылка на ресурс** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Выполнение задачи | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-службам Aspose.Cells. Пример ниже показывает, как выполнить задачу SmartMarker и сохранить результирующую рабочую книгу.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <ваш_токен_доступа>" \
     -d '{
  "TaskData": {
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "SmartMarker",
          "SmartMarkerTaskParameter": {
            "SourceWorkbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "Designer.xlsx"
            },
            "DestinationWorkbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "Temp.xlsx"
            },
            "xmlFile": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "DataSet.xml"
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "SaveResult",
          "SaveResultTaskParameter": {
            "ResultSource": "InMemoryFiles",
            "ResultDestination": {
              "DestinationType": "OutputStream",
              "InputFile": "Temp.xlsx",
              "OutputFile": "Output.xlsx"
            }
          }
        }
      }
    ]
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "FileLink": "https://api.aspose.cloud/v3.0/storage/file/Output.xlsx",
    "FileSize": 254321,
    "FileName": "Output.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Схема запроса (выдержка)

| Элемент | Тип | Обязательный | Описание |
| ------- | ---- | -------- | ----------- |
| `TaskData` | объект | Да | Корневой элемент, содержащий один или несколько объектов `TaskDescription`. |
| `Tasks` | массив объектов | Да | Коллекция задач, выполняемых в порядке следования. |
| `TaskDescription.TaskType` | строка | Да | Тип задачи (`SmartMarker`, `SaveResult` и т.д.). |
| `SmartMarkerTaskParameter.SourceWorkbook` | объект | Да | Указывает местоположение шаблона рабочей книги. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | объект | Да | Указывает, где сохраняется промежуточная рабочая книга. |
| `SmartMarkerTaskParameter.xmlFile` | объект | Да | Источник данных (XML/JSON), используемый SmartMarker. |
| `SaveResultTaskParameter.ResultDestination` | объект | Да | Определяет способ возврата финальной рабочей книги (например, `OutputStream`). |

### Обработка ошибок

API может возвращать следующие HTTP-коды состояния:

- **400 Bad Request** — некорректная структура тела запроса или отсутствие обязательных полей.  
- **401 Unauthorized** — недействительный или отсутствующий токен аутентификации.  
- **404 Not Found** — один из указанных исходных файлов не найден.  
- **500 Internal Server Error** — непредвиденная ошибка на стороне сервера.

Проверьте тело ответа на наличие объекта `Error`, содержащего `Code` и описательное `Message`.

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя работу с низкоуровневыми деталями, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}.

Примеры кода ниже демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

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
using (HttpWebResponse response = helper.CallPost(
       "https://api.aspose.cloud/v3.0/cells/task/runtask",
       xml,
       "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("OK");
        using (Stream st = response.GetResponseStream())
        using (FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate))
        {
            st.CopyTo(fs);
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}
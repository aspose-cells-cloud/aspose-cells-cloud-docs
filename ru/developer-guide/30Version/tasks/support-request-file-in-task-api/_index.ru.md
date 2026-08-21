---
title: "Файл запроса в Task API"
second_title: "Документ"
type: docs
url: /tasks/support-request-file/
aliases: [/support-request-file-in-task-api/]
keywords: "Aspose.Cells, REST API, Excel, облако"
description: "Aspose.Cells Cloud API позволяет выполнять обработку файлов запросов на основе задач для рабочих книг Excel."
weight: 10
ArticleTitle: "Файл запроса в Task API Aspose.Cells"
---

## REST API

| **API** | **Тип** | **Описание** | **Ссылка на ресурс** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Выполнение задачи | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) определяет общедоступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

**Параметры запроса**

| Параметр | Тип | Обязательный | Описание |
|----------|-----|-------------|----------|
| TaskDescription | object | Да | Контейнер для одного определения задачи. |
| TaskType | string | Да | Тип задачи, например `ImportData` или `SaveResult`. |
| Workbook.FileSourceType | string | Да | Источник файла рабочей книги (`CloudFileSystem`, `InMemoryFiles`). |
| Workbook.FilePath | string | Да | Путь к файлу рабочей книги в выбранном источнике. |
| ImportBatchDataOption.DestinationWorksheet | string | Да | Имя целевого рабочего листа для импортируемых данных. |
| ImportBatchDataOption.IsInsert | boolean | Да | Флаг вставки строк (`true`) или перезаписи (`false`). |
| ImportBatchDataOption.Source.FileSourceType | string | Да | Источник файла запроса (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | string | Да | Путь к файлу запроса, содержащему пакетные данные. |
| SaveResultTaskParameter.ResultSource | string | Да | Источник результирующего файла (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | Да | Тип назначения результата (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | string | Да | Имя входного файла рабочей книги. |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | Да | Желаемое имя выходного файла. |

**Ответ**

| Поле | Тип | Описание |
|------|-----|----------|
| Code | integer | Код HTTP-статуса (например, 200 — успех). |
| Status | string | Статус операции (`OK` или сообщение об ошибке). |
| Result | object | Подробности выполнения задачи, включая любые созданные файлы. |

Для простого доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки **cURL**. В следующем примере показано, как выполнять вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -H "x-aspose-client: Containerize.Swagger" \
  -d '{
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet1",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml.txt"
              }
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet2",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml_2.txt"
              }
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
              "DestinationType": "CloudFileSystem",
              "InputFile": "TaskBook.xlsx",
              "OutputFile": "ImpDataBook.xlsx"
            }
          }
        }
      }
    ]
  }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "GeneratedFiles": [
      {
        "FilePath": "ImpDataBook.xlsx",
        "FileUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

Дополнительные сведения о связанных задачах см. на страницах [ImportData task](/cells/tasks/importdata/) и [SaveResult task](/cells/tasks/save-result/).

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берет на себя низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

В приведенных ниже примерах кода показано, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}
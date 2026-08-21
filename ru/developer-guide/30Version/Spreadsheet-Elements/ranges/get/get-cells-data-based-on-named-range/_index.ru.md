---
title: "Получение данных ячеек по именованному диапазону"
second_title: "Документ"
linktitle: "Значения"
type: docs
url: /ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: "Aspose.Cells, облако, REST API, Excel, именованный диапазон, значения ячеек, рабочий лист"
description: "Получение значений ячеек из именованного диапазона в рабочем листе Excel с использованием REST API Aspose.Cells Cloud. Сервис доступен через множество SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) и работает на широком спектре платформ разработки."
weight: 20
ArticleTitle: "Получение данных ячеек по именованному диапазону — Aspose.Cells Cloud API"
---

**Необходимые условия**

- Действующий JWT-токен доступа с соответствующей областью действия.  
- Книга должна быть загружена в облачное хранилище Aspose (или в указанную папку).  
- При использовании нестандартного хранилища необходимо указать его имя.

Этот REST API возвращает список ячеек в диапазоне, определяемом по именованному диапазону или по индексам строки и столбца.

Эта операция позволяет разработчикам программно получать значения ячеек, принадлежащих конкретному именованному диапазону в рабочем листе Excel. При передаче идентификатора `namedRange` либо явных индексов строки и столбца API возвращает подробный список ячеек, включая их адрес, строку, столбец, значение, тип данных и информацию о форматировании. Ответ может использоваться для создания приложений, основанных на данных, генерации отчётов или выполнении дополнительных вычислений на стороне сервера. Сервис Aspose.Cells Cloud поддерживает множество языков программирования через SDK, обеспечивая беспрепятственную интеграцию независимо от платформы разработки. Использование HTTPS гарантирует защищённую передачу данных, а API соответствует принципам REST, возвращая стандартные коды состояния HTTP для успешных и ошибочных операций.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                                                 |
|---------------|--------|--------------|--------------------------------------------------------------------------|
| name          | string | path         | Имя файла книги.                                                         |
| sheetName     | string | path         | Имя рабочего листа внутри книги.                                        |
| namedRange    | string | query        | Имя именованного диапазона для извлечения, например `A1:B2` или `range_name1`. |
| firstRow      | integer | query       | Нулевой индекс первой строки диапазона (используется, если `namedRange` не задан). |
| firstColumn   | integer | query       | Нулевой индекс первого столбца диапазона (используется, если `namedRange` не задан). |
| rowCount      | integer | query       | Количество строк в диапазоне.                                            |
| columnCount   | integer | query       | Количество столбцов в диапазоне.                                         |
| folder        | string | query        | Папка, содержащая книгу.                                                 |
| storageName   | string | query        | Имя облачного хранилища, в котором находится книга.                     |

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для вызова веб-сервисов Aspose.Cells. Ниже приведён пример запроса значений ячеек из именованного диапазона.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Примечание по безопасности:** Всегда используйте HTTPS при вызове API. Сервис не поддерживает незащищённый HTTP; использование HTTPS гарантирует шифрование запроса и соответствие лучшим практикам безопасности.

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                             |
|-----|-----------------------------|------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр успешно применён; в ответе содержатся детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.       |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает ограничение по размеру. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                     |

**Пример ответа об ошибке (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Отсутствует или недопустим параметр 'namedRange'."
}
```

> **Совет:** API использует нулевые индексы для `firstRow` и `firstColumn`. Например, первая строка рабочего листа имеет индекс `0`.

## Семейство облачных SDK

Использование SDK — наиболее эффективный способ ускорения разработки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен на [GitHub-репозитории](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
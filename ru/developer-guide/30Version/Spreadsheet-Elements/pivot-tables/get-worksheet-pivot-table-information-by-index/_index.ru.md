---
title: "Получение сводной таблицы в листе Excel"
second_title: "Документ"
linktype: "Получить"
type: docs
url: /ru/pivot-tables/get/
aliases: [  /ru/get-worksheet-pivot-table-information-by-index/ ]
keywords: "Aspose.Cells, сводная таблица, Excel, REST API, получение сводной таблицы листа"
description: "Получение сводной таблицы из листа Excel через Aspose.Cells Cloud REST API. Включает синтаксис запроса, параметры, аутентификацию, схему ответа, обработку ошибок и примеры SDK."
weight: 10
ArticleTitle: "Получение сводной таблицы в листе Excel"
---

Этот REST API позволяет получить информацию о **сводной таблице** в листе по её индексу.

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### Параметры запроса

| Имя параметра     | Тип     | Местоположение | Описание                                             |
| ----------------- | ------- | -------------- | ---------------------------------------------------- |
| **name**          | string  | path           | Имя файла Excel.                                     |
| **sheetName**     | string  | path           | Имя листа, содержащего сводную таблицу.             |
| **pivottableIndex** | integer | path         | Индекс сводной таблицы в листе (начинается с 0).    |
| **folder**        | string  | query          | Папка, в которой хранится документ.                 |
| **storageName**   | string  | query          | Имя облачного хранилища Aspose Cloud.               |

Для удобного доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки **cURL**. Пример ниже показывает, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**Схема ответа**

| Поле            | Тип     | Описание                                             |
|-----------------|---------|------------------------------------------------------|
| Status          | string  | Текст статуса операции (например, «OK»).            |
| PivotFilters    | array   | Коллекция определений фильтров сводной таблицы.      |
| └─ AutoFilter   | object  | Подробная информация об автоматической фильтрации.   |
|    └─ link      | object  | Сведения о гиперссылке для фильтра.                  |
|    └─ FilterColumns | array | Параметры фильтрации отдельных столбцов.         |
|    └─ Range     | string  | Диапазон ячеек, к которому применяется фильтр.       |
|    └─ Sorter    | object  | Конфигурация сортировки отфильтрованных данных.     |
| (дополнительные вложенные поля имеют такую же структуру, как показано в примере JSON) |

{{< /tab >}}

{{< /tabs >}}

### Обработка ошибок

API использует стандартные HTTP-коды состояния. Типичные ответы:

| Код состояния | Значение                                                           | Пример JSON (ошибка)                              |
|--------------|--------------------------------------------------------------------|---------------------------------------------------|
| 200          | Успех — возвращена сводная таблица                                | —                                                 |
| 401          | Неавторизованный доступ — недействительный или отсутствующий токен | `{"code":401,"message":"Invalid access token."}`  |
| 404          | Не найдено — файл, лист или индекс сводной таблицы не существуют  | `{"code":404,"message":"Pivot table not found."}` |
| 500          | Ошибка сервера — непредвиденное условие                           | `{"code":500,"message":"Internal server error."}` |

**Примечания:** API поддерживает файлы Excel объёмом до 150 МБ и работает с форматами Excel 2007–2021. Убедитесь, что имя листа указано с учётом регистра.

## Семейство облачных SDK

Использование SDK — оптимальный способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в репозитории [GitHub](https://github.com/aspose-cells-cloud).

В приведённых ниже примерах показано, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}
---
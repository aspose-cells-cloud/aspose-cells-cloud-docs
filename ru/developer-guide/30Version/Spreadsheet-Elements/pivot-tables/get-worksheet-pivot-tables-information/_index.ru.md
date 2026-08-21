---
title: "Получить все сводные таблицы в листе Excel"
second_title: "Документ"
linktype: "Получить все"
type: docs
url: "/pivot-tables/get-all/"
aliases: [/get-worksheet-pivot-tables-information/]
keywords: "получить все сводные таблицы, Aspose.Cells Cloud API, Excel PivotTable, REST API"
description: "Получить все сводные таблицы из листа Excel с помощью Aspose.Cells Cloud API. Включает конечную точку, параметры, шаги аутентификации, примеры cURL и SDK для API сводных таблиц."
weight: 20
ArticleTitle: "Получить все сводные таблицы в листе Excel – Aspose.Cells Cloud API"
---

**Sводная таблица (PivotTable)** — это инструмент сводки данных в Excel, позволяющий переупорядочивать и анализировать большие наборы данных. Данный REST API извлекает информацию обо **всех** сводных таблицах в указанном листе.

## Безопасность и аутентификация

Aspose.Cells Cloud API защищены и требуют [аутентификации с использованием токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                  |
|---------------|--------|--------------|-------------------------------------------|
| name          | string | path         | Имя файла Excel.                          |
| sheetName     | string | path         | Имя листа.                                |
| folder        | string | query        | Папка, в которой хранится документ.       |
| storageName   | string | query        | Имя сервиса хранилища.                    |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Запрос

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### Ответ

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Ответы об ошибках

| HTTP-код | Описание                                                       | Пример JSON-тела ответа                                     |
|----------|----------------------------------------------------------------|-------------------------------------------------------------|
| 400      | Неверный запрос — отсутствует обязательный параметр.          | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401      | Неавторизован — недействительный или отсутствующий токен.     | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404      | Не найдено — рабочая книга, лист или сводная таблица не найдены. | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500      | Внутренняя ошибка сервера — непредвиденное условие на сервере. | `{ "Code": "500", "Message": "Server error." }`               |

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK берет на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на вашем проекте. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}
---
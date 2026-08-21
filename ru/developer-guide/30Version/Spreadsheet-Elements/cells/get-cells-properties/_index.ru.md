---
title: "Получение свойств ячеек"
type: docs
url: /ru/get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, Рабочий лист, Свойства ячеек, Получение свойств ячеек"
description: "Узнайте, как использовать REST API Aspose.Cells Cloud для получения свойств конкретной ячейки или предопределённых методов ячейки в рабочем листе Excel."
---

Этот REST API демонстрирует, как получить конкретную ячейку в файле Excel.

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## Безопасность и аутентификация

API Aspose.Cells Cloud безопасны и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Параметры запроса


| Имя параметра         | Тип    | Расположение | Описание                                                                                                                                                                   |
| --------------------- | ------ | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**              | string | path         | Имя документа Excel.                                                                                                                                                       |
| **sheetName**         | string | path         | Имя рабочего листа, содержащего ячейку.                                                                                                                                    |
| **cellOrMethodName**  | string | path         | Имя ячейки или имя предопределённого метода (например, `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`). |
| **folder**            | string | query        | Папка, в которой хранится документ.                                                                                                                                        |
| **storageName**       | string | query        | Имя сервиса хранилища.                                                                                                                                                     |

## **Ответ**

Возвращает объект CellResponse.

- **Обзор полей ответа**

| Поле            | Тип     | Описание                                                |
| --------------- | ------- | ------------------------------------------------------- |
| `Name`          | string  | Адрес ячейки (например, `F341`).                        |
| `Row`           | integer | Индекс строки (начиная с нуля).                         |
| `Column`        | integer | Индекс столбца (начиная с нуля).                        |
| `Value`         | string  | Отображаемое значение ячейки.                           |
| `Type`          | string  | Тип данных ячейки (например, `IsString`).               |
| `Formula`       | string  | Текст формулы, если ячейка содержит формулу.            |
| `IsFormula`     | bool    | Указывает, содержит ли ячейка формулу.                  |
| `IsMerged`      | bool    | Указывает, является ли ячейка частью объединённого диапазона. |
| `IsArrayHeader` | bool    | Указывает, является ли ячейка заголовком массива.       |
| `IsInArray`     | bool    | Указывает, принадлежит ли ячейка массиву.               |
| `IsErrorValue`  | bool    | Указывает, содержит ли ячейка значение ошибки.          |
| `IsInTable`     | bool    | Указывает, находится ли ячейка внутри таблицы.          |
| `IsStyleSet`    | bool    | Указывает, применён ли к ячейке стиль.                  |
| `HtmlString`    | string  | HTML-представление значения ячейки.                     |
| `Style.link`    | object  | Гиперссылка на ресурс стиля.                            |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит данные о выполненной операции.   |
| 400  | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недействительный или отсутствующий JWT-токен.                           |
| 413  | Payload Too Large           | Загруженный файл превышает предельный размер.                            |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                                           |

## Как использовать API GetWorksheetCell с SDK

### Спецификация API GetWorksheetCell

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как сделать вызов облачного API с помощью cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — наиболее эффективный способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), где представлен полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Как получить конкретную ячейку

- [Получить данные ячейки с рабочего листа](/ru/cells/get-cell-data-from-a-worksheet/)
- [Получить первую ячейку из рабочего листа Excel](/ru/cells/get-first-cell-from-excel-worksheet/)
- [Получить последнюю ячейку рабочего листа Excel](/ru/cells/get-last-cell-of-excel-worksheet/)
- [Получить MaxRow из рабочего листа Excel](/ru/cells/get-maxrow-from-excel-worksheet/)
- [Получить MaxDataRow из рабочего листа Excel](/ru/cells/get-maxdatarow-from-excel-worksheet/)
- [Получить MaxColumn из рабочего листа Excel](/ru/cells/get-maxcolumn-from-excel-worksheet/)
- [Получить MaxDataColumn из рабочего листа Excel](/ru/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Получить MinRow из рабочего листа Excel](/ru/cells/get-minrow-from-excel-worksheet/)
- [Получить MinDataRow из рабочего листа Excel](/ru/cells/get-mindatarow-from-excel-worksheet/)
- [Получить MinColumn из рабочего листа Excel](/ru/cells/get-mincolumn-from-excel-worksheet/)
- [Получить MinDataColumn из рабочего листа Excel](/ru/cells/get-mindatacolumn-from-excel-worksheet/)
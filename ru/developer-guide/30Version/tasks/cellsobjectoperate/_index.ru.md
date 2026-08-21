---
title: "Aspose.Cells Cloud API – Работа с задачей CellsObjectOperate (REST)"
second_title: "Документ"
type: docs
url: /ru/tasks/cells-object-operate/
aliases: [  /ru/working-with-cellsobjectoperate-task/ ]
description: "Ознакомьтесь с использованием задачи CellsObjectOperate в Aspose.Cells Cloud API: справочник по параметрам, примеры запросов и ответов, а также рекомендации по работе с рабочими листами, диаграммами и сводными таблицами."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – Работа с задачей CellsObjectOperate (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "Задача CellsObjectOperate"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "операция с диаграммой"
  - "API сводной таблицы"
  - "API разрыва страницы"
---

**Обзор**  
Задача **CellsObjectOperate** позволяет выполнять операции создания, чтения, обновления и удаления (CRUD) над объектами Excel, такими как рабочие книги, рабочие листы, диаграммы, сводные таблицы, фигуры, разрывы страниц и другими, с помощью одного REST-вызова. Укажите тип объекта через параметр `OperateObjectType` и предоставьте соответствующий блок параметров (например, `ChartOperateParameter` для действий с диаграммами).

---

**OperateObject**

| Имя параметра          | Тип    | Описание |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | string | Тип объекта Excel, над которым следует выполнить операцию. Допустимые значения: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition   | object | Контейнер, определяющий местоположение целевого объекта (например, имя рабочей книги, имя рабочего листа, индекс диаграммы). Обязателен для большинства операций. |

**OperateObjectPosition**

| Имя параметра | Тип    | Описание |
| -------------- | ------ | ----------- |
| Workbook       | object | Рабочая книга, содержащая целевой объект. Должна включать либо `FileName` (облако), либо `FileContent` (base64). |
| SheetName      | string | Имя рабочего листа, к которому применяется операция. Обязателен для объектов уровня листа (диаграммы, фигуры и др.). |
| ChartIndex     | integer| Нулевой индекс диаграммы в пределах рабочего листа (используется, если `OperateObjectType` равен `Chart`). |
| ShapeIndex     | integer| Нулевой индекс фигуры в пределах рабочего листа (используется, если `OperateObjectType` равен `Shape`). |
| CellName       | string | Ссылка на ячейку в формате A1 (например, `A1`). Используется для операций на уровне ячейки. |
| ListObjectIndex| integer| Нулевой индекс объекта-списка (таблицы) (используется, если `OperateObjectType` равен `ListObject`). |

**ChartOperateParameter**

| Имя параметра        | Тип    | Описание |
| --------------------- | ------ | ----------- |
| ChartIndex            | integer| Индекс диаграммы, которую следует изменить. Обязателен при обновлении существующей диаграммы. |
| ChartType             | string | Тип создаваемой диаграммы (например, `Bar`, `Line`, `Pie`). |
| UpperLeftRow          | integer| Номер строки верхнего левого угла диаграммы (с нуля). |
| UpperLeftColumn       | integer| Номер столбца верхнего левого угла диаграммы (с нуля). |
| LowerRightRow         | integer| Номер строки нижнего правого угла диаграммы. |
| LowerRightColumn      | integer| Номер столбца нижнего правого угла диаграммы. |
| Area                  | string | Диапазон данных для диаграммы (например, `A1:B5`). |
| IsVertical            | string | `true`, если ориентация диаграммы вертикальная; иначе `false`. |
| CategoryData          | string | Диапазон, содержащий метки оси X (категории). |
| IsAutoGetSerialName   | string | `true`, чтобы автоматически генерировать имена рядов; `false`, чтобы использовать пользовательские имена. |
| Title                 | string | Текст заголовка, отображаемый на диаграмме. |

**ListObjectOperateParameter**

| Имя параметра | Тип    | Описание |
| -------------- | ------ | ----------- |
| ListObject     | object | Объект конфигурации операции со списком (таблицей). Включает свойства, такие как `ShowHeader`, `ShowTotal` и `Style`. |

**PageBreakOperateParameter**

| Имя параметра | Тип    | Описание |
| -------------- | ------ | ----------- |
| PageBreakType  | string | Тип разрыва страницы (`Horizontal` или `Vertical`). |
| Index          | integer| Нулевой индекс удаляемого или изменяемого разрыва страницы. |
| Row            | integer| Номер строки, в которой размещается горизонтальный разрыв страницы. |
| Column         | integer| Номер столбца, в котором размещается вертикальный разрыв страницы. |
| StartIndex     | integer| Начальный индекс для операции с диапазоном разрывов страниц. |
| EndIndex       | integer| Конечный индекс для операции с диапазоном разрывов страниц. |

**PageSetupOperateParameter**

| Имя параметра | Тип    | Описание |
| -------------- | ------ | ----------- |
| PageSetup      | object | Параметры макета страницы (поля, ориентация, размер бумаги и т.д.). |

**PivotTableOperateParameter**

| Имя параметра    | Тип         | Описание |
| ---------------- | ----------- | ----------- |
| DestCellName     | string      | Ячейка верхнего левого угла целевого диапазона для сводной таблицы (например, `C5`). |
| SourceData       | string      | Исходный диапазон для сводной таблицы (например, `A1:D100`). |
| TableName        | string      | Имя, присваиваемое созданной сводной таблице. |
| UseSameSource    | string      | `true`, чтобы повторно использовать существующий исходный диапазон; `false`, чтобы создать новый. |
| PivotTableIndex  | integer     | Индекс обновляемой сводной таблицы (обязателен для действий изменения/удаления). |
| PivotFieldRows   | integer[]   | Коллекция индексов полей, отображаемых в строковой области. |
| PivotFieldColumns| integer[]   | Коллекция индексов полей, отображаемых в столбцовой области. |
| PivotFieldData   | integer[]   | Коллекция индексов полей, отображаемых в области данных. |

**ShapeOperateParameter**

| Имя параметра | Тип    | Описание |
| -------------- | ------ | ----------- |
| Shape          | object | Определение фигуры (тип, позиция, размер, текст и т.д.). |

**WorkbookSettingsOperateParameter**

| Имя параметра   | Тип    | Описание |
| ---------------- | ------ | ----------- |
| WorkbookSettings | object | Параметры, влияющие на всю рабочую книгу (например, режим вычислений, точность). |

**WorksheetOperateParameter**

| Имя параметра | Тип    | Описание |
| -------------- | ------ | ----------- |
| Name           | string | Текущее имя рабочего листа, над которым выполняется операция. |
| SheetType      | string | Тип листа (`Worksheet`, `Chart` и т.д.). |
| NewName        | string | Новое имя рабочего листа при переименовании. |
| MovingRequest  | object | Параметры перемещения рабочего листа (например, `FromIndex`, `ToIndex`). |

## REST API

| API                | Тип  | Описание | Ссылка на ресурс |
| ------------------ | ---- | ----------- | ------------- |
| /cells/task/runtask| POST | Выполнение задачи | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Предварительные требования
- **Аутентификация** – Необходимо добавить корректный заголовок `Authorization: Bearer <access_token>`.  
- **Хранилище** – Исходная рабочая книга должна находиться в облаке Aspose или быть передана как base64-кодированное содержимое в теле запроса.  
- **Версия API** – В данном документе рассматривается **v3.0** Aspose.Cells Cloud API.

### Пример запроса (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

Тело запроса следует схеме **CellsObjectOperateRequest**, определённой ниже:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* Дополнительные определения опущены для краткости */
  }
}
```

### Пример ответа (успех – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Диаграмма успешно создана."
  }
}
```

Ответ содержит следующие поля:

| Поле    | Тип    | Описание |
| ------- | ------ | ----------- |
| Code    | integer| Код состояния, возвращаемый движком задачи (аналог HTTP-кода). |
| Status  | string | Человекочитаемое состояние (например, `OK`). |
| TaskId  | string | Идентификатор асинхронной задачи. |
| Result  | object | Объект с результатами конкретной операции. |
| Result.ChartId | integer | Идентификатор созданной или изменённой диаграммы. |
| Result.Message | string | Краткое сообщение о результате. |

### Обработка ошибок

| HTTP-статус | Код ошибки | Описание | Рекомендуемое решение |
| ----------- | ---------- | ----------- | ---------------- |
| 400         | InvalidParameter | Один или несколько параметров запроса отсутствуют или некорректны. | Проверьте обязательные поля и типы данных. |
| 401         | Unauthorized | Недействительный или отсутствующий токен аутентификации. | Обновите токен доступа и добавьте его в заголовок `Authorization`. |
| 404         | NotFound | Указанная рабочая книга, рабочий лист или объект не найдены. | Проверьте `FileName`, `SheetName` и индексы объектов. |
| 500         | ServerError | На сервере произошла непредвиденная ошибка. | Повторите запрос; если проблема сохраняется, обратитесь в службу поддержки. |

### Типичные сценарии использования
- **Добавление новой диаграммы** на рабочий лист.  
- **Переименование рабочего листа** (`OperateObjectType = "Worksheet"` с `WorksheetOperateParameter.NewName`).  
- **Вставка разрыва страницы** (`OperateObjectType = "PageBreak"` с `PageBreakOperateParameter`).  
- **Обновление исходных данных сводной таблицы** (`OperateObjectType = "PivotTable"` с `PivotTableOperateParameter.SourceData`).  
- **Изменение параметров рабочей книги**, таких как режим вычислений (`OperateObjectType = "WorkbookSettings"`).  

---  

*Все описания получены из официальной спецификации Aspose.Cells Cloud OpenAPI.*  
---
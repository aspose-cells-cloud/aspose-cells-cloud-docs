---
title: "Преобразование таблицы в сводную таблицу"
second_title: "Документ"
linktype: "Преобразование"
type: docs
url: /pivot-tables/convert-table-to-pivottable/
aliases:
  [
    "/create-a-pivottable-with-table/",
    "/create-new-pivot-table-with-list-object-as-source-data/",
  ]
keywords: "сводная таблица, объект списка, Aspose.Cells Cloud, REST API, преобразование таблицы в сводную таблицу"
description: "Узнайте, как создать сводную таблицу из объекта списка с помощью Aspose.Cells Cloud REST API. Включает детали запроса, пример cURL и ссылки на SDK."
weight: 60
ArticleTitle: "Преобразование таблицы в сводную таблицу – Документация Aspose.Cells Cloud"
---

Этот REST API создает **сводную таблицу** из объекта списка.

Сводная таблица агрегирует данные из объекта списка, позволяя анализировать и отображать большие наборы данных непосредственно в рабочей книге.

**Необходимые условия:**  
- Действующий JWT-токен для аутентификации.  
- Рабочая книга должна существовать в указанном хранилище.  
- Целевой рабочий лист должен содержать объект списка, который вы хотите агрегировать.

## API PostWorksheetListObjectSummarizeWithPivotTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра   | Тип     | Расположение | Описание                                       |
| --------------- | ------- | ----------- | --------------------------------------------- |
| name            | string  | path        | Имя файла рабочей книги.                       |
| sheetName       | string  | path        | Рабочий лист, содержащий объект списка.        |
| listObjectIndex | integer | path        | Индекс объекта списка на рабочем листе.        |
| destsheetName   | string  | query       | Имя целевого рабочего листа.                  |
| request         | object  | body        | JSON-полезная нагрузка, определяющая сводную таблицу. |
| folder          | string  | query       | Путь к папке, где находится рабочая книга.   |
| storageName     | string  | query       | Имя хранилища.                                |

Тело запроса должно соответствовать следующей JSON-схеме:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Имя новой сводной таблицы." },
    "DestCellName": { "type": "string", "description": "Верхняя левая ячейка сводной таблицы (например, «C1»)." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Нулевые индексы полей для размещения в строках."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Нулевые индексы полей для размещения в столбцах."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Нулевые индексы полей, используемых в качестве полей данных."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

<a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступное программное интерфейсное взаимодействие и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*Примечание: Используйте продакшн-эндпоинт (`api.aspose.cloud`) для рабочих сред. Эндпоинт QA (`api-qa.aspose.cloud`) предназначен только для тестирования. Все вызовы в продакшн должны использовать HTTPS.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                          |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; в ответе содержатся детали операции. |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Некорректный или отсутствующий JWT-токен.       |
| 413 | Payload Too Large           | Загружаемый файл превышает допустимый размер.    |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                   |

## Семейство облачных SDK

Использование SDK — оптимальный способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с помощью различных SDK:
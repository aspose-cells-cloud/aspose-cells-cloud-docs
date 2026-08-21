---
---
title: "Работа с строками Excel-файлов — Aspose.Cells Cloud API"
ArticleTitle: "Работа с строками Excel-файлов — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Строки"
type: docs
url: /rows/
aliases: [/working-with-rows/]
keywords: "Aspose.Cells, строки Excel, REST API, обработка электронных таблиц"
description: "Обработка строк в Excel-файлах с помощью Aspose.Cells Cloud REST API. Поддерживает Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift."
weight: 100
---

## Работа со строками в Excel-файле

**Последнее обновление: июль 2026 г.**

- [Как получить информацию о строке в листе Excel.](/cells/rows/get/row/)
- [Как добавить пустую строку в лист Excel.](/cells/rows/add/row/)
- [Как скопировать строки в листе Excel.](/cells/rows/copy/)
- [Как скрыть строки в листе Excel.](/cells/rows/hide/)
- [Как отобразить скрытые строки в листе Excel.](/cells/rows/unhide/)
- [Как сгруппировать строки в листе Excel.](/cells/rows/group/)
- [Как разгруппировать строки в листе Excel.](/cells/rows/ungroup/)
- [Как удалить строку из листа](/cells/rows/delete/)

Краткая справка по API для типовых операций со строками:

| Операция           | HTTP-метод | Эндпоинт                                                               | Ключевые параметры                          |
|--------------------|------------|------------------------------------------------------------------------|---------------------------------------------|
| [Получить строку](https://docs.aspose.cloud/cells/rows/get/row/)     | GET        | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`         |
| [Добавить строку](https://docs.aspose.cloud/cells/rows/add/row/)     | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                        |
| [Скопировать строки](https://docs.aspose.cloud/cells/rows/copy/)     | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Удалить строку](https://docs.aspose.cloud/cells/rows/delete/)      | DELETE     | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`         |
| [Скрыть строки](https://docs.aspose.cloud/cells/rows/hide/)         | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`                    |
| [Отобразить строки](https://docs.aspose.cloud/cells/rows/unhide/)   | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`                    |
| [Сгруппировать строки](https://docs.aspose.cloud/cells/rows/group/) | POST       | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`                    |
| [Разгруппировать строки](https://docs.aspose.cloud/cells/rows/ungroup/)| POST      | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`                    |

**Детали запроса и ответа**

- **Получить строку**  
  *Запрос*: Тело запроса не требуется.  
  *Ответ (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *Ошибки*: 400 Bad Request (недопустимый индекс), 404 Not Found (отсутствует файл или лист).

- **Добавить строку**  
  *Тело запроса (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *Ответ (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *Ошибки*: 400 Bad Request (отсутствующие/недопустимые параметры), 401 Unauthorized.

- **Скопировать строки**  
  *Тело запроса (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *Ответ (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *Ошибки*: 400 Bad Request, 404 Not Found.

- **Удалить строку**  
  *Запрос*: Тело запроса не требуется.  
  *Ответ (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *Ошибки*: 400 Bad Request, 404 Not Found.

- **Скрыть строки**  
  *Тело запроса (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *Ответ (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *Ошибки*: 400 Bad Request.

- **Отобразить строки** — тот же формат запроса, что у *Скрыть строки*; ответ аналогичен, статус — «Rows unhidden».

- **Сгруппировать строки** — тот же формат запроса, что у *Скрыть строки*; статус ответа — «Rows grouped».

- **Разгруппировать строки** — тот же формат запроса, что у *Скрыть строки*; статус ответа — «Rows ungrouped».

Все операции требуют действительного токена доступа OAuth 2.0/JWT и соответствующей версии SDK.  

---
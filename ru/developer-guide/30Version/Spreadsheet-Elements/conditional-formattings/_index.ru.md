---
title: "Работа с условным форматированием в Excel"
second_title: "Документ"
linktype: "Условное форматирование"
type: docs
url: /ru/conditional-formattings/
aliases: [  /ru/working-with-conditional-formatting/ ]
keywords: "Excel, условное форматирование, Aspose.Cells Cloud, API"
description: "API Aspose.Cells Cloud для Excel предоставляет конечные точки для извлечения, добавления, изменения и удаления правил условного форматирования, что позволяет динамически визуально анализировать данные рабочего листа."
weight: 100
ArticleTitle: "Работа с условным форматированием в Excel – Руководство по API"
---

Условное форматирование в Excel позволяет выделять ячейки определённым цветом в зависимости от значения ячейки.

Используйте условное форматирование для визуального исследования и анализа данных, выявления критических проблем, а также обнаружения паттернов и тенденций.

Условное форматирование упрощает выделение интересующих ячеек или диапазонов ячеек, подчеркивание необычных значений и визуализацию данных с помощью диаграмм данных, цветовых шкал и наборов значков, соответствующих определённым изменениям в данных.

Условное форматирование изменяет внешний вид ячеек в зависимости от заданных вами условий. Если условие истинно, диапазон ячеек форматируется; если ложно — остаётся без изменений. Встроенных условий существует множество, а также вы можете создавать свои собственные (в том числе с помощью формулы, результатом которой является **TRUE** или **FALSE**).

API Aspose.Cells Cloud предоставляет набор конечных точек для программного управления правилами условного форматирования. Доступны следующие операции:

- **Получить условные форматы рабочего листа** – извлекает все правила условного форматирования, применённые к рабочему листу.  
  - **Метод:** `GET`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Параметры:** `fileName` (строка, обязательный), `sheetName` (строка, обязательный), необязательные параметры запроса, например `folder`, `storageName`  
  - **Пример cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **Получить условный формат** – возвращает конкретное правило условного форматирования по его идентификатору.  
  - **Метод:** `GET`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Параметры:** `index` (целое число, обязательный) определяет позицию правила.  
  - **Пример cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **Добавить ячейочный диапазон для условия форматирования** – добавляет диапазон ячеек, к которому будет применяться указанное условие форматирования.  
  - **Метод:** `POST`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Тело запроса (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **Пример cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **Добавить условие для условия форматирования** – определяет новое условие (например, значение, формулу) для существующего правила форматирования.  
  - **Метод:** `POST`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **Тело запроса (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **Пример cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **Добавить условие форматирования** – создаёт полное правило условного форматирования, включая тип и стиль.  
  - **Метод:** `POST`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Тело запроса (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **Пример cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **Очистить все условия форматирования** – удаляет все правила условного форматирования с целевого рабочего листа.  
  - **Метод:** `DELETE`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Пример cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **Удалить ячейочный диапазон из условного форматирования** – удаляет ранее определённый ячейочный диапазон из правила условного форматирования.  
  - **Метод:** `DELETE`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Пример cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **Удалить условное форматирование** – удаляет всё правило условного форматирования с рабочего листа.  
  - **Метод:** `DELETE`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Пример cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

Примеры иллюстрируют необходимый HTTP-метод, шаблон URL, ключевые параметры и примеры полезной нагрузки запроса для каждой операции. При необходимости используйте соответствующий SDK (C#, Java, Python и т.д.) для получения фрагментов кода на нужном языке.
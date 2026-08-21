---
title: "Aspose.Cells Cloud API – Объединение диапазона ячеек"
second title: "Документ"
linktitle: "Объединение"
type: docs
url: /ranges/merge/
aliases: [/combines-a-range-of-cells-into-a-single-cell/]
keywords: "Aspose.Cells, объединение ячеек, Excel API, REST, облачный SDK"
description: "Объединить диапазон ячеек в одну ячейку с помощью Aspose.Cells Cloud REST API. Описан формат запроса, параметры и примеры SDK для C#, Java, Python и других языков."
weight: 20
---

Этот REST API объединяет диапазон ячеек в одну ячейку на листе Excel.

**Обзор** – объединение диапазона объединяет выбранные ячейки в одну ячейку, сохраняя значение левой верхней ячейки и отбрасывая остальные. Используйте эту операцию, если вам нужно создать заголовок, охватывающий несколько столбцов или строк, или упростить структуру листа.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **Параметры запроса**

| Имя параметра  | Тип    | Местоположение | Описание                                              |
| --------------- | ------ | -------------- | ----------------------------------------------------- |
| **name**        | string | path           | Имя рабочей книги.                                    |
| **sheetName**   | string | path           | Имя листа.                                            |
| **range**       | object | body           | Объект диапазона, определяющий ячейки для объединения. |
| **folder**      | string | query          | Папка, в которой хранится рабочая книга.             |
| **storageName** | string | query          | Имя хранилища.                                        |

#### Схема тела запроса

Объект **Range** должен содержать следующие поля (остальные — необязательны):

| Свойство        | Тип     | Обязательное | Описание                                                |
| --------------- | ------- | ------------ | ------------------------------------------------------- |
| **FirstRow**    | integer | Да           | Индекс первой строки в диапазоне (начинается с 0).      |
| **FirstColumn** | integer | Да           | Индекс первого столбца в диапазоне (начинается с 0).    |
| **RowCount**    | integer | Да           | Количество строк, включаемых в диапазон.                |
| **ColumnCount** | integer | Да           | Количество столбцов, включаемых в диапазон.             |
| **Name**        | string  | Нет          | Необязательное имя диапазона.                           |
| **RefersTo**    | string  | Нет          | Формула, на которую ссылается диапазон.                 |
| **Worksheet**   | string  | Нет          | Имя листа (если отличается от параметра пути).          |
| **RowHeight**   | number  | Нет          | Высота строк в диапазоне (в пикселях).                  |
| **ColumnWidth** | number  | Нет          | Ширина столбцов в диапазоне (в пикселях).               |

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
```

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

#### Подробности ответа

| HTTP-статус                   | Описание                                                    | Пример JSON                                            |
| ----------------------------- | ----------------------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | Диапазон успешно объединён.                                 | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | Некорректные параметры диапазона (например, выход индексов за пределы). | `{ "Code": 400, "Message": "Invalid range." }`         |
| **401 Unauthorized**          | Отсутствует или недействителен JWT-токен.                  | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found**             | Рабочая книга или лист не найдены.                          | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500 Internal Server Error** | Непредвиденная ошибка сервера.                              | `{ "Code": 500, "Message": "Internal server error." }` |

## Семейство облачных SDK

Использование SDK — оптимальный способ ускорить разработку. SDK берёт на себя работу с низкоуровневыми деталями, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже показывают, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
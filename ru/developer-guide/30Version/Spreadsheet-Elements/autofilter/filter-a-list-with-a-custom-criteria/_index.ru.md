---
title: "Добавление пользовательского критерия в рабочий лист Excel"
second_title: "Document"
linktitle: "Добавить пользовательский фильтр"
type: docs
url: /autofilter/add-custom-filter/
aliases: [/filter-a-list-with-a-custom-criteria/,/autofilter/add-a-custom-filter/]
keywords: "Excel, пользовательский фильтр, Aspose.Cells Cloud, REST API, автофильтр, рабочий лист, пользовательский критерий"
description: "Узнайте, как использовать Aspose.Cells Cloud REST API для добавления пользовательского фильтра в рабочий лист Excel. Включает подробности запроса, пример cURL и фрагменты кода SDK для различных языков программирования."
weight: 65
ArticleTitle: "Добавление пользовательского критерия в рабочий лист Excel – Aspose.Cells Cloud API"
---

Этот REST API фильтрует список с использованием **пользовательского критерия**.

## API PutWorksheetCustomFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются безопасными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса:

| Имя параметра   | Тип     | Местоположение               | Описание                                                                 |
|-----------------|---------|------------------------------|--------------------------------------------------------------------------|
| name            | string  | path                         | Имя файла Excel.                                                         |
| sheetName       | string  | path                         | Имя рабочего листа, содержащего данные, подлежащие фильтрации.          |
| range           | string  | query                        | Диапазон ячеек, к которому будет применён фильтр (например, `A1:B1`).   |
| fieldIndex      | integer | query                        | Индекс столбца (начиная с нуля), по которому применяется фильтр.        |
| operatorType1   | string  | query                        | Первый оператор сравнения (например, `LessOrEqual`, `Equal`).           |
| criteria1       | string  | query                        | Первое фильтрующее значение или выражение.                              |
| isAnd           | boolean | query                        | Если `true`, два критерия объединяются с помощью **И**; иначе — **ИЛИ**.|
| operatorType2   | string  | query                        | Второй оператор сравнения (необязательный).                             |
| criteria2       | string  | query                        | Второе фильтрующее значение или выражение (необязательное).             |
| matchBlanks     | boolean | query                        | Если `true`, пустые ячейки включаются в результаты фильтрации.          |
| refresh         | boolean | query                        | Если `true`, рабочий лист будет обновлён после применения фильтра.      |
| folder          | string  | query                        | Путь к папке в хранилище, где находится файл.                           |
| storageName     | string  | query                        | Имя сервиса хранилища.                                                   |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                                      |
|-----|------------------------------|---------------------------------------------------------------|
| 200 | OK (ОК)                      | Фильтр успешно применён; ответ содержит детали операции.     |
| 400 | Bad Request (Неверный запрос)| Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Неверный или отсутствующий JWT-токен.                         |
| 413 | Payload Too Large (Слишком большой payload) | Загружаемый файл превышает ограничение по размеру.         |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                            |

## Как использовать API PutWorksheetCustomFilter с SDK

### Спецификация API PutWorksheetCustomFilter

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на логике вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Другие операции AutoFilter, такие как добавление стандартного фильтра или фильтра по дате, описаны в соответствующих страницах документации в разделе AutoFilter.
---
title: "Добавление объекта списка (таблицы) в рабочий лист Excel"
second_title: "Документ"
linktitle: "Добавление"
type: docs
url: /ru/list-objects/add/
aliases: [  /ru/add-a-list-object-or-table-inside-the-worksheet/ , /ru/tables/add/ ]
keywords: "Aspose.Cells Cloud, Excel API, объект списка, таблица, REST API, рабочий лист"
description: "Узнайте, как добавить объект списка (таблицу Excel) в рабочий лист с помощью REST API Aspose.Cells Cloud. Включает endpoint, параметры, шаги аутентификации, пример cURL и примеры кода SDK."
weight: 10
ArticleTitle: "Добавление объекта списка (таблицы) в рабочий лист Excel – Документация Aspose.Cells Cloud"
---

Этот REST API добавляет **объект списка (таблицу)** в рабочий лист Excel.

Прежде чем использовать этот endpoint, убедитесь, что у вас есть действительный JWT-токен, книга хранится в поддерживаемом облачном хранилище и указанный рабочий лист существует.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### Параметры запроса

| Имя параметра   | Тип     | Расположение | Описание                                                                   |
| ---------------- | ------- | ------------ | -------------------------------------------------------------------------- |
| **name**         | string  | path         | Имя файла книги.                                                           |
| **sheetName**    | string  | path         | Имя рабочего листа.                                                        |
| **startRow**     | integer | query        | Индекс первой строки диапазона таблицы (начинается с 0).                   |
| **startColumn**  | integer | query        | Индекс первого столбца диапазона таблицы (начинается с 0).                |
| **endRow**       | integer | query        | Индекс последней строки диапазона таблицы (начинается с 0).               |
| **endColumn**    | integer | query        | Индекс последнего столбца диапазона таблицы (начинается с 0).             |
| **hasHeaders**   | boolean | query        | `true`, если первая строка содержит заголовки столбцов; иначе `false`.   |
| **listObject**   | object  | body         | Описание объекта списка (см. **Схему тела запроса**).                     |
| **folder**       | string  | query        | Папка, содержащая книгу.                                                   |
| **storageName**  | string  | query        | Имя хранилища.                                                             |

### Схема тела запроса

Объект **listObject** описывает таблицу, которая будет создана. Приведены только наиболее распространённые свойства; полный список смотрите в спецификации OpenAPI.

```json
{
  "displayName": "MyTable",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MyTable",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### Пример ответа

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Коды ошибок

| HTTP-статус | Причина               | Описание                                           |
|------------|----------------------|----------------------------------------------------|
| **400**    | Bad Request          | Неверные параметры диапазона или некорректный JSON в теле. |
| **401**    | Unauthorized         | Отсутствует или истёк JWT-токен.                  |
| **404**    | Not Found            | Указанная книга или рабочий лист не существуют.   |
| **500**    | Internal Server Error | Непредвиденная ошибка на стороне сервера.         |

**Пример ответа 400**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**Пример ответа 401**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

Полное описание этой операции приведено в [спецификации OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject).

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud см. в [репозитории GitHub](https://github.com/aspose-cells-cloud).

В приведённых ниже примерах кода показано, как выполнять вызовы веб-сервисов Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
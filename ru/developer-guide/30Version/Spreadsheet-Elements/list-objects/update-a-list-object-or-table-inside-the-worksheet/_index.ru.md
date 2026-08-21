---
title: "Обновление объекта списка в рабочей книге Excel"
ArticleTitle: "Обновление объекта списка в рабочей книге Excel – Документация API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Обновление"
type: docs
url: /ru/list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, Обновление таблицы, Excel API, REST, облачный SDK, обновление объекта списка, рабочая книга Excel, таблица"
description: "Узнайте, как обновить таблицу Excel с помощью API Aspose.Cells Cloud (версия 3.0). Включает endpoint, параметры, пример cURL, коды ошибок и примеры SDK."
weight: 20
---

Этот REST API обновляет свойства **объекта списка** (таблицы) в рабочей книге Excel.

## Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Схема тела запроса

DTO `listObject` содержит следующие поля. В теле запроса необходимо указать только те поля, значения которых вы хотите изменить.

| Поле                                             | Тип                | Обязательное | Описание                                                                    |
| ------------------------------------------------ | ------------------ | ----------- | --------------------------------------------------------------------------- |
| **DisplayName**                                  | string             | необязательное | Отображаемое имя таблицы.                                                   |
| **StartRow** / **StartColumn**                   | integer            | необязательное | Индекс первой строки/столбца таблицы (начинается с 0).                       |
| **EndRow** / **EndColumn**                       | integer            | необязательное | Индекс последней строки/столбца таблицы (начинается с 0).                    |
| **Range**                                        | string             | необязательное | Адрес диапазона таблицы в стиле A1 (например, `A1:D10`).                    |
| **ShowHeaderRow**                                | boolean            | необязательное | `true`, чтобы отобразить строку заголовков.                                 |
| **ShowTotals**                                   | boolean            | необязательное | `true`, чтобы отобразить строку итогов.                                      |
| **TableStyleName**                               | string             | необязательное | Имя встроенного стиля таблицы для применения.                               |
| **TableStyleType**                               | string             | необязательное | Тип стиля (`TableStyleLight`, `TableStyleMedium` и т.д.).                    |
| **ListColumns**                                  | array of objects   | необязательное | Коллекция определений столбцов (`Name`, `TotalsCalculation`).               |
| **Sorter**, **AutoFilter**, **ShowTableStyle…**  | object             | необязательное | Дополнительные параметры стилизации и фильтрации (см. полный DTO в спецификации OpenAPI). |

### Минимальный пример полезной нагрузки

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **Параметры запроса**

| Имя параметра       | Тип     | Расположение | Описание                                   |
| ------------------- | ------- | ------------ | ------------------------------------------ |
| **name**            | string  | путь         | Имя документа.                             |
| **sheetName**       | string  | путь         | Имя рабочего листа.                        |
| **listObjectIndex** | integer | путь         | Индекс объекта списка, который необходимо обновить. |
| **listObject**      | object  | тело         | DTO `ListObject` в теле запроса.          |
| **folder**          | string  | query        | Папка, содержащая документ.                |
| **storageName**     | string  | query        | Имя хранилища.                             |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST непосредственно из веб-браузера.

### Запрос

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Ответ

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Успешный ответ включает следующие поля:

| Поле                       | Тип    | Описание                                           |
| -------------------------- | ------ | -------------------------------------------------- |
| Code                       | integer| Код HTTP-статуса (200 — успех).                   |
| Status                     | string | Текстовое описание статуса.                        |
| UpdatedObject *(необязательное)* | object | Представление обновлённого `ListObject`, содержащее изменённые свойства. |

{{< /tab >}}

{{< /tabs >}}

## Ответы об ошибках

| Код HTTP | Описание                                                                          | Пример полезной нагрузки                                   |
| -------- | --------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **400**  | Неверный запрос — отсутствуют обязательные поля или некорректный JSON.            | `{ "Code": 400, "Message": "Invalid request body." }`      |
| **401**  | Неавторизованный запрос — отсутствует или недействителен токен JWT.              | `{ "Code": 401, "Message": "Authentication failed." }`     |
| **404**  | Не найдено — указанная рабочая книга, рабочий лист или объект списка не существует. | `{ "Code": 404, "Message": "Resource not found." }`        |
| **500**  | Внутренняя ошибка сервера — непредвиденное состояние на стороне сервера.          | `{ "Code": 500, "Message": "Server error." }`              |

## Часто задаваемые вопросы (FAQ)

<details>  
<summary>Как обновить объект списка с помощью API Aspose.Cells Cloud?</summary>

Используйте endpoint `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Включите в тело запроса JSON с теми свойствами, которые вы хотите изменить (например, `DisplayName`, `ShowHeaderRow`). Аутентифицируйтесь с помощью токена JWT в заголовке `Authorization`.

</details>

<details>  
<summary>Какой ответ я получу после успешного обновления?</summary>

Возвращается JSON-объект с `Code: 200` и `Status: "OK"`. В случае ошибки ответ содержит соответствующий HTTP-код и объект `Error` с описанием проблемы.

</details>

<details>  
<summary>Могу ли я обновить только часть свойств объекта списка?</summary>

Да. В теле запроса укажите только те поля, которые хотите изменить; все остальные поля останутся без изменений.

</details>

## См. также

- [Добавление объекта списка](https://docs.aspose.cloud/cells/list-objects/add/)
- [Получение объекта списка](https://docs.aspose.cloud/cells/list-objects/get/)
- [Удаление объекта списка](https://docs.aspose.cloud/cells/list-objects/delete/)

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список облачных SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells Cloud с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
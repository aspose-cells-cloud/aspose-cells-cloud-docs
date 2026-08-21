---
title: "Добавление условия форматирования"
type: docs
url: /conditional-formattings/add-format-condition/
aliases: [/add-a-format-condition/]
keywords: "Aspose.Cells Cloud, Conditional Formatting API, добавление условия форматирования, Excel REST API, Cells API"
description: "Узнайте, как добавить условие форматирования в лист Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Включает синтаксис запроса, параметры, пример безопасного вызова через cURL и фрагменты кода SDK."
ArticleTitle: "Добавление условия форматирования – документация API Aspose.Cells Cloud"
weight: 50
---

Этот REST API добавляет условие форматирования в лист.

## Безопасность и аутентификация
API Aspose.Cells Cloud защищены и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                 |
|---------------|--------|-------------|--------------------------------------------------------------------------|
| name          | string | path        | Имя рабочей книги Excel.                                                 |
| sheetName     | string | path        | Имя листа, содержащего диапазон, который необходимо отформатировать.     |
| index         | integer | path       | Нулевой индекс добавляемого или заменяемого условия форматирования.     |
| cellArea      | string | query       | Диапазон ячеек (например, `A1:C3`), к которому применяется условие.     |
| type          | string | query       | Тип условия (например, `Expression`, `CellValue`).                     |
| operatorType  | string | query       | Оператор условия (например, `Between`, `Equal`).                        |
| formula1      | string | query       | Первая формула или значение, используемое условием.                     |
| formula2      | string | query       | Вторая формула или значение (обязательна для некоторых операторов, таких как `Between`). |
| folder        | string | query       | Папка в хранилище, где расположена рабочая книга.                        |
| storageName   | string | query       | Имя сервиса хранилища (например, `Default`).                             |

### Ответы об ошибках

| HTTP-код | Причина                                           | Пример тела ответа                                                  |
|----------|---------------------------------------------------|----------------------------------------------------------------------|
| **400**  | Неверный запрос — отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Недопустимое значение параметра." }`   |
| **401**  | Неавторизован — отсутствует или недействителен токен JWT. | `{ "Code":"401", "Message":"Токен доступа отсутствует или недействителен." }` |
| **404**  | Не найдено — рабочая книга или лист не существуют. | `{ "Code":"404", "Message":"Файл не найден." }`                     |
| **500**  | Внутренняя ошибка сервера — непредвиденная ошибка сервера. | `{ "Code":"500", "Message":"Произошла непредвиденная ошибка." }`   |

### Успешный ответ

| HTTP-код | Причина                                         | Пример тела ответа                        |
|----------|-------------------------------------------------|-------------------------------------------|
| **200**  | OK — условие успешно добавлено или обновлено. | `{ "Code": "200", "Status": "OK" }`      |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать **cURL** для вызова API Aspose.Cells. Пример ниже демонстрирует полный запрос, включая пустое тело в формате JSON.

### Пример cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как вызывать облачные сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}
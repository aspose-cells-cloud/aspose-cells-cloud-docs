---
title: "Очистка условного форматирования"
type: docs
url: /ru/conditional-formattings/clear/
aliases: [  /ru/clear-all-condition-formattings/ ]
keywords: "Aspose.Cells Cloud, REST API, очистка условного форматирования, Excel, рабочие листы, JWT, v3.2"
description: "Удаление всех правил условного форматирования с рабочего листа с помощью API Aspose.Cells Cloud (v3.2). Ознакомьтесь с синтаксисом запроса, необходимыми параметрами, шагами аутентификации и образцами кода на различных SDK."
weight: 80
---

Этот REST API очищает все правила условного форматирования с рабочего листа.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Параметры запроса

| Имя параметра  | Тип    | Местоположение | Описание                                                          |
| -------------- | ------ | -------------- | ----------------------------------------------------------------- |
| **name**       | string | path           | Имя файла рабочей книги (например, `Book1.xlsx`).                |
| **sheetName**  | string | path           | Имя рабочего листа, из которого нужно удалить условное форматирование. |
| **folder**     | string | query          | _(Опционально)_ Путь к папке в хранилище, где расположена рабочая книга. |
| **storageName**| string | query          | _(Опционально)_ Имя сервиса хранилища.                            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) определяет публично доступное программное интерфейсное решение, а **OpenAPI Specification** позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. Приведенный ниже пример демонстрирует, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Ответы об ошибках

| HTTP-код | Причина                                              | Пример тела ответа                                                  |
| -------- | ---------------------------------------------------- | ------------------------------------------------------------------- |
| **400**  | Неверный запрос – отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Неверное значение параметра." }`        |
| **401**  | Неавторизованный доступ – отсутствует или некорректен JWT-токен. | `{ "Code":"401", "Message":"Токен доступа отсутствует или некорректен." }` |
| **404**  | Не найдено – рабочая книга или рабочий лист не существуют. | `{ "Code":"404", "Message":"Файл не найден." }`                     |
| **500**  | Внутренняя ошибка сервера – непредвиденная ошибка сервера. | `{ "Code":"500", "Message":"Произошла непредвиденная ошибка." }`   |

## Примеры SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}
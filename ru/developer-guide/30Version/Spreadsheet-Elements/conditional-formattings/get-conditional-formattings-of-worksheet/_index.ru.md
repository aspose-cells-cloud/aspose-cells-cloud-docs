---
title: "Получить правила условного форматирования"
type: docs
url: /ru/conditional-formattings/get-all/
aliases: [  /ru/get-conditional-formattings-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, условное форматирование, лист, API условного форматирования"
description: "Получить все правила условного форматирования, применённые к листу, с помощью REST API Aspose.Cells Cloud. Включает синтаксис запроса, шаги аутентификации, параметры, краткие примеры ответов и обработку ошибок."
weight: 20
---

Этот REST API возвращает правила условного форматирования, применённые к листу.

## Безопасность и аутентификация
API Aspose.Cells Cloud защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                    |
| ------------- | ------ | ------------ | ------------------------------------------- |
| name          | string | path         | Имя файла Excel.                            |
| sheetName     | string | path         | Имя листа.                                  |
| folder        | string | query        | Путь к папке, где хранится файл.            |
| storageName   | string | query        | Имя службы хранения (необязательно).        |

### Ответы об ошибках

| Код HTTP | Причина                                            | Пример тела ответа                                                  |
| -------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**  | Неверный запрос — отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Недопустимое значение параметра." }`   |
| **401**  | Неавторизован — отсутствует или недействителен JWT-токен. | `{ "Code":"401", "Message":"Отсутствует или недействителен токен доступа." }` |
| **404**  | Не найдено — книга или лист не существуют.         | `{ "Code":"404", "Message":"Файл не найден." }`                    |
| **500**  | Внутренняя ошибка сервера — непредвиденная ошибка сервера. | `{ "Code":"500", "Message":"Произошла непредвиденная ошибка." }`   |

<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">Спецификация OpenAPI</a> определяет общедоступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_Приведённый выше пример содержит только наиболее релевантные поля, чтобы сделать полезную нагрузку компактной._

**Параметры ответа**

| Параметр                             | Тип     | Описание                                               |
|--------------------------------------|---------|--------------------------------------------------------|
| Status                               | string  | Результат выполнения запроса (например, **OK**).      |
| ConditionalFormattings               | object  | Контейнер данных об условном форматировании.           |
| ConditionalFormattings.Count         | integer | Количество возвращённых правил условного форматирования. |
| ConditionalFormattings.ConditionalFormattingList | array   | Список объектов условного форматирования.              |
| ConditionalFormattingList[].sqref    | string  | Диапазон ячеек, к которому применяется форматирование (например, **A1:B10**). |
| ConditionalFormattingList[].FormatConditions | array   | Коллекция объектов условий форматирования для диапазона. |
| FormatConditions[].Priority          | integer | Приоритет оценки условия.                              |
| FormatConditions[].Type              | string  | Тип условия (например, **CellValue**).                |
| FormatConditions[].Operator          | string  | Оператор, используемый для условия (например, **GreaterThan**). |
| FormatConditions[].Formula1          | string  | Первая формула или значение условия.                   |
| FormatConditions[].Style             | object  | Стиль, применяемый при выполнении условия.             |
| Style.Font.Color                     | object  | Определение цвета шрифта в формате RGBA.               |
| Style.Font.IsBold                    | boolean | Указывает, является ли шрифт полужирным.               |

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Неверный запрос             | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Неавторизован               | Недействителен или отсутствует JWT-токен.             |
| 413 | Полезная нагрузка слишком велика | Размер загружаемого файла превышает допустимый лимит. |
| 500 | Внутренняя ошибка сервера   | Непредвиденная ошибка сервера.                        |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" target="_blank">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}